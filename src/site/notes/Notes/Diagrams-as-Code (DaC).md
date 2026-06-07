---
{"dg-publish":true,"permalink":"/notes/diagrams-as-code-da-c/","dg-note-properties":{}}
---


- Link: [[Notes\|Notes]]

**Diagrams-as-Code (DaC)**—also known as **Text-to-Diagram**—is a method of creating visual charts, technical architectures, and workflow maps by writing structured plain text instead of using manual drag-and-drop graphic interfaces.

Instead of spending time dragging shapes, drawing lines, and manually aligning layout boxes, you write out the relationships using a simple syntax ruleset (like `User --> Database`). A background rendering engine automatically takes that text and computes the layout, spacing, and styling into a pixel-perfect visual graphic. Because these diagrams are saved as plain text files, they can be easily tracked using version control systems like Git, edited directly within markdown note-taking tools, and updated without risk of breaking old file formats.

### Core Ecosystem Examples

- **Mermaid.js:** Optimized for web portability and markdown integration. It works out of the box inside modern documentation platforms like Obsidian, Notion, and GitHub without requiring any external software installation.
    
- **PlantUML:** The long-standing enterprise standard for software engineering. It excels at generating strict structural Unified Modeling Language (UML) layouts, complex database schemas, and deep multi-step sequence flows.
    
- **D2:** A modern, minimal, high-performance language designed specifically as a cleaner alternative to older tools. It features highly intuitive layout syntax and auto-generates beautifully polished modern vector graphics.
    
- **Diagrams (Python):** A developer-focused programming framework that lets you map out live cloud architecture systems (like AWS, Azure, Google Cloud, and Kubernetes) using native object loops directly inside Python scripts.
    
- **[[Notes/Graphviz (DOT)\|Graphviz (DOT)]]:** The foundation framework of the entire DaC category. It uses a mathematical layout script language to automatically map complex data networks and massive collections of interconnected informational nodes.

Last Updated: 07/06/26