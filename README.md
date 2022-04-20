# Data Editor for Mainframe
The Data Editor for Mainframe extension for VS Code adds a modern user interface to [File Master Plus for MVS](https://www.broadcom.com/products/mainframe/testing-and-quality/file-master-plus). Data Editor for Mainframe allows you to:

- Browse and edit VSAM data sets, sequential data sets and PDS members.
- Apply layouts to view data set records in single-record format.
- Interactively filter records using selection criteria.

## Example Use Cases
As an application developer, you can use Data Editor for Mainframe to:

- Filter and format data set records using selection criteria and layouts.
- View non-printable characters in HEX mode to diagnose issues with your application.
- Create new VSAM data sets with test data to debug the code.

To find out more about the capabilities of this extension, see this [blog post](https://medium.com/modern-mainframe/want-to-read-a-vsam-file-from-vs-code-bfc2bc0eba86).

## Prerequisites
Before you install Data Editor for Mainframe, ensure that you have installed and configured:

- File Master Plus version 10 or higher
- [Testing Tools Server](https://techdocs.broadcom.com/us/en/ca-mainframe-software/devops/ca-filemaster-plus/12-0/installing/install-testing-tools-server-and-rest-api.html)

We also recommend that you install [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe) to leverage all of this extension's features.

## Getting Started

Before you start using Data Editor for Mainframe, you establish a connection from the extension to the mainframe through a Testing Tools Server instance. We also recommend that you configure Zowe Explorer and set up a Zowe profile.

### Connect to the Mainframe

In the **Server URL** field of the Data Editor for Mainframe extension settings, specify the host URL and port of your Testing Tools Server instance in the following format: `http(s)://host:port`.

**Note**: Data Editor for Mainframe can only connect to one Testing Tools Server instance at a time. If you have connections to multiple subsystems with different Testing Tools Servers, the server URL in the extension settings must be changed manually to access data sets from a different subsystem.

### Integrate with Zowe Explorer

Integrating Data Editor for Mainframe with Zowe Explorer lets you:

- Start browse and edit sessions directly from the data set tree.
- View data set info.
- Save your mainframe credentials securely in a Zowe profile.

To enable these features, install the [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe) extension and configure a profile containing your mainframe credentials.

## Using

The Data Editor for Mainframe extension enables you to:

- Browse and edit VSAM data sets (KSDS, ESDS and RRDS), sequential data sets, and PDS members.
- Apply File Master Plus layouts to browse and edit records in single-record format.
- View records in hexadecimal format.
- Filter records using selection criteria.
- View data set info.

### Browse a Data Set

To start a Browse session using Data Editor for Mainframe, locate the data set in the Zowe Explorer tree, right click and select **Browse with Data Editor for Mainframe**. If you do not have Zowe Explorer installed, you can also select **Browse with Data Editor for Mainframe** from the command pallette (**F1**), and insert your mainframe username and password. The data set opens in Character view.

To show or hide the hexadecimal value of a record in Character view, use the arrow to the left of the record.

### Edit a Data Set

To start an Edit session using Data Editor for Mainframe, locate the data set in the Zowe Explorer tree, right click and select **Edit with Data Editor for Mainframe**. If you do not have Zowe Explorer installed, you can also select **Edit with Data Editor for Mainframe** from the command pallette (**F1**), and insert your mainframe username and password. The data set opens in Character view.

You can edit records in a data set either in Character view, or in Single-Record view after you apply a record layout. Changes are first saved locally to VS Code and then saved to the mainframe. Protected fields are highlighted and cannot be edited.

You can insert new records into a PDS member, a sequential file or a VSAM KSDS. To insert a new record, select an existing record in character view, right click, and select **insert row above** or **insert row below**. To copy the selected record, right click and select **copy**.

To save your changes to the mainframe, select **Save** from the **File** menu. Ensure that you save your changes to the mainframe before switching between view modes.

### Apply a Layout

Apply a record layout to enable the Single-Record view and the use of selection criteria in a Browse or Edit session. To apply a layout, open the **Options** panel and insert the layout DSN and member name in the **Layout** field.

After you provide a valid layout, you can switch between Character and Single-Record views in the **Options** panel.

Changes that you make in an Edit session which use an incompatible data type to the field definition in the layout (e.g. alphabetic characters in a field defined as a number) are automatically reverted and not saved.

### Apply Selection Criteria

Apply selection criteria to filter records in a Browse or Edit session. You can either apply selection criteria manually or by importing criteria from a data set.

Input selection criteria manually in the **Options** panel under **Selection Criteria**. Write selection criteria using the File Master Plus batch keyword SELRECIF. For an overview of the syntax, refer to the [File Master Plus documentation](https://techdocs.broadcom.com/fmp).

To import selection criteria from a data set, click **Import from Data Set** and specify the full DSN of your selection criteria data set and member.

After you specify your selection criteria, click **Apply** to filter records. Click **Clear Criteria** to remove your selection criteria and display all records.

### View Data Set Info

To view information about a data set, locate the data set in the Zowe Explorer tree, right click and select **Show properties**. This option is only available through Zowe Explorer.

## Technical Assistance and Support for Data Editor for Mainframe

The Data Editor for Mainframe extension is made available to customers on the Visual Studio Code Marketplace in accordance with the terms and conditions contained in the provided End-User License Agreement (EULA).

If you are on active support for File Master Plus, you get technical assistance and support in accordance with the terms, guidelines, details, and parameters that are located within the Broadcom [Working with Support](https://support.broadcom.com/external/content/release-announcements/CA-Support-Policies/6933) guide.

This support generally includes:

* Telephone and online access to technical support
* Ability to submit new incidents 24x7x365
* 24x7x365 continuous support for Severity 1 incidents
* 24x7x365 access to Broadcom Support
* Interactive remote diagnostic support
* Technical support cases must be submitted to Broadcom in accordance with guidance provided in “Working with Support”.

Note: To receive technical assistance and support, you must remain compliant with “Working with Support”, be current on all applicable licensing and maintenance requirements, and maintain an environment in which all computer hardware, operating systems, and third party software associated with the affected Broadcom software are on the releases and version levels from the manufacturer that Broadcom designates as compatible with the software. Changes you elect to make to your operating environment could detrimentally affect the performance of Broadcom software and Broadcom shall not be responsible for these effects or any resulting degradation in performance of the Broadcom software. Severity 1 cases must be opened via telephone and elevations of lower severity incidents to Severity 1 status must be requested via telephone.

## Privacy Notice

The extensions for Visual Studio Code developed by Broadcom Inc., including its corporate affiliates and subsidiaries, ("Broadcom") are provided free of charge, but in order to better understand and meet its users’ needs, Broadcom may collect, use, analyze and retain anonymous users’ metadata and interaction data, (collectively, “Usage Data”) and aggregate such Usage Data with similar Usage Data of other Broadcom customers. Please find more detailed information in [License and Service Terms & Repository](https://www.broadcom.com/company/legal/licensing).

This data collection uses built-in Microsoft VS Code Telemetry, which can be disabled, at your sole discretion, if you do not want to send Usage Data.

The current release of Data Editor for Mainframe collects anonymous data for the following events:
* Activation of this VS Code extension
* New records
* Browse and edit sessions
* Changes made in single-record view
* Local saves

Each such event is logged with the following information:
* Event time
* Operating system and version
* Country or region
* Anonymous user and session ID
* Version numbers of Microsoft VS Code and Data Editor for Mainframe
