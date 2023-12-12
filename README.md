# CRM Automation

## Problem

A company with a small sales team (under 5 people) wants to build a mini CRM system with the following key features:

- Automatically assign leads to salespeople when new leads come in.
- Nurture leads and manage the status of each lead.
- Access detailed information about individual leads.
- Manage the performance of each team member and the entire team.

## Dataset

The dataset consists of registration form entries for a workshop, with the following columns of information:
- Timestamp: The time when the form was filled out.
- Họ tên *(Full Name)*: The full name of the person filling out the form.
- Số điện thoại *(Phone Number)*: The phone number of the person filling out the form.
- Nghề nghiệp *(Occupation)*: The current job or occupation group.
- Nhu cầu chuyển ngành *(Career Transition Needs)*: The participant's demand for a career transition or course.
- Loại vé *(Ticket Class)*: The type of ticket registered for. There are three classes: Free, Premium, VIP, each with different privileges.

The dataset is in Vietnamese. You can download the original dataset [here](https://docs.google.com/spreadsheets/d/18CuhENE7h8tIXJWPeQimqPaE_V4ZlrzshgH8eZM3Zp0/edit?usp=sharing).

## Approach

### Automatically assign leads

- Identify the total number of salespeople.
- Retrieve the current row number using the `ROW()` function.
- Calculate the remainder (mod) when dividing the current row number by the total number of salespeople. Each resulting remainder will correspond to a specific salesperson. For example, with 4 salespeople, leads would be assigned as follows:
  - Lead 1 → Salesperson 1.
  - Lead 2 → Salesperson 2.
  - Lead 3 → Salesperson 3.
  - Lead 4 → Salesperson 4.
  - Lead 5 → Salesperson 1 (and so on...)

This method ensures an equitable distribution of leads among the available salespeople by cycling through them in a repeating pattern.

<img width="960" alt="Automatically assign leads to salespeople" src="https://github.com/thanhtruchhh/CRM-automation/assets/145547282/38a87b40-302c-403a-8d9b-eaf6a86908c8">

### Nurture leads and manage sales performance

Link data, process, aggregate, and visualize charts.

## Output

In this project, I assume the sales team consists of 4 salespeople. You can access the files directly [here](https://drive.google.com/drive/folders/1C3uhy2QjwjkuK78PVi2eR8x8oS8EE2RQ?usp=sharing), including:

- 1 data source file.
- 4 lead data files divided for each salesperson.
- 1 file for the manager to oversee performance.

<img width="960" alt="Leads are distributed to individual salesperson files for nurturing" src="https://github.com/thanhtruchhh/CRM-automation/assets/145547282/a7135792-bd58-4bb3-9ef6-9b1ee482b8a2">

<img width="672" alt="Salesperson dashboard" src="https://github.com/thanhtruchhh/CRM-automation/assets/145547282/3cd680d5-fba1-4d78-b0bf-b8d996e28e6a">

<img width="504" alt="Lead overview" src="https://github.com/thanhtruchhh/CRM-automation/assets/145547282/5fcc7bc9-a8d7-4e36-8d6e-749f93f4a8d9">

<img width="819" alt="Salesperson performance" src="https://github.com/thanhtruchhh/CRM-automation/assets/145547282/90fa7fe5-167a-447d-b01d-e29a54fe2632">

<img width="960" alt="Detail performance" src="https://github.com/thanhtruchhh/CRM-automation/assets/145547282/3daf2a46-3f01-4a59-a79f-0a2c36719037">
