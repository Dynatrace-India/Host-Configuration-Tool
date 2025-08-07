# Dynatrace Host Monitoring Configuration Tool (v2.0)

A GUI-based Python tool designed to streamline and automate the configuration of host monitoring modes in Dynatrace. With this tool, users can fetch host data, select specific hosts based on different criteria (Monitoring Mode, Management Zone, or Host Group), and change their monitoring configuration — all without writing a single line of code.

---

## Features

- Secure input fields for Tenant URL and API Token.
- Fetch host data from the Dynatrace OneAgent API and generate a detailed Excel report.
- Filter and group hosts by:
  - Monitoring Mode
  - Management Zone
  - Host Group
- Select specific hosts via checkboxes or select all hosts in a category.
- Trigger configuration changes (Enable/Disable Monitoring) for selected hosts.
- Logs all actions and API calls in a log.txt file for audit and traceability.
- External executable integration for advanced configuration.

---

## Prerequisites
- Publicly accessible Tenant URL
- Access Token with respective scopes/permissions

## Steps:
- Step 1: Launch Main Tool (Dynatrace_Host_Data_Tool.exe)
  - Run the bundled Dynatrace_Host_Data_Tool.exe file.
  - Enter the Tenant URL and API Token.
  - Click Fetch Host Data to retrieve and store host details in host_data.xlsx.

- Step 2: Select Implementation Approach
  - Click Next.
  - Choose the configuration approach:
  - Monitoring Mode
  - Management Zone
  - Host Group

- Step 3: Select Hosts
  - Based on your approach:
     - Use dropdown to select a management zone or host group.
  - Choose hosts via checkboxes or click Select All Hosts.
  - Once selected, a file selected_host_ids.txt is generated.

- Step 4: Trigger Configuration Change
  - After file creation, click Run Configuration Change.
  - This will trigger the external-app.exe which uses the selected host IDs to change the monitoring mode in Dynatrace.

## Logging
All API calls and actions are logged in the "logs.txt" file in the root folder.

## Developed By
Abhishek Satpathy (abhishek.satpathy@dynatrace.com)
