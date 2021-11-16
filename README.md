# nyc-social-services-data

This repository contains the data on verified locations for NYC City-Funded Social Service Contracts (obtained from the [open data portal](https://data.cityofnewyork.us/browse?Data-Collection_Data-Collection=Verified+Locations+for+NYC+City-Funded+Social+Service+Contracts) on Nov. 15, 2021).

The data has been added to a sqlite3 database [nyc.db](data/nyc.db) for its exploration using [datasette](https://datasette.io/).

## Run this locally

First, clone this repository. In your terminal,
```shell
# using GitHub's CLI tool (`brew install gh`)
gh repo clone we-are-alluma/nyc-social-services-data

# OR using git
git clone https://github.com/we-are-alluma/nyc-social-services-data
```

Go to the directory (`cd nyc-social-services-data`)

Then create a new python virtual environment. If you are familiar and have a preference, you can use whatever virtual environment tool you would like. We suggest using the python standard library's `venv`

```shell
# Use python 3
python3 -m venv .venv
```

Next step, activate the environment
```shell
# in Linux/MacOS
source .venv/bin/activate

# in Windows
.\venv\Scripts\activate
```

and install the `requirements.txt`
```shell
python3 -m pip install -r requirements.txt
```

This will provide you all the tools needed to manipulate the data but, more importantly, it will also install datasette which is the tool we will be using to explore the data. 

## Launch datasette
Now that you have all the packages installed you can run
```shell
datasette data/nyc.db
```
from the parent directory and visit your http://localhost:8001 to explore the data.

