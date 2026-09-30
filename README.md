# Implement Client Script & UI Policy (Incident)

**Module:** ServiceNow System Administrator - A&S
**Team:** Team 1 (Team ID: 6abc9e994c64692dd41ee230)

## Team Members

| Name | Email | Role |
|------|-------|------|
| Gopalakrishnan V | v.gopal18032007@gmail.com | Team Leader |
| Lathika R | rameshramesh49312@gmail.com | Member |
| Nandhagopal S | nandhanandha90826@gmail.com | Member |

## Links

- **GitHub Repository:** [github.com/vgopal18032007-netizen/v.gopalakeishnan](https://github.com/vgopal18032007-netizen/v.gopalakeishnan)
- **Clone:** `git clone https://github.com/vgopal18032007-netizen/v.gopalakeishnan.git`
- **Demo Video:** `<paste Google Drive / YouTube link here>`
- **Project Drive Folder:** https://drive.google.com/drive/folders/1m_vXdKkujfkVq1x57h6bZ3Kj_07hdh4T?usp=sharing

---

## 1. Project Overview

`<2-3 lines: what this project does and why it is useful. Example: This project applies a UI Policy and a Client Script to the Incident form in ServiceNow to enforce data quality and guide users while they fill in an incident.>`

## 2. Objectives

- `<Objective 1, e.g. Make required fields mandatory based on Incident State>`
- `<Objective 2, e.g. Show or hide fields dynamically using a UI Policy>`
- `<Objective 3, e.g. Display field messages / alerts using a Client Script>`

## 3. Environment

| Item | Details |
|------|---------|
| Platform | ServiceNow Personal Developer Instance (PDI) |
| Release | `<e.g. Xanadu / Yokohama / Zurich>` |
| Table | Incident (`incident`) |
| Role used | `admin` |

## 4. Implementation

### 4.1 UI Policy

| Property | Value |
|----------|-------|
| Name | `<UI Policy name>` |
| Table | Incident |
| Short description | `<...>` |
| Condition | `<e.g. State is Resolved>` |
| Run scripts | `<Yes / No>` |

**UI Policy Actions**

| Field | Mandatory | Visible | Read-only |
|-------|-----------|---------|-----------|
| `<field>` | `<True/False/Leave alone>` | `<...>` | `<...>` |
| `<field>` | `<...>` | `<...>` | `<...>` |

**Navigation:** System UI > UI Policies > New

### 4.2 Client Script

| Property | Value |
|----------|-------|
| Name | `<Client Script name>` |
| Table | Incident |
| Type | `<onChange / onLoad / onSubmit / onCellEdit>` |
| Field name | `<field, for onChange>` |
| Active | True |

**Script**

```javascript
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
    if (isLoading || newValue === '') {
        return;
    }
    // TODO: add your logic here
}
```

**Navigation:** System Definition > Client Scripts > New

## 5. Test Cases

| # | Scenario | Steps | Expected Result | Actual Result | Status |
|---|----------|-------|-----------------|---------------|--------|
| 1 | `<...>` | `<...>` | `<...>` | `<...>` | Pass / Fail |
| 2 | `<...>` | `<...>` | `<...>` | `<...>` | Pass / Fail |
| 3 | `<...>` | `<...>` | `<...>` | `<...>` | Pass / Fail |

## 6. Screenshots

Store images in a `screenshots/` folder and link them here.

| Description | Screenshot |
|-------------|------------|
| UI Policy configuration | `![UI Policy](screenshots/ui-policy.png)` |
| UI Policy actions | `![Actions](screenshots/ui-policy-actions.png)` |
| Client Script configuration | `![Client Script](screenshots/client-script.png)` |
| Incident form: rule firing | `![Result](screenshots/result.png)` |

## 7. Repository Structure

```
.
├── README.md
├── scripts/
│   └── client_script.js
├── screenshots/
├── update-set/
│   └── incident_client_script_ui_policy.xml
└── docs/
    └── project_report.pdf
```

## 8. Team Contributions

| Member | Contribution |
|--------|--------------|
| Gopalakrishnan V | `<e.g. UI Policy setup, GitHub repo>` |
| Lathika R | `<e.g. Client Script, testing>` |
| Nandhagopal S | `<e.g. Documentation, demo video>` |

## 9. Conclusion

`<2-3 lines summarising what was achieved and what was learned.>`

## 10. Future Enhancements

- `<e.g. Add a UI Action or Business Rule for server-side validation>`
- `<e.g. Apply the same rules to the Service Portal>`
