# Liquibase Init Properties Action

⚠️ **VERSION SUPPORT NOTICE**: This action supports Liquibase versions up to 4.x. For Liquibase 5.0+ features, please migrate to [`liquibase/setup-liquibase`](https://github.com/liquibase/setup-liquibase).

## Migration Guide

### Current Approach (Supports Liquibase 4.x)
```yaml
- uses: liquibase-github-actions/init-properties@v4.33.0
  with:
    # your parameters here
```

### Recommended for Liquibase 5.0+ Features
```yaml
- uses: liquibase/setup-liquibase@v1
  with:
    version: '5.0.0'  # Supports latest features
    edition: 'oss'
- run: liquibase init-properties # add your parameters as CLI flags
```

---

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
