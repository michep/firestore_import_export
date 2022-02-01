# firestore_export_import
Simple python script that performs export or import of data in YAML format with Firebase Firestore.

    usage: firestore_export_import.py [-h] [-e] [-n] [-p PATH] service_file data_file
    positional arguments:
    service_file          google cloud service account .json file
    data_file             yaml data file for export or import
    options:
    -h, --help            show this help message and exit
    -e, --export          perform export, if not present - import will be performed
    -n, --noid            do not export document ids
    -p PATH, --path PATH  initial path to start export or import into

Example of yaml file for import is in `example.yaml`

Main differences from other import tools are:
- if `_id` attribute of record of document is missiong - ID will be autogenerated
- with `$query` keyword it is possible to query data in Firestore to get values for attribuites
