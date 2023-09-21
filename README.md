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
Open a gitlab account if not created.
In the project page, create a new project .
create a new file in the created project and name the file as .gitlab-ci.yml as this is the syntax for naming the file.
write the required CI/CD code in the yml file and commit changes . 
Gitlab will automatically tell you whether the code written is synatactilly correct or you have to make changes . 
if everything is correct ,gitlab will automatically start building your pipeline which you can see.
if everything passes, you can click on the stages you created and then see the CLI in which everything is executed.

outputs:
![image](https://github.com/ananyashree2407/GITLAB/assets/83506143/cf8dfef5-75ed-4e6c-b423-aeda4b4472c3)

![image](https://github.com/ananyashree2407/GITLAB/assets/83506143/a3d99d64-b663-4b6f-a368-01c40c113fad)

![image](https://github.com/ananyashree2407/GITLAB/assets/83506143/b2545bb5-e2cf-404a-abf5-32fc5c1de3b2)


