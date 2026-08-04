<div id="header" align="center">

[![GitHub issues](https://img.shields.io/github/issues-raw/BroadcomMFD/data-editor-for-mainframe?style=flat-square)](https://github.com/BroadcomMFD/data-editor-for-mainframe/issues)
[![slack](https://img.shields.io/badge/chat-on%20Slack-blue)](https://join.slack.com/t/che4z/shared_invite/zt-37ewynplx-wCoabaIDxN6Ofm4_XBinZA)
[![Code4z](https://img.shields.io/badge/Code4z-marketplace-cc092f)](https://marketplace.visualstudio.com/search?term=code4z&target=VSCode)
</div>

# Data Editor for Mainframe

The Data Editor for Mainframe Code4z extension adds a modern user interface to [File Master Plus for MVS](https://www.broadcom.com/products/mainframe/testing-and-quality/file-master-plus). The Data Editor for Mainframe extension enables engineers to view and edit test data directly in VS Code without needing to submit jobs or use the traditional 3270 green screen interface. Data Editor for Mainframe includes the following features:

- Browse and edit VSAM data sets, sequential data sets and PDS members.
- Apply layouts to view data set records in single-record format.
- Interactively filter records using selection criteria.

<img align="left" alt="This extension is part of the Code4z experience" width="80" height="82" src="https://raw.githubusercontent.com/BroadcomMFD/code4z/refs/heads/main/icon5.png" />

Data Editor for Mainframe is part of the [Code4z](https://techdocs.broadcom.com/code4z) experience from Broadcom, which offers a modern experience for mainframe application developers. To get started with Code4z, check out our foundational [extension pack](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.code4z-extension-pack).

<br/>

<details>
<summary id="address-software-requirements"><span style="font-size: 1.5em"><b>Address Software Requirements</b></span><hr></summary>

Before you install Data Editor for Mainframe, ensure that your site and workstation meet the following requirements:

### Server
- File Master Plus version 11 or higher
- If you use File Master Plus version 11, acquire and install PTF LU21252
- If you use File Master Plus version 12, acquire and install PTF LU21249
- File Master Plus Server with GUI API enabled
- To connect to Data Editor for Mainframe through the Zowe API Mediation Layer, integrate your File Master Plus Server with Zowe API ML.

For more information, see the [File Master Plus documentation](https://techdocs.broadcom.com/fmp).

### Client
- Visual Studio Code or Github Codespaces

</details>

<details>
<summary id="integrate-with-zowe-explorer"><span style="font-size: 1.5em"><b>Integrate with Zowe Explorer</b></span><hr></summary>

Integrate Data Editor for Mainframe with Zowe Explorer to enable the following features of this extension:

- Start browse and edit sessions directly from the data set tree.
- View data set info.
- Save your mainframe credentials securely in a Zowe profile.
- Use the Single Sign-On feature of Zowe API ML.

To enable these features, install the [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe) extension and configure a profile that contains your mainframe credentials. To use the Single-Sign On feature of Zowe API ML, ensure that your Zowe profile is logged into the Zowe Explorer authentication service.

If you do not have Zowe Explorer installed and configured, you can start browse and edit sessions from the command palette and must enter your mainframe credentials each time.

<div align="center">
<a href="https://www.openmainframeproject.org/all-projects/zowe/conformance"><img alt="This extension is Zowe v3 conformant" src="https://artwork.openmainframeproject.org/other/zowe-conformant/zowev3/explorer-vs-code/color/zowe-conformant-zowev3-explorer-vs-code-color.png" width=208 height=156 /></a>
</div>

</details>

<details>
<summary id="add-a-connection-to-the-mainframe"><span style="font-size: 1.5em"><b>Add a Connection to the Mainframe</b></span><hr></summary>

In the **Server URL** field of the Data Editor for Mainframe extension settings, specify one of the following:
- The host URL and port of your File Master Plus Server instance in the format `http(s)://host:port`
- The host URL, port and service ID of your Zowe API ML Gateway instance in the format `http(s)://host:port/serviceid/api/v1`

**Note**: Data Editor for Mainframe can only connect to one File Master Plus Server at a time. If you have connections to multiple subsystems with different File Master Plus Servers, the server URL in the extension settings must be changed manually to access data sets from a different subsystem.

</details>

<details>
<summary id="browse-a-data-set"><span style="font-size: 1.5em"><b>Browse a Data Set</b></span><hr></summary>

To start a Browse session using Data Editor for Mainframe, locate the data set in the Zowe Explorer tree, right click and select **Browse with Data Editor for Mainframe**.

If you do not have Zowe Explorer installed, press **F1** to open the command palette, and run the command **Browse with Data Editor for Mainframe**. Insert your mainframe username and password when prompted.

The data set opens in Character view.

To show or hide the hexadecimal value of a record in Character view, use the arrow to the left of the record.

</details>

<details>
<summary id="edit-a-data-set"><span style="font-size: 1.5em"><b>Edit a Data Set</b></span><hr></summary>

To start an Edit session using Data Editor for Mainframe, locate the data set in the Zowe Explorer tree, right click and select **Edit with Data Editor for Mainframe**.

If you do not have Zowe Explorer installed, press **F1** to open the command palette, and run the command **Edit with Data Editor for Mainframe**. Insert your mainframe username and password when prompted.

You can edit records in a data set either in Character view, or in Single-Record view after you apply a record layout. Changes are first saved locally to VS Code and then saved to the mainframe. Protected fields are highlighted and cannot be edited.

You can insert new records into a PDS member, a sequential file or a VSAM KSDS. To insert a new record, select an existing record in character view, right click, and select **insert row above** or **insert row below**. To copy the selected record, right click and select **copy**.

To save your changes to the mainframe, select **Save** from the **File** menu. Ensure that you save your changes to the mainframe before switching between view modes.

</details>

<details>
<summary id="apply-a-layout"><span style="font-size: 1.5em"><b>Apply a Layout</b></span><hr></summary>

Apply a record layout to enable the Single-Record view and the use of selection criteria in a Browse or Edit session. To apply a layout, open the **Options** panel and insert the layout DSN and member name in the **Layout** field.

After you provide a valid layout, you can switch between Character and Single-Record views in the **Options** panel.

Changes that you make in an Edit session which use an incompatible data type to the field definition in the layout (e.g. alphabetic characters in a field defined as a number) are automatically reverted and not saved.

</details>

<details>
<summary id="apply-selection-criteria"><span style="font-size: 1.5em"><b>Apply Selection Criteria</b></span><hr></summary>

Apply selection criteria to filter records in a Browse or Edit session. You can either apply selection criteria manually or by importing criteria from a data set.

Input selection criteria manually in the **Options** panel under **Selection Criteria**. Write selection criteria using the File Master Plus batch keyword SELRECIF. For an overview of the syntax, refer to the [File Master Plus documentation](https://techdocs.broadcom.com/fmp).

To import selection criteria from a data set, click **Import from Data Set** and specify the full DSN of your selection criteria data set and member.

After you specify your selection criteria, click **Apply** to filter records. Click **Clear Criteria** to remove your selection criteria and display all records.

</details>

<details>
<summary id="view-data-set-info"><span style="font-size: 1.5em"><b>View Data Set Info</b></span><hr></summary>

To view information about a data set, locate the data set in the Zowe Explorer tree, right click and select **Show Properties**. This option is only available through Zowe Explorer.

</details>

<details>
<summary id="technical-assistance-and-support"><span style="font-size: 1.5em"><b>Technical Assistance and Support</b></span><hr></summary>

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

</details>

<details>
<summary id="privacy-notice"><span style="font-size: 1.5em"><b>Privacy Notice</b></span><hr></summary>

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

</details>
