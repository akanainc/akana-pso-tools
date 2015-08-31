# Akana PSO Tools
![Image of Akana] 
(https://www.akana.com/img/formerlyLOGO8.png) 
[Akana.com](http://akana.com)

## Akana PSO Tools - Technology Preview

## Akana APIHooks Technology Preview
### About the Akana APIHooks Technology Preview

### Pre-Reqs
- You need Policy Manager v7.2.11 or later
- You need Community Manager v7.2.4.1 or later
- you must install the pso technology preview:
      + unzip the com.akana.pso.apihooks.technology.preview_7.2.92.zip (available in this repository) into the <Policy Manager Home>/sm70 directory
    + stop all PM and ND(s)
    + run the configurator in update mode for all the PM and ND instances:
        + To run in configuration mode delete the cache directory of the container instance you are updating.
        + run this command, depending on whether you are running on Windows or Linux:
            Windows: 
            [Gateway base dir]\sm70\bin>startup.bat configurator "-Dsilent=true" "-DdeploymentName=Standalone" "-Dproperties=C:/<property file directory location>/myprops.properties" 
     
            UNIX 
            [Gateway base dir]/sm70/bin>startup.sh configurator "-Dsilent=true" "-DdeploymentName=Standalone" "-Dproperties=/export/home/username/<property file directory location>\myprops.properties"
        + the myprops.properties path must be the fully qualified path, and the file contnents will look like:
            container.instance.name=[intance name, e.g. PM]
            credential.username = [administrator login] 
            credential.password = [administrator password] 
            default.host=[instance Host, e.g. localhost] 
            default.port=[instance Port, e.g. 9905]
            wizard.mode=update
     + restart all PM and ND(s)


### License
Copyright 2015 Akana, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

