# Command and Configuration GIT

#### List all the config of GIT in your machine.

```sh
git config --list
```
#### There are three types of configuration in GIT

```sh
#The git configure command for the whole system.
git config --system
```
```sh
#the specific user git configuration
git config --global
```
```sh
#the specific project's git configuration.
git config --local
```
#### For the edit configuration use the flag
```sh
git config --global --edit
```
#### To specify an editor to open the configuration file with.

```sh
#Command to seting editor
git config --global core.editor code
```
#### Add in file end line .gitconfig
```
[core]
editor = code --wait
[alias]
s=!git status -s
c=!git add --all && git commit -m
l=!git log --pretty=format:'%C(blue)%h %C(yellow)%d %C(red)%s - %C(cyan)%cn, %C(green)%cr'
```
| Command Before change                      | Command After change |
|--------------------------------------------|----------------------|
| git status                                 | git s                |
| git add --all<br/> git commit -m "message" | git c "message"      |
| git log                                    | git l                |

#### Standardize project commits

The convention that will be used in the project
```
<type>: <description>
```
The types used

> - **build**: `used for project build-related changes such as build settings, dependencies or build scripts.`
> - **chore**: `used for minor task changes that are not related to a source code change itself. This might include updating libraries, performing maintenance tasks, or updating configuration files.`
> - **ci**: `used for changes to configuration files or scripts related to continuous integration (CI) or continuous delivery (CD).`
> - **docs**: `used for project documentation changes, such as README updates, comments or internal documentation.`
> - **style**: `used for changes that don't affect the meaning of the code, such as changes to formatting, whitespace, variable names or linter adjustments.`
> - **refactor**: `used for code changes that don't add new features or fix bugs, but improve code structure or readability.`
> - **perf**: `used for changes that improve code performance.`
> - **test**: `used to add or modify tests.`

for more details
    [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
 
#### To enforce following design convention.

```sh
#Run using npm
npm i git-commit-msg-linter
```
```sh
#Run using yarn
yarn add git-commit-msg-linter
```
for more details [Npm Git Commit msg linter](https://www.npmjs.com/package/git-commit-msg-linter).
