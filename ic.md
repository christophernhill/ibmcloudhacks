IBM cloud commands

```
root@301ac20d922d:/# Bluemix_CLI/bin/ibmcloud sl vs options
Name                              Value   
datacenter                        ams01,ams03,che01,dal05,dal06,dal07,dal09,dal10,dal12,dal13,fra02,fra04,fra05,hkg02,hou02,lon02,lon04,lon05,lon06,mel01,mex01,mil01,mon01,osl01,par01,sao01,sea01,seo01,sjc01,sjc03,sjc04,sng01,syd01,syd04,syd05,tok02,tok04,tok05,tor01,wdc01,wdc04,wdc06,wdc07   
flavors (balanced)                B1_1X2X25,B1_1X2X25,B1_1X2X100,B1_1X2X100,B1_1X4X25,B1_1X4X25,B1_1X4X100,B1_1X4X100,B1_2X4X25,B1_2X4X25,B1_2X4X100,B1_2X4X100,B1_2X8X25,B1_2X8X25,B1_2X8X100,B1_2X8X100,B1_4X8X25,B1_4X8X25,B1_4X8X100,B1_4X8X100,B1_4X16X25,B1_4X16X25,B1_4X16X100,B1_4X16X100,B1_8X16X25,B1_8X16X25,B1_8X16X100,B1_8X16X100,B1_8X32X25,B1_8X32X25,B1_8X32X100,B1_8X32X100,B1_16X32X25,B1_16X32X25,B1_16X32X100,B1_16X32X100,B1_16X64X25,B1_16X64X25,B1_16X64X100,B1_16X64X100,B1_32X64X25,B1_32X64X25,B1_32X64X100,B1_32X64X100,B1_32X128X25,B1_32X128X25,B1_32X128X100,B1_32X128X100,B1_48X192X25,B1_48X192X25,B1_48X192X100,B1_48X192X100   
flavors (balanced local - hdd)    BL1_1X2X100,BL1_1X4X100,BL1_2X4X100,BL1_2X8X100,BL1_4X8X100,BL1_4X16X100,BL1_8X16X100,BL1_8X32X100,BL1_16X32X100,BL1_16X64X100,BL1_32X64X100,BL1_32X128X100,BL1_56X242X100   
flavors (balanced local - ssd)    BL2_1X2X100,BL2_1X4X100,BL2_2X4X100,BL2_2X8X100,BL2_4X8X100,BL2_4X16X100,BL2_8X16X100,BL2_8X32X100,BL2_16X32X100,BL2_16X64X100,BL2_32X64X100,BL2_32X128X100,BL2_56X242X100   
flavors (compute)                 C1_1X1X25,C1_1X1X25,C1_1X1X100,C1_1X1X100,C1_2X2X25,C1_2X2X25,C1_2X2X100,C1_2X2X100,C1_4X4X25,C1_4X4X25,C1_4X4X100,C1_4X4X100,C1_8X8X25,C1_8X8X25,C1_8X8X100,C1_8X8X100,C1_16X16X25,C1_16X16X25,C1_16X16X100,C1_16X16X100,C1_32X32X25,C1_32X32X25,C1_32X32X100,C1_32X32X100,AC1_8X60X25,AC1_8X60X100,AC1_16X120X25,AC1_16X120X100   
flavors (memory)                  M1_1X8X25,M1_1X8X25,M1_1X8X100,M1_1X8X100,M1_2X16X25,M1_2X16X25,M1_2X16X100,M1_2X16X100,M1_4X32X25,M1_4X32X25,M1_4X32X100,M1_4X32X100,M1_8X64X25,M1_8X64X25,M1_8X64X100,M1_8X64X100,M1_16X128X25,M1_16X128X25,M1_16X128X100,M1_16X128X100,M1_30X240X25,M1_30X240X25,M1_30X240X100,M1_30X240X100,M1_48X384X25,M1_48X384X25,M1_48X384X100,M1_48X384X100,M1_56X448X25,M1_56X448X25,M1_56X448X100,M1_56X448X100,M1_64X512X25,M1_64X512X25,M1_64X512X100,M1_64X512X100   
cpu (standard)                    1,2,4,8,12,16,32,56   
cpu (dedicated)                   1,2,4,8,16,32,56   
cpu (dedicated host)              1,2,4,8,12,16,32,56   
memory                            1024,2048,4096,6144,8192,12288,16384,32768,49152,65536,131072,247808   
memory (dedicated host)           1024,2048,4096,6144,8192,12288,16384,32768,49152,65536,131072,247808   
os (CENTOS)                       CENTOS_5_32,CENTOS_5_64,CENTOS_6_32,CENTOS_6_64,CENTOS_7_64,CENTOS_LATEST,CENTOS_LATEST_32,CENTOS_LATEST_64   
os (CLOUDLINUX)                   CLOUDLINUX_5_32,CLOUDLINUX_5_64,CLOUDLINUX_6_32,CLOUDLINUX_LATEST,CLOUDLINUX_LATEST_32,CLOUDLINUX_LATEST_64   
os (COREOS)                       COREOS_CURRENT_64,COREOS_LATEST,COREOS_LATEST_64   
os (DEBIAN)                       DEBIAN_6_32,DEBIAN_6_64,DEBIAN_7_32,DEBIAN_7_64,DEBIAN_8_32,DEBIAN_8_64,DEBIAN_9_64,DEBIAN_LATEST,DEBIAN_LATEST_32,DEBIAN_LATEST_64   
os (REDHAT)                       REDHAT_5_32,REDHAT_5_64,REDHAT_6_32,REDHAT_6_64,REDHAT_7_64,REDHAT_LATEST,REDHAT_LATEST_32,REDHAT_LATEST_64   
os (UBUNTU)                       UBUNTU_10_32,UBUNTU_10_64,UBUNTU_12_32,UBUNTU_12_64,UBUNTU_14_32,UBUNTU_16_64,UBUNTU_18_64,UBUNTU_LATEST,UBUNTU_LATEST_32,UBUNTU_LATEST_64   
os (VYATTACE)                     VYATTACE_6.5_64,VYATTACE_6.6_64,VYATTACE_LATEST,VYATTACE_LATEST_64   
os (WIN)                          WIN_2003-DC-SP2-1_32,WIN_2003-DC-SP2-1_64,WIN_2003-ENT-SP2-5_32,WIN_2003-ENT-SP2-5_64,WIN_2003-STD-SP2-5_32,WIN_2003-STD-SP2-5_64,WIN_2008-STD-R2-SP1_64,WIN_2008-STD-SP2_32,WIN_2008-STD-SP2_64,WIN_2012-STD-R2_64,WIN_2012-STD_64,WIN_2016-STD_64,WIN_2019-STD_64,WIN_LATEST,WIN_LATEST_32,WIN_LATEST_64   
san disk (0)                      25,100   
san disk (2)                      10,20,25,30,40,50,75,100,125,150,175,200,250,300,350,400,500,750,1000,1500,2000   
san disk (3)                      10,20,25,30,40,50,75,100,125,150,175,200,250,300,350,400,500,750,1000,1500,2000   
san disk (4)                      10,20,25,30,40,50,75,100,125,150,175,200,250,300,350,400,500,750,1000,1500,2000   
san disk (5)                      10,20,25,30,40,50,75,100,125,150,175,200,250,300,350,400,500,750,1000,1500,2000   
local disk (0)                    25,100   
local disk (2)                    25,100,150,200,300   
local (dedicated host) disk (0)   25,100,150   
local (dedicated host) disk (2)   25,100,150,300,400   
local (dedicated host) disk (3)   25,100,150,300,400   
local (dedicated host) disk (4)   25,100,150,300,400   
local (dedicated host) disk (5)   25,100,150,300,400   
nic                               10,100,1000   
nic (dedicated host)              100,1000   

```

