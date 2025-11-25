# VERIFICATION

## 1. MCP servers in Claude Desktop

The following screenshot shows all four MCP servers (Rolldice, Bootcamp AI Agent, Calendar Booking, GitHub) configured in Claude Desktop.

### Rolldice 
<img src="images/RolldiceScreenshot 2025-11-25 182306.png" width="400">

### Bootcamp
<img src="images/bootcampScreenshot 2025-11-25 182604.png" width="400">

### Calendar
<img src="images/calenderScreenshot 2025-11-25 182738.png" width="400">

### GitHub
<img src="images/GithubScreenshot 2025-11-25 182809.png" width="400">

> Note: Some workshop servers (Rolldice, Bootcamp, Calendar) show a failed status because they are sample servers provided in the bootcamp material and are not actually running in the background. The configuration itself is correctly set up in `claude-desktop-config.json`.

# GitHub MCP Server – Interaction Verification

This section demonstrates that the **GitHub MCP Server** is correctly connected and functioning in Claude Desktop.  
I confirmed this by successfully using the GitHub MCP tools to interact with my repository:

**Repository:** `momo23546842/ai-agent-dev-setup--momoyo-`

---

##  What I Did

I asked Claude to retrieve the `README.md` file using the GitHub MCP server.  
Here is the exact command I sent to Claude:


Claude executed the MCP tool request and retrieved the file successfully.

---

## Tool Execution Proof

Claude returned the following MCP tool response:

- **Ran:** `Get file or directory contents` (GitHub MCP Server)  
- **File returned:** `README.md`  
- Claude displayed the contents directly in the conversation.

This confirms:

✔ The GitHub MCP server is connected  
✔ Tool calls to the GitHub API are working  
✔ Claude can fetch files from my repository  

---

##  Screenshot

<img src="images/exampleScreenshot 2025-11-26 093053.png" width="400">

This screenshot demonstrates:

- GitHub MCP server is enabled  
- The MCP tool successfully retrieved the file  
- The interaction with the GitHub repository is functioning  

---

## Summary

- The GitHub MCP server works correctly in Claude Desktop.  
- Claude successfully fetched a file from my GitHub repository.  
- This fulfills the requirement:  
  **“Example of using GitHub MCP server to interact with your repository.”**




