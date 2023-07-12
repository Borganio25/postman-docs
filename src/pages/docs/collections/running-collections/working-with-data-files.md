---
title: "Importing data files in Postman"
updated: 2023-06-21
contextual_links:
  - type: section
    name: "Additional resources"
  - type: subtitle
    name: "Videos"
  - type: link
    name: "Loop Through a Data File | Postman Level Up"
    url: "https://youtu.be/RH8b3gbujPY"
  - type: subtitle
    name: "Blog posts"
  - type: link
    name: "Looping through a Data File in the Postman Collection Runner"
    url: "https://blog.postman.com/looping-through-a-data-file-in-the-postman-collection-runner/"
  - type: subtitle
    name: "Case Studies"
  - type: link
    name: "Reputation imports data files with Postman"
    url: "https://www.postman.com/case-studies/reputation/"
---

You can use data files to pass Postman sets of values to use in a collection run. By selecting a JSON or CSV data file in the Collection Runner, you can test your requests with multiple values as part of a single run.

Before exporting your file, take into account the following considerations.

* Preceding zeroes (for example, `000000345`) are stripped by Postman unless wrapped in double quotation marks (for example, `"000000345"`). Also, common spreadsheet programs (Microsoft Excel and Google Sheets) do not wrap values in quotes unless the value contains a comma or a double quotation mark.

* To treat numbers with leading zeroes as strings in Postman, reopen your exported CSV file in a text editor (or create a script) to wrap the number in double quotes.

* You do not need to add double quotes to simple integers. You do, however, need to format numbers larger than 15 digits as text in your spreadsheet program, so they are not truncated during export.

## Running collections with data files

You can select a data file to use in a [collection run](/docs/collections/running-collections/intro-to-collection-runs/).

1. Select <img alt="Runner icon" src="https://assets.postman.com/postman-docs/icon-runner-v9.jpg#icon" width="16px"> __Runner__ from the Postman footer.
1. Select your collection and drag it into the **Run Order** work area.
1. Select your data file with the __Select File__ button.

    <img alt="Data File Select" src="https://assets.postman.com/postman-docs/v10/select-data-file-1-v10.jpg" height="350px"/>
    <!-- Note this image will likely need updating when scheduled collection runs ships -->

1. After you select your data file, you can select **Preview** to inspect the data in the file before you start the run.

    ![Data File Preview](https://assets.postman.com/postman-docs/v10/preview-data-file-1-v10.jpg)

1. Select __Run using data files__ to begin the run with the values from the file. The Collection Runner runs the collection requests for each iteration in the data file. The output indicates the results for any tests you defined in your collection requests.

    > * You can test the steps in this page by first importing [the sample collection](https://assets.postman.com/postman-docs/58533790.json). Download and import it into Postman using __Import__ at the top of the sidebar.
    > ![Import Collection](https://assets.postman.com/postman-docs/v10/import-export-import-ui-v10-2.jpg)
    > * In the Collection Runner, choose the collection you imported. Download [the sample data file](https://assets.postman.com/postman-docs/58702589.json) and select it in the __Runner__ also.
    > * Note that the sample collection has a `POST` request which uses a `path` variable in the URL. This path variable is specified in each record in the data file. The request also uses a `value` variable in the body which is also pulled from the data file for each iteration. _The example request is to the [Postman Echo API](https://www.postman.com/postman/workspace/published-postman-templates/documentation/631643-f695cab7-6878-eb55-7943-ad88e1ccfd65?ctx=documentation), a learning resource that returns the data you send it._
    > ![Tests](https://assets.postman.com/postman-docs/data-file-tests-tab-v8.jpg)

1. Select a request in the Collection Runner results to get more details on its data.

    ![Collection Run Results](https://assets.postman.com/postman-docs/data-file-collection-run-v8.jpg)

Any data defined in the requests will be used when the collection runs, and your request data can reference values defined in the data file.

![Data File Value](https://assets.postman.com/postman-docs/request-body-data-run-v8.jpg)

## Accessing data file values

You can reference values defined in the data file throughout your requests, but accessing them with scripts requires a different technique. To use values from the data file in your __Tests__ or __Pre-request Script__ code, use `iterationData`, which provides access to the current data file record used to run the request.

```js
//get the 'value' field from the data file for this request run
pm.iterationData.get("value")
```

See the [Sandbox Reference](/docs/writing-scripts/script-references/postman-sandbox-api-reference/) for more on what you can do with iteration data.

## Errors when reading data files

You may encounter errors when Postman attempts to read your data file during a collection run. If this happens, you can take the following steps:

* Ensure your data file is formatted as either CSV or JSON.

* If you want to retain numbers with leading zeros, open the file in a text editor and wrap the number in double quotes as follows:

  ```csv
  index,specialNumber
  1,"000001"
  2,"9223372036854775807"
  ```

If the errors persist, [contact the Postman support team](https://support.postman.com/hc/en-us).
