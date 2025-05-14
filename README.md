[![MseeP.ai Security Assessment Badge](https://mseep.net/pr/mordavid-bloodhound-mcp-ai-badge.png)](https://mseep.ai/app/mordavid-bloodhound-mcp-ai)

# BloodHound-MCP

![BloodHound-MCP](/images/BloodHound-MCP-Banner.png)

## Model Context Protocol (MCP) Server for BloodHound

BloodHound-MCP is a powerful integration that brings the capabilities of Model Context Procotol (MCP) Server to BloodHound, the industry-standard tool for Active Directory security analysis. This integration allows you to analyze BloodHound data using natural language, making complex Active Directory attack path analysis accessible to everyone.

> 🥇 **First-Ever BloodHound AI Integration!**  
> This is the first integration that connects BloodHound with AI through MCP, [originally announced here](https://www.linkedin.com/posts/mor-david-cyber_bloodhound-ai-cybersec-activity-7310921541213470721-N390).

## 🔍 What is BloodHound-MCP?

BloodHound-MCP combines the power of:
- **BloodHound**: Industry-standard tool for visualizing and analyzing Active Directory attack paths
- **Model Context Protocol (MCP)**: An open protocol for creating custom AI tools, compatible with various AI models
- **Neo4j**: Graph database used by BloodHound to store AD relationship data

With over 75 specialized tools based on the original BloodHound CE Cypher queries, BloodHound-MCP allows security professionals to:
- Query BloodHound data using natural language
- Discover complex attack paths in Active Directory environments
- Assess Active Directory security posture more efficiently
- Generate detailed security reports for stakeholders

## 📱 Community

Join our Telegram channel for updates, tips, and discussion:
- **Telegram**: [root_sec](https://t.me/root_sec)

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=MorDavid/BloodHound-MCP-AI&type=Date)](https://www.star-history.com/#MorDavid/BloodHound-MCP-AI&Date)

## ✨ Features

- **Natural Language Interface**: Query BloodHound data using plain English
- **Comprehensive Analysis Categories**:
  - Domain structure mapping
  - Privilege escalation paths
  - Kerberos security issues (Kerberoasting, AS-REP Roasting)
  - Certificate services vulnerabilities
  - Active Directory hygiene assessment
  - NTLM relay attack vectors
  - Delegation abuse opportunities
  - And much more!

## 📋 Prerequisites

- BloodHound 4.x+ with data collected from an Active Directory environment
- Neo4j database with BloodHound data loaded
- Python 3.8 or higher
- MCP Client

## 🔧 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/MCP-BloodHound.git
   cd MCP-BloodHound
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Configure the MCP Server
    ```bash
    "mcpServers": {
        "BloodHound-MCP": {
            "command": "python",
            "args": [
                "<Your_Path>\\BloodHound-MCP.py"
            ],
            "env": {
                "BLOODHOUND_URI": "bolt://localhost:7687",
                "BLOODHOUND_USERNAME": "neo4j",
                "BLOODHOUND_PASSWORD": "bloodhoundcommunityedition"
            }
        }
    }
   ```
## 🚀 Usage

Example queries you can ask through the MCP:

- "Show me all paths from kerberoastable users to Domain Admins"
- "Find computers where Domain Users have local admin rights"
- "Identify Domain Controllers vulnerable to NTLM relay attacks"
- "Map all Active Directory certificate services vulnerabilities"
- "Generate a comprehensive security report for my domain"
- "Find inactive privileged accounts"
- "Show me attack paths to high-value targets"

## 🔐 Security Considerations

This tool is designed for legitimate security assessment purposes. Always:
- Obtain proper authorization before analyzing any Active Directory environment
- Handle BloodHound data as sensitive information
- Follow responsible disclosure practices for any vulnerabilities discovered

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- The BloodHound team for creating an amazing Active Directory security tool
- The security community for continuously advancing AD security practices

---

*Note: This is not an official Anthropic product. BloodHound-MCP is a community-driven integration between BloodHound and MCP.* 
