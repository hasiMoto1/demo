name: Codacy Security Scan

on:

push:

branches: [ \"master\", \"main\" ]

pull_request:

branches: [ \"master\", \"main\" ]

jobs:

codacy-security-scan:

name: Codacy Security Scan

runs-on: ubuntu-latest

steps:

- name: Checkout code

uses: actions/checkout@main

- name: Run Codacy Analysis CLI

uses: codacy/codacy-analysis-cli-action@master

with:

api-token: \${{ secrets.CODACYAPITOKEN }}

output: results.sarif

format: sarif

gh-code-scanning-compat: true

max-allowed-issues: 2147483647

- name: Upload SARIF results file

uses: github/codeql-action/upload-sarif@main

with:

sarif_file: results.sarif
