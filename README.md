# iotcore-heartrate

This project contains the code necessary to setup either 
(1) a Raspberry Pi with a heart rate sensor or 
(2) a Ubuntu Machine with a data simulation script in order to demonstrate how Google Cloud IoT Core works. 

The full instructions are contained this Codelab https://codelabs.developers.google.com/codelabs/iotcore-heartrate#0

Use Python2.7 to run the scripts given here.
You neeed to probably set up the python-dev tools and also python-jwt for the same.

## Data Simulation Quickstart


        sudo apt-get update
        sudo apt-get install git
        git clone https://github.com/vadi84/GCPIoTDemo
        cd GCPIoTDemo
        chmod +x initialsoftware.sh
        ./initialsoftware.sh
        chmod +x generate_keys.sh
        ./generate_keys.sh
        cd ../.ssh
        pwd
        exit


        python2 heartrateSimulator.py --registry_id=heartrate --project_id=PROJECT_ID --device_id=myVM --private_key_file=../.ssh/ec_private.pem
        [Change the cloud region according to your setup in the script or in the command line]
        
   
Go to BigQuery, query the data and export it to Google Sheets.
Plot charts and see the data.

Stop all the jobs created in the GCP.

