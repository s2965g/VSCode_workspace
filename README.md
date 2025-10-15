# 🧰 VS Code Workspace for SQL, JSON/XML, and Markdown

An empty workspace for working  with SQL queries, JSON/XML data files, and Markdown documentation — not full code projects.  Includes formatting/prettifying, math objects and, previews tools for each file type.

CoPilot and Chat included.

---

## 📍 1. Folder Setup

Recommended default location (no admin rights required):

```
C:\Users\<username>\Documents\VSCode_Workspace\
```

Folder structure:

```
VSCode_Workspace/
│
├─ .vscode/
│   └─ settings.json          ← Editor and formatter configuration
│
├─ .prettierrc.json           ← Prettier formatting rules
│
├─ sql/                       ← SQL queries (group by topic)
│   ├─ connections/
│   ├─ queries/
│   └─ templates/
│
├─ data/                      ← JSON / XML / CSV data files
│
└─ docs/                      ← Markdown notes, meeting logs, README files
```

---

## 🧩 2. Required VS Code Extensions

Install the following extensions (open VS Code → press **Ctrl + Shift + X** → search and install):

| Purpose | Extension | ID |
|----------|------------|---|
| SQL Server querying | **SQL Server (mssql)** | `ms-mssql.mssql` |
| SQL formatting | **SQL Formatter** | `adpyke.vscode-sql-formatter` |
| JSON formatting | **Prettier – Code Formatter** | `esbenp.prettier-vscode` |
| JSON tools | **JSON Tools** | `eriklynd.json-tools` |
| XML support | **XML by Red Hat** | `redhat.vscode-xml` |
| Markdown editing | **Markdown All in One** | `yzhang.markdown-all-in-one` |
| Markdown with math | **Markdown+Math** | `goessner.mdmath` |
| Markdown linting | **markdownlint** | `DavidAnson.vscode-markdownlint` |
| GitHub Copilot (optional) | **Copilot + Copilot Chat** | `GitHub.copilot`, `GitHub.copilot-chat` |

Install them all at once from a terminal or PowerShell prompt:

```bash
code --install-extension ms-mssql.mssql `
     --install-extension adpyke.vscode-sql-formatter `
     --install-extension esbenp.prettier-vscode `
     --install-extension eriklynd.json-tools `
     --install-extension redhat.vscode-xml `
     --install-extension yzhang.markdown-all-in-one `
     --install-extension goessner.mdmath `
     --install-extension DavidAnson.vscode-markdownlint `
     --install-extension GitHub.copilot `
     --install-extension GitHub.copilot-chat
```

---

## ⚙️ 3. Settings Overview

This workspace includes two configuration files:

### `.vscode/settings.json`

Defines per-language formatting and preview behavior:

- SQL → formatted by **SQL Formatter**
- JSON/XML/Markdown → formatted by **Prettier** or **XML Red Hat**
- Markdown → live preview and KaTeX math rendering
- “Format on Save” is enabled globally

### `.prettierrc.json`

Ensures consistent formatting rules:

- 4-space indentation for JSON and SQL-style consistency
- 2-space indentation for Markdown/YAML
- 100-character line width limit
- Double quotes for JSON

---

## 🧮 4. File-Specific Behaviors

| File Type | Formatting Tool | Shortcut / Action |
|------------|------------------|------------------|
| `.sql` | SQL Formatter | **Shift + Alt + F** |
| `.json`, `.jsonc` | Prettier | **Shift + Alt + F** |
| `.xml` | Red Hat XML Formatter | **Shift + Alt + F** |
| `.md` | Prettier + Markdown Preview Enhanced | **Ctrl + K V** live preview |

---

## 🧠 5. Markdown Preview with Math

For technical documentation:

```markdown
Inline: The famous equation $E = mc^2$ relates energy and mass.

Display (block):

$$
\text{CVA} = \text{LGD} \times \int_0^T \text{EE}(t) \times \text{PD}'(t) \, dt
$$
```

---

## 🗃️ 6. SQL Usage Notes

- Press **Ctrl + Shift + P → “MS SQL: Connect”** to define a connection.
- Create **connection profiles** under `sql/connections/`.
- Run queries directly in VS Code; results show in a grid.

---

## 🧩 7. JSON & XML Notes

- JSON: auto-formatted on save; use **“JSON Tools → Sort JSON”** for quick cleanup.
- XML: uses the Red Hat XML extension for validation and formatting.
- Optional schema validation can be configured in `settings.json` via `"xml.fileAssociations"`.

---

## 🪶 8. Markdown & Notes

Shortcuts:

- **Ctrl + Shift + V** → open preview
- **Alt + Shift + F** → reformat

---

## 🔄 9. Portable

To move this environment to another machine:

1. Copy the entire `VSCode_Workspace` folder.
2. Reinstall the extensions (or use the same install command).
3. Open the folder in VS Code → settings apply automatically.

SEB syncs “Documents” to OneDrive, everything stays backed up automatically.

---

## ✅ 10. Quick Start

1. Clone or copy this folder to Documents directory.  
2. Install the listed extensions.  
3. Open VS Code → *File → Open Folder…* → select `VSCode_Workspace`.  
4. Start working:
   - Create or open a `.sql` file under `sql/`
   - Open and format `.json` or `.xml` files under `data/`
   - Create Markdown notes under `docs/`
