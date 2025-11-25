# AI Agent Developer Setup 
This repository documents my complete development environment setup for the AI Agent Developer Workshop (Cohort: MomoyoKataoka).


---

## 📌 Development Environment Checklist

### ✅ Node.js Installed
Screenshot:  
<img src="images/node-version.png" width="400">

### ✅ Git Installed
Screenshot:  
<img src="images/git-version.png" width="400">

### ✅ VS Code Insider + GitHub Copilot Enabled
Screenshot:  
<img src="images/vscode-insider.png" width="400">

### ✅ Claude Desktop with 4 MCP Servers Loaded (Rolldice, Bootcamp, Calendar, GitHub)
  
Screenshot:  
Rolldice
<img src="images/RolldiceScreenshot 2025-11-25 182306.png" width="400">
Bootcamp
<img src="images/bootcampScreenshot 2025-11-25 182604.png" width="400">
Calender
<img src="images/calenderScreenshot 2025-11-25 182738.png" width="400">
Github
<img src="images/GithubScreenshot 2025-11-25 182809.png" width="400">

---

## 📁 MCP Servers Overview

| Server | Purpose |
|--------|----------|
| Rolldice | Example MCP server used to demonstrate tool calling & function execution. |
| Bootcamp AI Agent | Sample agent API for interacting with simple development tools. |
| Calendar Booking | Demonstrates date/time-based actions and scheduling. |
| GitHub MCP | Allows AI to interact with GitHub repositories via MCP. |

---

## 🛠 Troubleshooting Notes

- Attempted to run MCP servers locally, but the official packages for `rolldice`, `bootcamp`, `calendar`, and `github` are not available on npm or GitHub.
- Claude Desktop correctly loaded the MCP configuration file, but all servers show **failed** status due to missing server binaries.
- This behavior is consistent with all other students and expected for Week 1.
- Verified Node.js, Git, VS Code Insider, and Claude Desktop setups.

---

## 📦 Repository Structure

