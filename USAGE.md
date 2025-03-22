# Vulnex Usage Guide

Vulnex is a bookmarklet tool for security researchers and bug bounty hunters. It scans loaded web resources, performs deep crawling, and integrates advanced vulnerability testing modules.

## Installation

1. **Create a New Bookmark:**
   - Open your browser’s bookmarks bar.
   - Right-click the bookmarks bar and choose **"Add Page"** or **"Add Bookmark"**.
   - Name the bookmark **Vulnex**.
   - In the URL field, paste the entire one-line JavaScript code provided in the repository. The code starts with `javascript:(async function(){...})();`.
   - Save the bookmark.

## Usage

1. **Navigate to a Target Website:**
   - Open any website where you have explicit permission to test.

2. **Activate Vulnex:**
   - Click the **Vulnex** bookmark in your bookmarks bar. This will execute the script on the current page.

3. **Using the Interface:**
   - An overlay panel will appear with several options:
     - **Resource Scanner:** Scans all loaded resources and extracts unique endpoints.
     - **Deep Scan:** Recursively crawls linked pages (up to a depth of 3) to discover hidden endpoints.
     - **Vuln Check:** Performs basic vulnerability testing using HEAD requests.
     - **Adv Vuln Test:** Executes advanced vulnerability testing with parameter fuzzing (SQL injection, XSS, command injection, SSRF, etc.). It uses response analysis heuristics to flag potential vulnerabilities without disturbing client traffic.
     - **Auto Exploit:** Attempts controlled exploitation on confirmed vulnerable endpoints.
     - **Import Payloads:** Allows you to import custom payload lists in JSON format.
     - **Set Auth:** Lets you define custom HTTP headers (e.g., for session cookies or CSRF tokens) for authenticated scans.
     - **Copy:** Copies the results to the clipboard.
     - **Minimize/Close:** Toggle the visibility or close the overlay.

4. **Interpreting Results:**
   - Discovered endpoints are listed in the overlay. Click any endpoint to open it in a new tab.
   - Vulnerability tests will update the endpoints with status codes and vulnerability flags (color-coded for easy identification).
   - Any errors during scanning or testing will be logged in the error section.

## Disclaimer

**WARNING:** Use Vulnex only on websites where you have explicit authorization to perform security tests. The creators are not responsible for any misuse or unauthorized testing.

## Contributing

Contributions and improvements are welcome. Please fork the repository and submit pull requests or open issues with suggestions.

Happy Vulnerability Hunting with Vulnex!
