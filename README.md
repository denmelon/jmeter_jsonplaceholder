
# 🧪 JMeter Performance Tests — JSONPlaceholder

This project contains performance tests for [JSONPlaceholder](https://jsonplaceholder.typicode.com) created with Apache JMeter.

## 📁 Project Structure

```
performance-tests/
├── jsonplaceholder_test.jmx       # JMeter test plan
├── posts.csv                      # Optional CSV file for parameterization
└── .github/
    └── workflows/
        └── jmeter.yml             # GitHub Actions workflow
```

## ✅ Covered Scenario

- `GET /posts/{id}` with multiple IDs from a CSV file
- Configurable threads, ramp-up, loop count
- Constant Timer to simulate think-time

## 🧪 Run Locally

1. Make sure JMeter is installed.
2. Use the following command:

```bash
jmeter -n -t jsonplaceholder_test.jmx -l results.jtl -e -o report
```

- `-n`: non-GUI mode
- `-t`: test plan file
- `-l`: JTL results file
- `-e`: generate HTML report
- `-o`: output report folder

3. Open `report/index.html` in a browser

## ⚙️ Run via GitHub Actions

This project includes a CI workflow that automatically runs the test on every push to the `main` branch.

- Runs JMeter on a virtual Ubuntu runner
- Generates a report and uploads it as an artifact

## 🚀 Report Example

After GitHub workflow finishes, you’ll find a downloadable artifact with the full HTML report.

## 📦 Requirements

- Apache JMeter 5.6.3 or later
- Java 11+ (locally)
- GitHub repository with Actions enabled

---

📁 *This project is part of a QA portfolio to demonstrate skills in performance testing with JMeter.*
