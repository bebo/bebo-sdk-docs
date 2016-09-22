# bebo-sdk-docs

Hosted at http://bebo-sdk.readthedocs.io

To setup:

1. Clone repo
2. `$ cd bebo-sdk-docs`
3. `$ virtualenv env` to make a Python virtual environment (`pip install virtualenv` if you don't have this command)
4. `$ source env/bin/activate` to activate your virtual environment

To edit locally:

1. `$ cd docs` 
1. Create/edit any .rst file
2. `$ make html` inside docs to build new HTML files
3. Open newly-built docs/_build/html/ file in a browser

To publish to RTD:

1. Simply commit and RTD will auto-build
