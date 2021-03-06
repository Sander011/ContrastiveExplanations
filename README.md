# Contrastive explantions using local foil trees

The project is divided in two parts, one for running the metrics of the local foil trees and one for the interactive user interface.

_Note: all version listed below are what we used for the experiments, higher versions might behave differently_

**Front-end**
_Requirements_:

- Node v12.4.0
- Npm v6.9.0

To run the front-end go into the root directory and enter the following commands:

    npm install
    npm run start

This launches the front-end server on localhost:3000 by default. In order to make it work the back-end server should also be running.

**Back-end**
_Requirements_

- Python v3.7.7
- Pip v20.0.2

To run the backend go into the root directory and enter the following commands:

    pip install -r requirements.txt
    python manage.py migrate
    python manage.py runserver

This should launch the back-end server on localhost:8000 by default. The front-end seen on localhost:8000 is the one generated by running `npm run build`. Immediate changes to the front-end can be seen on localhost:3000.

**Metrics**
In order to compute the metrics as seen in the paper, run the following command from the root directory:

    python compute-metrics.py
