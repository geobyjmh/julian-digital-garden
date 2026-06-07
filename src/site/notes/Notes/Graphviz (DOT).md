---
{"dg-publish":true,"permalink":"/notes/graphviz-dot/","dg-note-properties":{}}
---

- link: [[Notes/Diagrams-as-Code (DaC)\|Diagrams-as-Code (DaC)]]

**DOT** is a plain-text graph description language used to define and visualize structured networks, such as flowcharts, trees, and network topologies. It allows users to describe nodes (the data points) and edges (the connections between them) using a simple, human-readable syntax, which is then compiled into visual diagrams by graph layout tools like **Graphviz**. Instead of manually drawing shapes and lines, you write the relationships in code, and the software automatically calculates the best way to position the elements cleanly. It is widely used in software development and data analysis for automated documentation, mapping dependencies, and rendering complex data structures.

# Tools

- **Online Tool**: [Webgraphviz](http://www.webgraphviz.com/?source=techstories.org) 

# Dot Examples
## Example 1
```
graph graphname {
    a -- b -- c;
    b -- d;
}
```
![Pasted image 20260607094137.png](/img/user/Images/Pasted%20image%2020260607094137.png)

# Reference
Wikipedia (2026) _DOT (graph description language)_. Available at: [https://en.wikipedia.org/wiki/DOT_(graph_description_language)](https://en.wikipedia.org/wiki/DOT_\(graph_description_language\)) (Accessed: 7 June 2026).

Last Updated: 07/06/26