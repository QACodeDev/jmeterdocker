#JMeter Docker Image

Easily run JMeter tests without installing Java on your machine.
Image contains superb useful JMeter plugins provided by https://jmeter-plugins.org/.

## Usage

Folder structure

* Scripts - contains scripts
* TestdData - Any test Data file
* Results - for results files

To run sample load test...
1. Create an image from the docker file by below commnad
docker build -t <jmeter_image_name> .

2. pull the jmeter image from docker hub.

docker pull  droplr/jmeter 
```
$ docker run -v $(pwd):/jmeter -t droplr/jmeter -n -t Scripts/<Script_Name>.jmx -JFilePath   TestData/<Test_Data_FileName>.csv -l Results/<ResultFileName>.jtl

### Clean old results before starting new test

You have to remove old results file, otherwise JMeter will append results of the new test-run to it.

```results.jtl
```
