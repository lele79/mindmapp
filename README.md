<p align="center">
    <h1 align="center">
        <img width="40" src="resources/icon.png">
        CAFCha 
    </h1>
    <p align="center">Core application for project CAFCha</p>
</p>
============================================

##  Table of Contents
-  [Install](#hammer-install)
-  [Usage](#video_game-usage)
-  [Development](#chart_with_upwards_trend-development)
    - [Rules](#scroll-rules)
        - [Commits](#commits)
        - [Branches](#branches)
-  [License](#page_facing_up-license)
-  [Contacts](#telephone_receiver-contacts)
  -  [Developers](#boy-developers)


##  Install

With the following installed:
- git
- node >= 12
- npm >= 6

Clone the repo and install the dependencies from npm.

```bash
git clone https://gitlab.flosslab.com/cafcha/contratti
cd contratti
npm i
```

##  Usage

For local *development*:

Start Ganache:

```bash
ganache-cli -a "$(grep ACCOUNT_NUMBER .env | cut -d '=' -f2)" -d -m "$(grep DEV_MNEMONIC .env | cut -d '=' -f2)"
oz create CafchaBase --init
```
Compile with Truffle:

```bash
rm -fr build && truffle compile
```

Push project:

```bash
oz push
```

Init project:

```bash
oz create CafchaBase --init
```

Upgade project:

```bash
npm run compile && oz upgrade CafchaBase
```
Deploy Company data:

```bash
truffle exec scripts/create-companies.mock.js --network development
```

Start testing:

```bash
truffle test
```


If you want to generate the project documentation:

```bash
work in progress
```

A `documentation` folder will be generated in the project path.

##  Development

###  Rules

#### Commits

* Use this commit message format (angular style):  

    `[<type>] <subject>`

    where `type` must be one of the following:

    - feat: A new feature
    - fix: A bug fix
    - docs: Documentation only changes
    - style: Changes that do not affect the meaning of the code
    - refactor: A code change that neither fixes a bug nor adds a feature
    - test: Adding missing or correcting existing tests
    - chore: Changes to the build process or auxiliary tools and libraries such as documentation generation
    - update: Update of the library version or of the dependencies

and `body` must be should include the motivation for the change and contrast this with previous behavior (do not add body if the commit is trivial). 

* Use the imperative, present tense: "change" not "changed" nor "changes".
* Don't capitalize first letter.
* No dot (.) at the end.

#### Branches

* There is a master branch, used only for release.
* There is a dev branch, used to merge all sub dev branch.
* Avoid long descriptive names for long-lived branches.
* No CamelCase.
* Use grouping tokens (words) at the beginning of your branch names (in a similar way to the `type` of commit).
* Define and use short lead tokens to differentiate branches in a way that is meaningful to your workflow.
* Use slashes to separate parts of your branch names.
* Remove branch after merge if it is not important.

Examples:
    
    git branch -b docs/README
    git branch -b test/one-function
    git branch -b feat/side-bar
    git branch -b style/header


##  License
* Work in progress

##  Contacts
* Work in progress
###  Developers
* Omar Desogus
    - e-mail : omardesogus9@gmail.com
    - github : [@cedoor](https://github.com/cedoor)
    - website : https://cedoor.org
* Raffaele Porcu
    - e-mail : porcu.raffaele@gmail.com
    - github : [@lele79](https://github.com/lele79)
* Giacomo Corrias
    - e-mail : giacomocorrias7@gmail.com
    - github : [@Jeeiii](https://github.com/Jeeiii)

