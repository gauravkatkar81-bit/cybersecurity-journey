# Module 6: How The Web Works
**Path:** TryHackMe - Pre-Security
**Date Completed:** 29 October 2026
**Focus:** DNS in Details, HTTP in Details, How Websites Work, Putting It All Together

---

## 📌 1. Key Concepts Learned
- **DNS in Details:** DNS (Domain Name System), Domain Hierarchy (Root, Top-Level Domain like `.com` or `.in`, Second-Level Domain like `tryhackme` or `google`, and Subdomains), DNS Record Types, and what happens when you make a DNS request.
- **HTTP in Details:** HTTP (HyperText Transfer Protocol), Requests & Responses, HTTP Methods (`GET`, `POST`, `PUT`, `DELETE`), HTTP Status Codes, Request/Response Headers, and Cookies.
- **How Websites Work:** Front-end (client-side), Back-end (server-side), HTML (HyperText Markup Language), JavaScript (JS), Sensitive Data Exposure, and HTML Injection.
- **Putting It All Together:** Load Balancers, CDN (Content Delivery Network), Databases, WAF (Web Application Firewall), Web Servers, Virtual Hosts, Static & Dynamic Content, and Backend Languages.

---

## 🧪 2. Hands-On Lab Walkthroughs & Exercises

### Lab 1: DNS & `nslookup` Exploration
- **Tasks:** Use query tools to gather server and domain information.
- **Action:**
  1. Used the `nslookup` command-line tool to query domain records for specific websites.
  2. Investigated different DNS record types such as **A records** (IPv4 addresses), **AAAA records** (IPv6 addresses), and **CNAME records** (canonical names/aliases).
  3. Analyzed how name resolution maps human-readable domain names to machine-readable IP addresses.
- **Key Takeaway:** Understanding how to query DNS records helps map infrastructure targets during reconnaissance.

---

### Lab 2: HTTP Methods & Request Inspection
- **Tasks:** Test and examine HTTP methods (`GET`, `POST`, `PUT`) and inspect server responses.
- **Action:**
  1. Experimented with different HTTP methods to see how data is sent and requested from a web server.
  2. Answered practical quiz questions by inspecting request payloads, server IP addresses, user credentials, and header details.
- **Key Takeaway:** Knowing how web methods handle data transmission is essential for identifying web application functionality and flaws.

---

### Lab 3: HTML Injection & Request Flow Ordering
- **Tasks:** Practice basic HTML injection in an input box and review the complete end-to-end web request lifecycle.
- **Action:**
  1. Tested input fields by injecting basic HTML queries to see how unvalidated input reflects on the page.
  2. Completed a final workflow exercise where components were arranged in correct order from start to end (tracing the request path through DNS, Load Balancers, Web Servers, and Databases).
- **Key Takeaway:** Seeing how unvalidated input causes HTML injection, and reviewing how all web components interact together in production.

---

## 🛠️ Commands & Tools Summary
| Tool / Concept | Function |
| :--- | :--- |
| **`nslookup`** | Command-line tool for querying DNS records (A, AAAA, CNAME) |
| **HTTP Methods** | Verbs (`GET`, `POST`, `PUT`, `DELETE`) used to interact with web servers |
| **HTML Injection** | Vulnerability occurring when untrusted user input is rendered directly by the browser |
| **WAF / CDN** | Security filtering and content caching layers protecting modern web architectures |
