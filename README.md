
[![Screenshot](https://tridentnets.com/banner.png)](https://tridentnets.com/)
# Firebase-Commands

This is a collection of Firebase Commands for easy reference.

Auth_Export Command :

Step 1 : npm install -g firebase-tools

Step 2: firebase login

Command: 

firebase auth:export [YourFileName.json] --format=json --project=[Your Project Id]

Auth_Import Command :

Step 1 : Need to get  Password hash parameters  before doing auth Import.

How to get Password hash parameters ?

You click on Authentication -> Users and then click on the three vertical dots next to the reload button and a popup menu will show up with a single menu item: "Password hash parameters".

Sample  Password hash parameters  : 

hash_config {
  algorithm: SCRYPT, // Exported_Auth_Algorithm
  base64_signer_key: 8NP0gPNCGatxKabgOGdvb7rIfUA2lEg==, //Exported_Auth_base64_singer_key
  base64_salt_separator: Bw==, //Exported_Auth_base64_salt_separator
  rounds: 8, //Exported_Auth_Rounds
  mem_cost: 14, //Exported_Auth_Mem_Cost
}

Command: 

firebase auth:import [YourFileName.json ]--hash-algo=[Exported_Auth_Algorithm] --rounds=[Exported_Auth_Rounds]  --mem-cost=[Exported_Auth_Mem_Cost]  --hash-key=l[Exported_Auth_base64_singer_key] --salt-separator=[Exported_Auth_base64_salt_separator] --project=[Your Project Id]


Export  Stoarge Image  From google cloud Bucket:

Step 1 : Shell & could SDK download (Download Link - https://cloud.google.com/sdk/docs/)

Step 2 : ./google-cloud-sdk/install.sh

Step 3 : ./google-cloud-sdk/bin/gcloud init

Command: 

gsutil -m cp -R gs://BucketName./LocalFolder

How to set Specific floder as Public in  google cloud Bucket ?

Command:

gsutil acl ch -r -u allUsers:R gs://[BUCKET_NAME]/[Folder_NAME]


## License

    Copyright 2019, Trident Solutions

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
    

### ⭐ Show some ❤️ and star if you like what you see ⭐
