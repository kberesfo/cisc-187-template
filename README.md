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
git remote add template https://github.com/kberesfo/cisc-187-template.git
git fetch template
git merge template/main --allow-unrelated-histories
```

```
git remote remove template
```

## Submodule

```
git submodule add <repo> labs
```

## Fetch upstream

```
git fetch upstream
git merge upstream/main
```
