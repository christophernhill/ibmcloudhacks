* ```docker pull ubuntu```
* ```docker run -d -v `pwd`:/host --name 'ibmcloud' -P -i -t --rm ubuntu /bin/bash```
* ```docker exec -i -t ibmcloud /bin/bash```
* ```apt-get -y update```
* ```apt-get -y upgrade```
* ```apt-get -y install curl```
* ```dl=`curl https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64  | sed s'/.*"\(https[^"]*\).*/\1/'` ```
* ```curl ${dl} > `basename ${dl}` ```
