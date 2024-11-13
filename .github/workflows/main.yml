name: Example workflow for Python using Snyk 
on: pull_request
jobs:
  security:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: Run Snyk to check for vulnerabilities
      uses: snyk/actions/python@master
      env:
        COMMAND: "python setup.py install"
        SNYK_TOKEN: ${{ secrets.SNYK_TOKEN }}
      with:
        args: --file=setup.py
