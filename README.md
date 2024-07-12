# TIA Worksheet with Power Pages and Dataverse
# Summary
The application is intended for internal use only. This document includes all the necessary details for running the application, related links, and automation details.
The following UI is custom and all the services are called through code. 

![image](https://github.com/user-attachments/assets/1eaa2e0e-8091-47cb-966d-a9f9434b6d04)

## Step by Step tutorial to add the custom UI.

Create entities (tables) in DATAVERSE and add all your metadata (columns). 


![Image](https://github.com/user-attachments/assets/514e45e7-3e09-4e71-b876-d0e90a512a62)

## Grant Permissions

Create the following three Site Settings from the Site Setting pages to access the Dataverse entities on the Power Page site with the values given. 
e.g. Webapi/InternalTableName/disableodatafilter

![Image](https://github.com/user-attachments/assets/2e5a76fe-777b-4d77-95bb-7a020f25d297)

## Table Permissions
Provide Table Permissions as per the requirements from the following screen

![Image](https://github.com/user-attachments/assets/ff2272a8-2a4c-4a03-b3d8-22e3aef0782e)


## Adding Custom Code
Go to Power Pages Management -> Web Pages -> Localized Content -> Home

![image](https://github.com/user-attachments/assets/ad157af8-2b0f-43b3-b121-da4dee99e075)


In the **General** tab add in the HTML code in the **Content** section as shown. 


![Image](https://github.com/user-attachments/assets/3ba441b3-2fc5-44b9-be53-8feca1b8a284)

```
<div class="container">
  <table>
    <thead>
      <tr>
        <th colspan="2" class="heading">TIA Worksheet</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Description</td>
        <td><select id="descriptionDropdown"></select></td>
      </tr>
      <tr>
        <td>Units (Input Value)</td>
        <td><input type="text" id="InputUnits" pattern="[0-9]*" title="Please enter units" required />
        <label id="refUnit" style="font-style: italic;"></label>
        <!-- <label id="unitsErrorMessage"> Error </label> -->
        </td>
      </tr>
      <tr>
        <td>Land Use Code</td>
        <td><label id="landUseCodeLabel"></label></td>
      </tr>
      <tr>
        <td>AM Peak</td>
        <td><label id="AMPeak"></label></td>
      </tr>
      <tr>
        <td>PM Peak</td>
        <td><label id="PMPeak"></label></td>
      </tr>
      <tr>
        <td>Weekend Peak (Sat.)</td>
        <td><label id="WeekendPeak"></label></td>
      </tr>
      <tr>
        <td>Weekend Peak (Sun.)</td>
        <td><label id="SundayPeak"></label></td>
      </tr>
      <tr>
        <td>Daily Total</td>
        <td><label id="DailyPeak"></label></td>
      </tr>
      <tr>
        <td>Result</td>
        <td><label id="result" class="result-text"></label></td>
      </tr>
      <tr>
        <td colspan="2" class="button-cell"><!-- Button for showing results --><button id="loadDataButton" class="show-results-button">Show Result</button></td>
      </tr>
    </tbody>
  </table>
</div>
<div data-component-theme="portalThemeColor7" id="i2753q" class="row sectionBlockLayout text-left" style="display: flex; flex-wrap: wrap; margin: 0px; min-height: auto; padding: 8px;">
  <div id="i6tfgh" class="container" style="padding: 0px; display: flex; flex-wrap: wrap;"><div id="ivapqp" class="col-md-12 columnBlockLayout" style="word-break: break-word; flex-grow: 1; display: flex; flex-direction: column; min-width: 300px;"></div></div>
</div>

```

Add Custom Javascript with the logic in the Advanced tab. 

![image](https://github.com/user-attachments/assets/0ef8c581-9693-462e-98f5-c01b8d4fe34e)


## Sync and Preview
After Saving changes always apply Sync from the Edit mode and Preview. 

![Image](https://github.com/user-attachments/assets/0e194aad-3ca8-4475-b1ce-77549ae45df5)


