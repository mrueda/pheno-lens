# Pheno-Lens
<p align="center">
    <em>Visualize and Perform Data Analytics on Phenotypic and Clinical Data Stored in GA4GH Standards and Beyond</em>
</p>

[![Build and Test](https://github.com/mrueda/pheno-lens/actions/workflows/build-and-test.yml/badge.svg)](https://github.com/mrueda/pheno-lens/actions/workflows/build-and-test.yml)
[![Coverage Status](https://coveralls.io/repos/github/CNAG-Biomedical-Informatics/pheno-lens/badge.svg?branch=main)](https://coveralls.io/github/CNAG-Biomedical-Informatics/pheno-lens?branch=main)
![version](https://img.shields.io/badge/version-0.04_beta-orange)
[![Docker Build](https://github.com/mrueda/pheno-lens/actions/workflows/docker-build.yml/badge.svg)](https://github.com/mrueda/pheno-lens/actions/workflows/docker-build.yml)
[![Docker Pulls](https://badgen.net/docker/pulls/manuelrueda/pheno-lens?icon=docker&label=pulls)](https://hub.docker.com/r/manuelrueda/pheno-lens/)
[![Docker Image Size](https://badgen.net/docker/size/manuelrueda/pheno-lens?icon=docker&label=image%20size)](https://hub.docker.com/r/manuelrueda/pheno-lens/)
[![Documentation Status](https://github.com/mrueda/pheno-lens/actions/workflows/documentation.yml/badge.svg)](https://github.com/mrueda/pheno-lens/actions/workflows/documentation.yml)
[![License: Artistic-2.0](https://img.shields.io/badge/License-Artistic%202.0-0298c3.svg)](https://opensource.org/licenses/Artistic-2.0)

**Documentation**: <a href="https://mrueda.github.io/pheno-lens" target="_blank">https://mrueda.github.io/pheno-lens</a>

**Docker Hub Image**: <a href="https://hub.docker.com/r/manuelrueda/pheno-lens/tags" target="_blank">https://hub.docker.com/r/manuelrueda/pheno-lens/tags</a>


# Download and Installation

## Installing Kibana

```
docker pull docker.elastic.co/kibana/kibana:7.10.0
```

Run Kibana
```bash     
docker run --link docker.elastic.co/elasticsearch/elasticsearch:7.10.0 -p 5601:5601 {docker.elastic.co/kibana/kibana:7.10.0}
```

# Access Kibana

Accessible via [http://localhost:5601](http://localhost:5601)

# Explore your data

Create an Index Pattern: To explore your data in Kibana, you first need to create an index pattern that matches the name of the index(es) into which you've ingested data.
* Go to the "Management" section, find "Index Patterns," and click "Create index pattern."
* Enter the index name (index_name as used in your bulk insert command) or a pattern that matches your index(es). Follow the prompts to select the time field if your data includes one.
* Discover: Once your index pattern is created, go to the "Discover" section to explore your data. Here, you can see all documents within your index, search and filter the data, and get a feel for what's available in your dataset.

# Visualize and Dashboard
After exploring your data in the Discover tab, you can start creating visualizations and dashboards in Kibana. The "Visualize" and "Dashboard" sections of Kibana provide powerful tools to create visual representations of your data.
