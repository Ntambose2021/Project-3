# Project-3

Stages

- build
- test

build the store:
  stage: build
  script: 
    - mkdir build
    - cd build
    - touch car.txt
    - echo "frontend" > store.txt
    - echo "shelves" > store.txt
    - echo "money" > store.txt
    
test the store:
  stage: test
  script:
    - test -f build/store.txt
    - cd build
    - grep "frontend" store.txt
    - grep "shelves" store.txt
    - grep "money" > store.txt

