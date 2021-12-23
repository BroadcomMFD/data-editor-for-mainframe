# Data Editor for Mainframe
The Data Editor for Mainframe extension for VS Code adds a modern user interface to [File Master Plus for MVS](https://www.broadcom.com/products/mainframe/testing-and-quality/file-master-plus). Data Editor for Mainframe enhances the functionality of [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe) to allow you to apply record layouts to VSAM data sets and interactively filter records using selection criteria. 

## Prerequisites
- File Master Plus version 10 or higher
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

## Technical Assistance and Support for Data Editor for Mainframe

The Data Editor for Mainframe extension is made available to customers on the Visual Studio Code Marketplace in accordance with the terms and conditions contained in the provided End-User License Agreement (EULA).

If you are on active support for File Master Plus, you get technical assistance and support in accordance with the terms, guidelines, details, and parameters that are located within the Broadcom [Working with Support](https://support.broadcom.com/external/content/release-announcements/CA-Support-Policies/6933) guide.

This support generally includes:

* Telephone and online access to technical support
* Ability to submit new incidents 24x7x365
* 24x7x365 continuous support for Severity 1 incidents
* 24x7x365 access to CA Support Online
* Interactive remote diagnostic support
* Technical support cases must be submitted to Broadcom in accordance with guidance provided in “Working with Support”.

Note: To receive technical assistance and support, you must remain compliant with “Working with Support”, be current on all applicable licensing and maintenance requirements, and maintain an environment in which all computer hardware, operating systems, and third party software associated with the affected Broadcom CA software are on the releases and version levels from the manufacturer that Broadcom designates as compatible with the software. Changes you elect to make to your operating environment could detrimentally affect the performance of Broadcom CA software and Broadcom shall not be responsible for these effects or any resulting degradation in performance of the Broadcom CA software. Severity 1 cases must be opened via telephone and elevations of lower severity incidents to Severity 1 status must be requested via telephone.
