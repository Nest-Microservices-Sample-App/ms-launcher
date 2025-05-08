### Pasos para crear los Git Submodules


1. Clone repo from Github
2. Run `git submodule update --recursive` to download submodules
3. Add the submodule, where `repository_url` is the URL of the repository and `directory_name` is the name of the folder where you want the submodule to be saved (the folder must not already exist in the project)
```
git submodule add <repository_url> <directory_name>
```
4. Add the changes to the repository (git add, git commit, git push)
Example:
```
git add .
git commit -m "Add submodule"
git push
```
5. Initialize and update submodules: when someone clones the repository for the first time, they must run the following command to initialize and update the submodules

```
git submodule update --init --recursive
```
6. To update the submodule references
```
git submodule update --remote
```

## Important
If you are working in the repository that contains submodules, **first update and push** the submodule, and **then** push the main repository.

If you do it the other way around, the main repository will lose the submodule references, and you'll have to resolve conflicts.

