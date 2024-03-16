# my new project
[![Build Status](https://jenkins.services.ai4os.eu/buildStatus/icon?job=AI4OS-hub/my-new-project/test)](https://jenkins.services.ai4os.eu/job/AI4OS-hub/job/my-new-project/job/main/)

my project here

To launch it, first install the package then run [deepaas](https://github.com/ai4os/DEEPaaS):
```bash
git clone https://github.com/ai4os-hub/my-new-project
cd my-new-project
pip install -e .
deepaas-run --listen-ip 0.0.0.0
```

## Project structure
```
│
├── Dockerfile             <- Describes main steps on integration of DEEPaaS API and
│                             my_new_project application in one Docker image
│
├── Jenkinsfile            <- Describes basic Jenkins CI/CD pipeline (see .sqa/)
│
├── LICENSE                <- License file
│
├── README.md              <- The top-level README for developers using this project.
│
├── .sqa/                  <- CI/CD configuration files
│
├── my_new_project    <- Source code for use in this project.
│   │
│   ├── __init__.py        <- Makes my_new_project a Python module
│   │
│   ├── api.py             <- Main script for the integration with DEEPaaS API
│   │
│   └── misc.py            <- Misc functions that were helpful accross projects
│
├── data/                  <- Folder to store the data
│
├── models/                <- Folder to store models
│   
├── tests/                 <- Scripts to perfrom code testing
|
├── metadata.json          <- Defines information propagated to the AI4OS Hub
│
├── requirements.txt       <- The requirements file for reproducing the analysis environment, e.g.
│                             generated with `pip freeze > requirements.txt`
├── requirements-test.txt  <- The requirements file for running code tests (see tests/ directory)
│
└── setup.py, setup.cfg    <- makes project pip installable (pip install -e .) so
                              my_new_project can be imported
```
