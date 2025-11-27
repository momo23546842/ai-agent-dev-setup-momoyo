# AI Agent Developer Setup

**Student:** Momoyo Kataoka  
**Cohort:** CH181125  
**Program:** Full Stack Developer and Agentic AI Industry Project Internship  
**Workshop:** AI Agent Developer Workshop - Week 1  
**Repository:** `ai-agent-dev-setup-momoyo`

---

## 📋 Overview

This repository documents my complete development environment setup for the AI Agent Developer Workshop. It demonstrates a fully functional AI-enhanced development environment with MCP (Model Context Protocol) server integration, enabling Claude Desktop to interact with external tools and services.

---

## ✅ Development Environment Checklist

### 1. Node.js Installation
**Status:** ✅ Completed  

<img src="images/node.png" width="600" alt="Node.js version output">

Node.js is required for running MCP servers and managing npm packages for AI agent development.

---

### 2. Git Installation
**Status:** ✅ Completed  

<img src="images/GitScreenshot 2025-11-25 185107.png" width="600" alt="Git version output">

Git enables version control and collaboration, essential for AI agent development workflows.

---

### 3. VS Code Insider + GitHub Copilot
**Status:** ✅ Completed

<img src="images/Github-copiloteScreenshot 2025-11-25 190553.png" width="600" alt="VS Code with GitHub Copilot enabled">

VS Code Insider provides cutting-edge IDE features, while GitHub Copilot enhances coding productivity through AI-powered code suggestions.

---

### 4. Claude Desktop with MCP Servers
**Status:** ✅ Completed (GitHub MCP server successfully connected and running)

Claude Desktop successfully loaded the MCP configuration file with 4 servers configured.  
Rolldice / Bootcamp / Calendar servers are configured and showing warning icons as expected for the current workshop stage, while the GitHub MCP server is fully running and able to access my repository.


#### **Server 1: Rolldice**
<img src="images/RolldiceScreenshot 2025-11-25 182306.png" width="600" alt="Rolldice MCP server">

**Purpose:** Demonstrates basic MCP tool calling and function execution patterns.

---

#### **Server 2: Bootcamp AI Agent**
<img src="images/bootcampScreenshot 2025-11-25 182604.png" width="600" alt="Bootcamp MCP server">

**Purpose:** Sample agent API showcasing interaction with development tools and environment management.

---

#### **Server 3: Calendar Booking**
<img src="images/calenderScreenshot 2025-11-25 182738.png" width="600" alt="Calendar MCP server">

**Purpose:** Demonstrates time-based actions, scheduling, and date/time manipulation capabilities.

---

#### **Server 4: GitHub MCP**
<img src="images/GithubRunningScreenshot 2025-11-27 112128.png" width="600" alt="GitHub MCP server">

**Purpose:** Enables AI to interact directly with GitHub repositories - creating issues, managing pull requests, and automating repository workflows.

**Verification:** Confirmed that the GitHub MCP server is running and can successfully interact with my repository `ai-agent-dev-setup-momoyo` from Claude Desktop.


---

## 📁 Repository Structure

```
ai-agent-dev-setup-momoyo/
├── README.md                          # This file
├── reflection.md                      # 500-word personal reflection
├── VERIFICATION.md                    # Proof of MCP server functionality
├── mcp-configs/
│   ├── claude-desktop-config.json    # Claude Desktop MCP configuration
│   ├── mcp-servers-list.md           # Detailed server documentation
│   └── connection-test.md            # Server connection test results
└── images/
    ├── node.png
    ├── GitScreenshot 2025-11-25 185107.png
    ├── Github-copiloteScreenshot 2025-11-25 190553.png
    ├── RolldiceScreenshot 2025-11-25 182306.png
    ├── bootcampScreenshot 2025-11-25 182604.png
    ├── calenderScreenshot 2025-11-25 182738.png
    └── GithubScreenshot 2025-11-25 182809.png
```

---

## 🔧 MCP Servers: Purpose & Functionality

### 1. **Rolldice Server**
- **Category:** Example/Tutorial Server
- **Functionality:** Generates random numbers, simulates dice rolls
- **Use Case:** Learning MCP tool calling patterns and basic function execution
- **Key Learning:** Demonstrates request/response flow between Claude and external tools

### 2. **Bootcamp AI Agent Server**
- **Category:** Development Tools Server
- **Functionality:** Provides AI agent training environment interaction
- **Use Case:** Managing bootcamp-specific workflows, tracking progress, accessing learning resources
- **Key Learning:** Shows how MCP can integrate domain-specific tools into AI workflows

### 3. **Calendar Booking Server**
- **Category:** Scheduling & Time Management Server
- **Functionality:** Creates, reads, updates calendar events; checks availability
- **Use Case:** Scheduling meetings, setting reminders, managing time-sensitive tasks
- **Key Learning:** Demonstrates stateful operations and time-based logic in MCP

### 4. **GitHub MCP Server**
- **Category:** Developer Productivity Server
- **Functionality:** Repository management, issue tracking, pull request automation
- **Use Case:** AI-assisted code review, automated issue creation, repository insights
- **Key Learning:** Real-world integration of AI with version control workflows

---

##  Troubleshooting Notes

### Issue: GitHub MCP Server Was Running but Not Responding to Commands

**Problem:**  
Although the GitHub MCP server showed **“Running”** in Claude Desktop, it did not respond to commands.  
For example, when I asked Claude to:

- list the files in the repository  
- retrieve README.md  
- access the root directory  

Claude returned errors such as:

- “No result received from client-side tool execution”
- “Repository not found”
- “Unable to access repository”

At first, it seemed like the MCP server itself was failing.

---

### Investigation Step 1: Suspected Token Permission Issue (But It Was Correct)

My first hypothesis was that the GitHub Personal Access Token (PAT) might not have enough permissions.  
I checked my token settings and confirmed:

✔ `repo` permission was fully enabled  
✔ public and private repo access allowed  
✔ the token was correctly placed in `claude-desktop-config.json`  
✔ Claude Desktop was fully restarted to load the updated token  

**Result:**  
The PAT was correctly configured — token permissions were *not* the cause.

---

### Investigation Step 2: MCP Server Configuration  
I also checked the MCP server configuration inside `claude-desktop-config.json`.  
Everything was correct, and the server status remained **Running**, meaning Claude successfully authenticated with GitHub.

---

### Final Root Cause: Incorrect Repository Name

The actual issue was much simpler:

❌ Claude was trying to access the wrong repository name.  
The repository name in my command did not exactly match the actual GitHub repo.

GitHub MCP cannot access a repository that doesn’t exist → so it returned no results.

---

### Fix Implemented

I renamed the repository to a clean and correct format:
<img src="testGithubandClaudeScreenshot 2025-11-27 151348.png" width="600" alt="GitHub MCP" >



## 🎯 Key Insights

### AI Agent Developer Mindset Shift
The setup process revealed a fundamental shift from traditional development to AI-augmented workflows:

1. **Tool Integration Focus:** MCP servers demonstrate that AI agents become more powerful when connected to external tools rather than operating in isolation.

2. **Declarative Configuration:** The `claude-desktop-config.json` approach shows how modern AI development emphasizes declarative tool definitions over imperative programming.

3. **Multi-Tool Orchestration:** Having 4 different MCP servers highlights how AI agents can coordinate multiple specialized tools to accomplish complex tasks.