```
Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal10 --os CENTOS_LATEST_64 --hostname cnh-v100-02 --domain QI-Hill.cloud --san 
```

```
Bluemix_CLI/bin/ibmcloud sl vs list  
```



```
Bluemix_CLI/bin/ibmcloud sl vs detail 84047749 
```

```
Bluemix_CLI/bin/ibmcloud sl vs cancel -f  84047749
```

```
Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal10 --os CENTOS_LATEST_64 --hostname cnh-v100-03-8 --domain QI-Hill.cloud --san -f 
Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal12 --os CENTOS_LATEST_64 --hostname cnh-v100-03-9 --domain QI-Hill.cloud --san -f 
Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter lon04 --os CENTOS_LATEST_64 --hostname cnh-v100-03-17 --domain QI-Hill.cloud --san -f 
```

```
#!/bin/bash -xv
set +e
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter ams01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-1 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter ams03 --os CENTOS_LATEST_64 --hostname cnh-v100-03-2 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter che01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-3 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal05 --os CENTOS_LATEST_64 --hostname cnh-v100-03-4 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal06 --os CENTOS_LATEST_64 --hostname cnh-v100-03-5 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal07 --os CENTOS_LATEST_64 --hostname cnh-v100-03-6 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal09 --os CENTOS_LATEST_64 --hostname cnh-v100-03-7 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal10 --os CENTOS_LATEST_64 --hostname cnh-v100-03-8 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal12 --os CENTOS_LATEST_64 --hostname cnh-v100-03-9 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter dal13 --os CENTOS_LATEST_64 --hostname cnh-v100-03-10 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter fra02 --os CENTOS_LATEST_64 --hostname cnh-v100-03-11 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter fra04 --os CENTOS_LATEST_64 --hostname cnh-v100-03-12 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter fra05 --os CENTOS_LATEST_64 --hostname cnh-v100-03-13 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter hkg02 --os CENTOS_LATEST_64 --hostname cnh-v100-03-14 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter hou02 --os CENTOS_LATEST_64 --hostname cnh-v100-03-15 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter lon02 --os CENTOS_LATEST_64 --hostname cnh-v100-03-16 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter lon04 --os CENTOS_LATEST_64 --hostname cnh-v100-03-17 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter lon05 --os CENTOS_LATEST_64 --hostname cnh-v100-03-18 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter lon06 --os CENTOS_LATEST_64 --hostname cnh-v100-03-19 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter mel01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-20 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter mex01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-21 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter mil01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-22 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter mon01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-23 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter osl01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-24 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter par01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-25 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter sao01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-26 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter sea01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-27 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter seo01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-28 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter sjc01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-29 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter sjc03 --os CENTOS_LATEST_64 --hostname cnh-v100-03-30 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter sjc04 --os CENTOS_LATEST_64 --hostname cnh-v100-03-31 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter sng01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-32 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter syd01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-33 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter syd04 --os CENTOS_LATEST_64 --hostname cnh-v100-03-34 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter syd05 --os CENTOS_LATEST_64 --hostname cnh-v100-03-35 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter tok02 --os CENTOS_LATEST_64 --hostname cnh-v100-03-36 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter tok04 --os CENTOS_LATEST_64 --hostname cnh-v100-03-37 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter tok05 --os CENTOS_LATEST_64 --hostname cnh-v100-03-38 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter tor01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-39 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter wdc01 --os CENTOS_LATEST_64 --hostname cnh-v100-03-40 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter wdc04 --os CENTOS_LATEST_64 --hostname cnh-v100-03-41 --domain QI-Hill.cloud --san -f   )
( Bluemix_CLI/bin/ibmcloud sl vs create --flavor AC2_8X60X25 --datacenter wdc06 --os CENTOS_LATEST_64 --hostname cnh-v100-03-42 --domain QI-Hill.cloud --san -f   )
```
