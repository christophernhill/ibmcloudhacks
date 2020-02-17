* ```docker pull ubuntu```
* ```docker run -d -v `pwd`:/host --name 'ibmcloud' -P -i -t --rm ubuntu /bin/bash```
* ```docker exec -i -t ibmcloud /bin/bash```
* ```apt-get -y update```
* ```apt-get -y upgrade```
* ```apt-get -y install curl```
* ```dl=`curl https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64  | sed s'/.*"\(https[^"]*\).*/\1/'` ```
* ```curl ${dl} > `basename ${dl}` ```
* ```tar -xzvf `basename ${dl}` ```
* ``` Bluemix_CLI/bin/ibmcloud login -u XXX@mit.edu -p 'PPPPPPPPPPPPPPPPPPPP' -r us-east -c 6b8a45a3901c48c88bdc10df5aedef6a ```

# configure to use gen 2 vpc in region us-south

* ```Bluemix_CLI/bin/ibmcloud plugin install vpc-infrastructure```
* ```Bluemix_CLI/bin/ibmcloud is target --gen 2```
* ```Bluemix_CLI/bin/ibmcloud target -r us-south```
