A lightweight tool for building campaign URLs with UTM tracking parameters. 
The app uses HTML, CSS, and vanilla JavaScript and runs directly in a modern web browser.

Quick start
  1. Download utm-builder.html or download the ZIP package and extract it.
  2. If you downloaded the ZIP, extract its contents to a folder on your computer.
  3. Double-click utm-builder.html to open it in your default browser.
  4. You can also right-click it and choose Open with to select Chrome, Edge, Firefox, or another modern browser.
  5. Enter the full destination URL, including https://.
  6. Select a Campaign Source and Campaign Medium, then enter the Campaign Name. Campaign Content and Campaign Term are optional.
  7. Select Build UTM URL.
  8. Select Copy URL to copy the result.

No installation, account, web server, or build process is required.

Field reference
- Destination URL — The page visitors should land on. Enter a complete HTTPS URL, for example https://www.example.com/events.
- Campaign Source (utm_source) — Choose the source from the dropdown.
- Campaign Medium (utm_medium) — Choose the channel type from the dropdown.
- Campaign Name (utm_campaign) — Enter a descriptive campaign name; use dashes between words.
- Campaign Content (utm_content) — Optional creative details, such as creative name, size, or format. Use dashes between words.
- Campaign Term (utm_term) — Optional keyword or placement detail, such as {keyword}, newsfeed, or story.

URL behavior
- UTM parameter names and values are converted to lowercase when the URL is generated.
- Existing UTM parameters are removed before the new configured values are added, avoiding duplicate UTM parameters when rebuilding a URL.
- Other parts of the destination URL, including its path and non-UTM query parameters, are preserved.
- URL values are encoded using the browser's URL APIs.

Customize the tool
Open utm-builder.html in a code editor such as VS Code or Notepad. Find the UTM_CONFIG object in the JavaScript section.
- Change the options array under utm_source or utm_medium to update dropdown choices.
- Update label, description, required, type, and placeholder to change field labels and behavior.
- Save the file, then refresh the browser tab to load the changes.

Troubleshooting
- The file opens as text:
  - Solution: Right-click utm-builder.html, choose Open with, and select your browser.
- The destination URL is rejected:
  - Solution: Enter a complete URL beginning with https:// and check that the hostname is valid.
- Copying does not work:
  - Solution: Build the URL first. If the browser blocks clipboard access, select the generated URL and copy it manually.
- Configuration changes are not visible:
  - Solution: Save the HTML file and refresh the browser tab.
Privacy and limitations
The tool is designed to run locally in your browser and does not need to send campaign values to a server. It checks URL formatting and configured validation rules, but it does not verify that the destination page exists or is reachable.
