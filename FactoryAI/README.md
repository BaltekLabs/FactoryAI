# MyProject

A generated IBM Cloud application

[![](https://img.shields.io/badge/bluemix-powered-blue.svg)](https://bluemix.net)

## Run locally as Flask application
```bash
pip install -r requirements.txt
export FLASK_APP=server
gunicorn -b 0.0.0.0:8080 server:app
```

## To test the Flask Application
```bash
export PYTHONPATH=$(pwd)
python tests/<resource>_test
```
For example, where a resource person is generated, then within server/routes a _**person.py**_ implementation will be generated and a corresponding testcase _**person_tests.py**_ will be generated within the tests directory.

To test all endpoints, run
```bash
export PYTHONPATH=$(pwd)
for test in tests/*_tests.py; do python $test; done
```
