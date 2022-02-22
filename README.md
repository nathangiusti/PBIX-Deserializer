# PBIX-Deserializer

The PBIX Deserializer action scans for any changed PBIX files in your repo and creates a folder of json files showing the contents.

For a file "Example Report.pbix" with "Section 1", "Section 2", and "Section 3" will create a folder called "ExampleReport" with 4 files inside:
- Example Report.json
- Section 1.json
- Section 2.json
- Section 3.json

Example use:

~~~~
name: Reformat PBIX Files
on: [pull_request]
jobs:
  Reformat-PBIX-Files:
    runs-on: ubuntu-latest
    steps:
        - name: PBIX Deserializer
          uses: nathangiusti/PBIX-Deserializer@v1.3
~~~~

If you require more fine tuning than this action allows, the heart of the PBIX Deserializer action is located here:
https://github.com/nathangiusti/Power-BI-VC-Utils/

You can use/modify that action to create a new action/workflow.
