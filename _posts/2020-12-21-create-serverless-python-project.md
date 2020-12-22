---
title: "Create Serverless Python Project"
date: 2020-12-21T22:30:00-06:00
categories:
  - Serverless
tags:
  - Serverless
  - Python
---

1. Create the serverless project
```bash
serverless create --template aws-python3 --name service_name --path given_path_folder
```

2. Create the virtual environment
```bash
virtualenv --python=python3 venv
source venv/bin/activate
```

3. Install serverless package for deployment
```bash
npm init
npm install --save serverless-python-requirements
```

    Add the configure to the serverless.yml
    ```
    plugins:
      - serverless-python-requirements

    custom:
      pythonRequirements:
        dockerizePip: non-linux
    ```