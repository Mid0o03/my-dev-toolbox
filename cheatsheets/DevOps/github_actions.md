# GitHub Actions (CI/CD)

GitHub Actions allow you to automate your workflow directly in your repository.

## Workflow File Structure
Location: `.github/workflows/main.yml`

```yaml
name: Node.js CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3
    - name: Use Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18.x'
    - run: npm ci
    - run: npm run build
    - run: npm test
```

## Common Triggers
- `on: [push, pull_request]`
- `on: schedule`: Cron jobs.
- `on: workflow_dispatch`: Manual trigger.

## Matrix Builds
Test across multiple OS or versions.
```yaml
strategy:
  matrix:
    node-version: [14.x, 16.x, 18.x]
```

## Secrets
Access sensitive data securely in your actions.
- Access via: `${{ secrets.MY_SECRET_NAME }}`
- Set in: `Settings -> Secrets and variables -> Actions`
