This is the simple CI/CD pipeline built for task5 .
the code written in the yml file is as below:


stages:
  - build
  - test

build:
  stage: build
  script:
    - echo "Building"
    - mkdir build
    - touch build/info.txt
  artifacts:
    paths:
      - build/

test:
  stage: test
  script:
    - echo "testing"
    - test -f build/info.txt

the steps followed for creating the CI/CD pipeline in gitlab is:
