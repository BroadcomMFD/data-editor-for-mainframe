# Data Editor for Mainframe
The Data Editor for Mainframe extension for VS Code adds a modern user interface to [CA File Master Plus for MVS](https://www.broadcom.com/products/mainframe/testing-and-quality/file-master-plus). Data Editor for Mainframe enhances the functionality of [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe) to allow you to apply record layouts to VSAM data sets and interactively filter records using selection criteria. 

## Prerequisites
- CA File Master Plus version 10 or higher
- [Testing Tools Server](https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/ca-filemaster-plus/12-0/installing/install-testing-tools-server-and-rest-api.html)
- [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe)

## Connect to the Mainframe
To establish a connection to the mainframe, complete the following tasks:
- Install and configure the Zowe Explorer extension with at least one profile containing your mainframe credentials.
- In the **Server URL** field of the Data Editor for Mainframe extension settings, specify the host URL and port of your Testing Tools Server instance in the format `http(s)://host:port`.

## Browse a Data Set
The Data Editor for Mainframe extension enables you to:
- Browse VSAM data sets in character mode view.
- Apply CA File Master Plus layouts to browse VSAM records in single-record format.
- View VSAM records in hexadecimal format.
- Filter records using selection criteria.

### Open a Data Set
To open a data set using Data Editor for Mainframe, locate the data set in the Zowe Explorer tree, right click and select **Open with Data Editor for Mainframe**. The data set opens in Character view.

To enable hexadecimal format, open the **Options** panel and enable **Hexadecimal**. Expand a record to view its hexadecimal value in Character view.

### Apply a Layout
Apply a record layout to enable the Single-Record view and the use of selection criteria. To apply a layout, open the **Options** panel and insert the layout DSN and member name in the **Layout** field.

After you provide a valid layout, you can switch between Character and Single-Record views in the **Options** panel.

### Apply Selection Criteria

You can apply selection criteria either manually or by importing criteria from a data set.

You can input selection criteria manually in the **Options** panel under **Selection Criteria**. Write selection criteria using the File Master Plus batch keyword SELRECIF. For an overview of the syntax, refer to the [File Master Plus documentation](https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/ca-filemaster-plus/12-0/using-batch/batch-reference-for-ca-file-master-plus/keywords/keyword-descriptions.html#concept.dita_de213555aa271bc5db6b08bc7a3ffe71e3bb4084_SELRECIFANDOR)

To import selection criteria from a data set, click **Import from Data Set** and specify the full DSN of your selection criteria data set and member.

After you specify your selection criteria, click **Apply** to filter records. Click **Clear Criteria** to remove your selection criteria and display all records.
