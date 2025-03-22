# Vulnex: Resource Scanner Bookmarklet

A single-line JavaScript bookmarklet designed for security researchers, bug bounty hunters, and penetration testers. This tool scans loaded web resources, performs deep crawling of linked pages, and integrates advanced vulnerability testing modules—including parameter fuzzing for SQL injection, XSS, command injection, SSRF, directory traversal, and more. It also supports automated exploitation, authenticated scans with custom headers, and allows users to import custom payloads.

## Features

- **Resource Scanning**:  
  Scans all resources loaded on a page using browser performance entries. Extracts and normalizes relative paths to absolute URLs.

- **Deep Scan**:  
  Recursively crawls linked pages (up to a configurable depth) to discover hidden endpoints and directories.

- **Basic Vulnerability Testing**:  
  Checks endpoints using HEAD requests and color-codes responses for quick identification of potential issues.

- **Advanced Vulnerability Testing**:  
  Implements parameter fuzzing with a broad payload library for SQL injection, XSS, command injection, SSRF, and directory traversal. Uses response analysis heuristics (comparing content length differences) to flag vulnerabilities without disturbing the target client's traffic.

- **Automated Exploitation**:  
  Attempts controlled exploitation on confirmed vulnerabilities based on the testing results.

- **Authentication & Session Testing**:  
  Supports authenticated scans by allowing custom HTTP headers (including session cookies and CSRF tokens).

- **Payload Customization**:  
  Users can import their own JSON payload lists to extend or override default payloads.

- **User-Friendly UI**:  
  A dynamic overlay panel with progress bars, result lists, error logs, and control buttons to trigger each functionality (e.g., Deep Scan, Vulnerability Check, Advanced Vulnerability Testing, Auto Exploit).

## Installation & Usage

1. **Create a Bookmark**:  
   Copy the single-line JavaScript code provided in the repository and create a new bookmark in your browser. Paste the code into the bookmark's URL field.

2. **Activate the Bookmarklet**:  
   Navigate to any website and click the bookmark to launch the overlay panel.

3. **Perform Scans**:  
   - The tool will start by scanning loaded resources.
   - Use the **Deep Scan** button to crawl linked pages recursively.
   - Use **Vuln Check** for basic vulnerability testing.
   - Use **Adv Vuln Test** for advanced vulnerability testing with payload fuzzing.
   - Use **Auto Exploit** to attempt controlled exploitation.
   - Use **Import Payloads** to load custom payload lists.
   - Use **Set Auth** to define custom headers for authenticated scans.

## Disclaimer

**WARNING**: Use this tool responsibly and only on websites you are authorized to test. The creator is not responsible for any misuse or illegal activities. Always obtain proper permission before performing any security testing.

## Contributing

Contributions, improvements, and feature suggestions are welcome. Feel free to fork the repository and submit pull requests.

Happy Hunting!!
