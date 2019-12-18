<p align="center">
    <img alt="chart-streams logo" src="./assets/logo/chart-streams.png">
</p>
<p align="center">
    <a alt="GoReport" href="https://goreportcard.com/report/github.com/redhat-developer/helm-repository-service">
        <img alt="GoReport" src="https://goreportcard.com/badge/github.com/redhat-developer/helm-repository-service">
    </a>
    <a alt="Code Coverage" href="https://codecov.io/gh/redhat-developer/helm-repository-service">
        <img alt="Code Coverage" src="https://codecov.io/gh/redhat-developer/helm-repository-service/branch/master/graph/badge.svg">
    </a>
    <a href="https://godoc.org/github.com/redhat-developer/helm-repository-service/pkg/chartstreams">
        <img alt="GoDoc Reference" src="https://godoc.org/github.com/redhat-developer/helm-repository-service/pkg/chartstreams?status.svg">
    </a>
    <a alt="CI Status" href="https://travis-ci.com/redhat-developer/helm-repository-service">
        <img alt="CI Status" src="https://travis-ci.com/redhat-developer/helm-repository-service.svg?branch=master">
    </a>
     <a alt="CI Status" href="https://quay.io/repository/redhat-developer/helm-repository-service/status">
        <img alt="CI Status" src="https://quay.io/repository/redhat-developer/helm-repository-service/status">
    </a>
<!--
    <a alt="Docker-Cloud Build Status" href="https://hub.docker.com/r/otaviof/chart-streams">
        <img alt="Docker-Cloud Build Status" src="https://img.shields.io/docker/cloud/build/otaviof/chart-streams.svg">
    </a>
  -->
</p>

# Helm Charts Repository Service

`Helm Charts Repository Service`, formerly known as `chart-streams`, is a thin layer on top of a Git repository to make it behave as a Helm-Charts
repository would. With the the following advantages:

- keeping all charts data in a single place
- being able to on-the-fly generate `index.yaml`;
- use `semver` to retrieve a chart in a given `commit-id`/`branch`;

The basic workflow is represented as:

<p align="center">
    <img alt="chart-streams diagram" src="./assets/diagrams/cs-diagram-1.png">
</p>


## Usage

### Build and run
```
make run
```

Or

```
make && ./build/chart-streams serve
```

### Chart repository Index

Call the `/index.yaml` endpoint to get the index of all charts present in https://github.com/helm/charts/tree/master/stable
