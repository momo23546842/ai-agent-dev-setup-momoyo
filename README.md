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
ai-agent-dev-setup--momoyo/
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

## 🐛 Troubleshooting Notes

### Issue 1: MCP Server Binaries Not Found
**Problem:** All four MCP servers show "failed" status in Claude Desktop despite correct configuration.

**Root Cause:** Official npm packages for `rolldice`, `bootcamp`, `calendar`, and `github` MCP servers are not yet publicly available.

**Current Status:** Configuration file is correctly loaded; servers will activate once binaries are provided during Week 1.

**Verification:** Confirmed this behavior is consistent across all workshop participants and is expected for initial setup.

---


## 🎯 Key Insights

### AI Agent Developer Mindset Shift
The setup process revealed a fundamental shift from traditional development to AI-augmented workflows:

1. **Tool Integration Focus:** MCP servers demonstrate that AI agents become more powerful when connected to external tools rather than operating in isolation.

2. **Declarative Configuration:** The `claude-desktop-config.json` approach shows how modern AI development emphasizes declarative tool definitions over imperative programming.

3. **Multi-Tool Orchestration:** Having 4 different MCP servers highlights how AI agents can coordinate multiple specialized tools to accomplish complex tasks.




