# Automated Web Security Scanner Using Python

**Student:** Sindhu T Byali  
**Project type:** Internship project

## Project description
This project is a lightweight Python-based web security configuration checker. It reviews an authorized public website's HTTP response for HTTPS usage, common security headers, basic CORS response behavior, and cookie security attributes. It displays findings and exports them to CSV.

This is an educational configuration checker, not a complete penetration-testing tool. A warning is not proof of an exploitable vulnerability, and a passing result does not guarantee that a website is secure.

## Technologies used
- Python
- Jupyter Notebook
- Requests
- Pandas
- IPython display

## Dataset / test data
This project does **not** require a machine-learning dataset. Its input is a website URL that the user owns or has explicit permission to assess. For a safe demonstration, use your own website, a dedicated test deployment, or a lab target approved by your internship supervisor. Do not scan third-party websites without authorization.

## Project files
- `SindhuTByali_AutomatedWebSecurityScanner.ipynb` — complete notebook code and execution instructions.
- `requirements.txt` — Python dependencies.
- `SindhuTByali_ProjectReport.docx` — project report.

## Setup instructions
1. Install Python 3.10 or newer.
2. Open a terminal in the project folder.
3. (Recommended) Create and activate a virtual environment.

   **Windows**
   ```powershell
   py -m venv .venv
   .venv\Scripts\activate
   ```

   **macOS/Linux**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

4. Install dependencies:
   ```bash
   python -m pip install -r requirements.txt
   ```
5. Start Jupyter:
   ```bash
   jupyter notebook
   ```
6. Open `SindhuTByali_AutomatedWebSecurityScanner.ipynb` and run cells from top to bottom.
7. When prompted, enter an authorized public website URL. Review any redirect destination before scanning it separately.
8. The notebook can export findings to a CSV file in the current working directory.

## Checks performed
- HTTP vs HTTPS URL scheme
- HTTP response status
- Presence of common security headers:
  - Strict-Transport-Security
  - Content-Security-Policy
  - X-Content-Type-Options
  - X-Frame-Options
  - Referrer-Policy
  - Permissions-Policy
- Basic CORS response behavior
- Sampled Set-Cookie security attributes: Secure, HttpOnly, SameSite
- CSV findings export

## Limitations
- The scanner does not crawl a website or test every route.
- CORS analysis is a basic response check, not a full policy audit.
- Security-header presence does not guarantee a correctly configured policy.
- The scanner does not exploit vulnerabilities, bypass authentication, or test application logic.
- DNS and network conditions can change; the URL/IP check is best-effort and is not a substitute for authorization or network controls.

## Responsible use
Only scan systems you own or have written permission to assess. Follow the scope and rules of engagement provided by the system owner or internship supervisor.
