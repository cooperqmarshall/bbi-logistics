# Logistics
Operational automation and dashboard updates for Brotman Baty Institute Logistics

### Order script documentation:
- [Delivery Express](orders/DE_ORDER_README.md)
- [USPS](orders/USPS_ORDER_README.md)

### [Dashboards documentation](update_dashboards/DASHBOARD_README.md)

## Usage
```
python3 orders/delivery_express_order.py
```

## Setup
Clone the logistics repo
```
cd ~/
git clone https://github.com/cooperqmarshall/logistics.git
cd logistics
```

Install required packages using:
```
python3 -mpip install -r requirements.txt
```

## Configure REDCap API Token environment variables
> You need to do these steps once per REDCap project.

```
cd ~/logistics/.env/
```

You'll need to copy your REDCap API token from each project and create a new file containing only the token.
We create file names using this pattern: `REDCAP_API_TOKEN_{REDCAP API URL}_{PROJECT_ID}`.
Here's an example of creating a new environment variable for the SCAN IRB English project (project ID 22461) with the text editor `nano`:
```
nano redcap/REDCAP_API_TOKEN_redcap.iths.org_22461
```
HCT now uses the url `hct.redcap.rit.uw.edu`

Note that you are literally typing the string `REDCAP_API_TOKEN` here.
Once you're inside the file with `nano`, paste your actual token copied from REDCap.
Then, press `CTRL+X` to exit.
Remember to save your work!
(Press `Y` then hit `Enter` to confirm the original save location.)

Repeat this process for every SCAN REDCap project you need orders from.

## Configure Google API Credentials
> Only needed for dashboard updates
To connect to the google sheets API, contact the admin of this repo to get the credentaials.

Create a file in the .config directory.
```
nano .config/logistics-db-1615935272839-a608db2dc31d
```
Paste the contents of what the admin sends in this file.

Then, press `CTRL+X` to exit.
Remember to save your work!
(Press `Y` then hit `Enter` to confirm the original save location.)
