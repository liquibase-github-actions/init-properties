# Liquibase Init Properties Action
Official GitHub Action to run Liquibase Init Properties in your GitHub Action Workflow. For more information on how init properties works visit the [Official Liquibase Documentation](https://docs.liquibase.com/commands/home.html).
## Init Properties
[PRO] Generate a summary of all Liquibase properties available.
## Usage
```yaml
steps:
- uses: actions/checkout@v3
- uses: liquibase-github-actions/init-properties@v4.33.0
  with:
    # Enable or disable reporting.
    # bool
    # Optional
    reportEnabled: ""

    # The path to the directory to generate the report.
    # string
    # Optional
    reportPath: ""

```

### Secrets
It is a good practice to protect your database credentials with [GitHub Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets)

## Optional Liquibase Global Inputs
The liquibase init properties action accepts all valid liquibase global options as optional parameters. A full list is available in the official [Liquibase Documentation](https://docs.liquibase.com/parameters/command-parameters.html).

### Example
```yaml
steps:
  - uses: actions/checkout@v3
  - uses: liquibase-github-actions/init-properties@v4.33.0
    with:
      headless: true
      licenseKey: ${{ secrets.LIQUIBASE_LICENSE_KEY }}
      logLevel: INFO
```

## Feedback and Issues
This action is automatically generated. Please submit all feedback and issues with the [generator repository](https://github.com/liquibase/github-action-generator/issues).
