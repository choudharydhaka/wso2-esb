# WSO2 ESB

This repository contains WSO2 ESB product docker file, with below mentioned details:

|Item|Description|Other|
|---|--------|--------|
|Product| WSO2 ESB|
|Version| 5.0.0|
|Java|OpenJDK 8 jre alpine|

## How to run?
### Run after building at your local machine
Step 1: Clone the project

```sh
git clone https://github.com/choudharydhaka/wso2-esb.git && cd  wso2-esb
```

Step 2: Build docker image
```sh
docker build . -t wso2-esb:1.0.0
```
or
```
./build.sh
```

Step 3: Run ESB

```sh
docker run wso2-esb:1.0.0 -p 9443:9443 -p 9763:9763 -p 8243:8243 -p 8280:8280 -name wso2-esb
```
or 
```
./run.sh
```

Step 4: Test 

```sh
./test.sh
```
or 

goto your browser and paste the following URL (https://localhost:9443/carbon)

### Run through Docker hub

```sh
docker pull wso2-esb:1.0.0
docker run wso2-esb:1.0.0 -p 9443:9443 -p 9763:9763 -p 8243:8243 -p 8280:8280 -name wso2-esb
```

## Test 
### Browser
Go to your browser and paste the following URL (https://localhost:9443/carbon)

### Bash
```
curl -vk https://localhost:9443/carbon
```
