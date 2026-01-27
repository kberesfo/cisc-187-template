# Data Structs Lab Template

## Build
```
cmake -S . -B build -G Ninja
cmake --build build
```


## Merge Template
first clone:
```
git clone <instructor-lab-repo-url>
```
then merge template:
```
git remote add template <your-template-repo-url>
git fetch template
git merge template/main --allow-unrelated-histories
```