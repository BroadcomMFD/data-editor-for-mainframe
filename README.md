# FMP Editor
The FMP Editor extension for VS Code adds a modern user interface to [CA File Master Plus for MVS](https://www.broadcom.com/products/mainframe/testing-and-quality/file-master-plus). FMP Editor enhances the functionality of [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe) to allow you to apply record layouts to sequential, partitioned and VSAM data sets and interactively filter records using selection criteria. 

## Prerequisites
- CA File Master Plus version 10 or higher
- [Testing Tools Server](https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/ca-filemaster-plus/12-0/installing/install-testing-tools-server-and-rest-api.html)
- [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe)

## Connect to the Mainframe
To establish a connection to the mainframe, complete the following tasks:
- Install and configure the Zowe Explorer extension with at least one profile containing your mainframe credentials.
- In the **Server URL** field of the FMP Editor extension settings, specify the host URL and port of your Testing Tools Server instance in the format `http(s)://host:port`.

## Browse a Data Set

The FMP Editor extension enables you to:
- Browse mainframe data sets in character mode view.
- Apply CA File Master Plus layouts to browse records in single-record format.
- View records in hexadecimal format.
- Apply selection criteria interactively using the IDE interface to filter records.

### Open a Data Set
To open a data set using FMP editor, locate the data set in the Zowe Explorer tree, right click and select **Open with FMP**. The data set opens in Character Mode view.

To enable hexadecimal format in Character Mode view, open the **Options** panel and enable **Hexadecimal**. Hover over a record with the mouse cursor to show the hexadecimal value of the whole record.

### Apply a Layout
Apply a CA File Master Plus record layout to enable the Single-Record Format view and the use of selection criteria. To apply a layout, insert the layout DSN and member name in the **Layout** field under **Options**.

Once you provide a valid layout, you can switch between Character Mode and Single-Record Format views in the **Options** panel.

### Apply Selection Criteria

(coming soon)
