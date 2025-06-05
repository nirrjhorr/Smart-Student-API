```markdown
# 🎓 Smart Student API – Automated Testing

A lightweight project for automated testing of the Smart Student API using Postman and Newman. The collection runs 50 iterations with a 200ms delay between requests, generating detailed HTML reports.

## 📁 Project Structure

```

├── Smart-Student-API.postman\_collection.json
├── Smart-Student-API.postman\_environment.json
└── reports/

````

- **Collection**: Contains the API test cases.
- **Environment**: Stores variables for environment-specific configurations.
- **Reports**: Contains CLI and HTML test reports.

## 🚀 Getting Started

### Prerequisites

Ensure Node.js is installed, then install Newman and the HTML Extra reporter:

```bash
npm install -g newman newman-reporter-htmlextra
````

### Run the Tests

```bash
newman run Smart-Student-API.postman_collection.json \
  -e Smart-Student-API.postman_environment.json \
  --iteration-count 50 \
  --delay-request 200 \
  -r cli,html,htmlextra \
  --reporter-html-export reports/basic-report.html \
  --reporter-htmlextra-export reports/detailed-report.html
```

## 📊 Output

* **CLI Summary**: Shows pass/fail stats in the terminal.
* **Basic HTML Report**: Simple visual overview.
* **Detailed HTML Report**: Advanced, styled report saved in `reports/`.

---

Feel free to fork, clone, or adapt for your own API projects!

```
