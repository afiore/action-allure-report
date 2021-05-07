# Action generate Allure report

Uses [allure-framework](https://github.com/allure-framework/allure2) to generate a browsable test report

## Inputs

### results-dir

**Required** The relative path to the Allure results directory. Default `allure-results`.

### report-dir

**Required** The relative path to the directory where Allure will write the generated report. Default `allure-results`.

## Building and running locally

Build the docker image by running:

```bash
docker build . -t allure-gen
```

Then, assuming you have a `allure-results` and a `allure-report` folder in your current directory, you can generate the report by running:

```bash
docker run -v ${PWD}:/github/workspace allure-gen allure-results allure-report
```

OBS.: Este repositório é uma cópia de [@afiore/action-allure-report](https://github.com/afiore/action-allure-report), porém como o mesmo está com erro na URL do Dockerfile, criei este com os ajustes necessários, porém os créditos são todos referenciados @afiore.


