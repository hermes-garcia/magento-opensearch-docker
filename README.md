# OpenSearch Docker compose for Magento 2.4+

### Installation
<em>Prerequisite: docker installed</em>

1. Clone this repo
```
git clone {{url}}
```

2. Navigate to the repository folder
```
$ cd ./magento-opensearch-docker
```

3. Run Docker build to create the image
```
$ docker build --tag="opensearchproject/opensearch:1.2.4" .
```

4. Run Docker run to up the container
```
$ docker run -p 9200:9200 -p 9600:9600 -e "discovery.type=single-node" opensearchproject/opensearch:1.2.4
```

5. Verify the OS connection
```
$ curl -XGET localhost:9200
```