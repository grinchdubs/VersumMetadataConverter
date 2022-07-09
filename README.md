# VersumMetadataConverter

Here you have a series of files to help create metadata for a manual mint on Versum NFT Marketplace

## JSON
The *metadataMASTER.json* shouldn't be modified without care. It contains the format and data needed to create a working JSON file with the metadata information that versum is expecting.

The *metadata.json* file is just a copy of *metadataMASTER.json* and will be the final file you will be using for your mint once the data from your csv has been entered in.

## CSV
The *metadataToJson.csv* file is where you will be entering in data needed by the json file. You can edit this in any text/table editor. Once you fill out the relevant information you will be ready to run the conversion script.

## Conversion
The *Replace-InFilesUsingList.ps1* is a Powershell script. From Powershell, change directories to the folder where all these files are located and run it using the following command:

```
.\Replace-InFilesUsingList.ps1 -List "metadataToJson.csv" -Files "metadata.json"
```

Once this runs, open *metadata.json* and you will see it contains the information from the csv file.

### Issues
If youh have any issues with permissions in Powershell please follow the instructions from the link below

https://www.mssqltips.com/sqlservertip/2702/setting-the-powershell-execution-policy/

