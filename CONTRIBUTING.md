# Contributing Guidelines

Thank you for your interest in contributing to our project. Whether it's a bug report, new feature, correction, or additional
documentation, we greatly value feedback and contributions from our community.

Please read through this document before submitting any issues or pull requests to ensure we have all the necessary
information to effectively respond to your bug report or contribution.


## Reporting Bugs/Feature Requests

We welcome you to use the GitHub issue tracker to report bugs or suggest features.

When filing an issue, please check existing open, or recently closed, issues to make sure somebody else hasn't already
reported the issue. Please try to include as much information as you can. Details like these are incredibly useful:

* A reproducible test case or series of steps
* The version of our code being used
* Any modifications you've made relevant to the bug
* Anything unusual about your environment or deployment


## Contributing via Pull Requests
Contributions via pull requests are much appreciated. Before sending us a pull request, please ensure that:

1. You are working against the latest source on the *main* branch.
2. You check existing open, and recently merged, pull requests to make sure someone else hasn't addressed the problem already.
3. You open an issue to discuss any significant work - we would hate for your time to be wasted.

To send us a pull request, please:

1. Fork the repository.
2. Modify the source; please focus on the specific change you are contributing. If you also reformat all the code, it will be hard for us to focus on your change.
3. Ensure local tests pass.
4. Commit to your fork using clear commit messages.
5. Send us a pull request, answering any default questions in the pull request interface.
6. Pay attention to any automated CI failures reported in the pull request, and stay involved in the conversation.

GitHub provides additional document on [forking a repository](https://help.github.com/articles/fork-a-repo/) and
[creating a pull request](https://help.github.com/articles/creating-a-pull-request/).

## Folders and Files

A full lab should be collected in one folder.

* ###_folder_name: Folder for the lab, for example 040_observability_monitoring
* ##_scenario.md: Introduction to the lab with a list of the tools used, issues investigated, and expectatons, for example 30_scenario.md
* ##_lab#.md: The lab instructions including images and notes, for example 42_lab1.md

Each file name includes an even number based on the folder name. For example folder 30 would have file names starting with 30, 32, 34, and so on. 

Each folder must have an _index.md file. The frontmatter (first lines) must include the following customized for your content:

```
---
title: "AWS Observability and Monitoring Lab"
chapter: true
draft: false
weight: 6
---
```

The weight can be tricky and needs testing as this determines what order the folder is in the left navigation. Each subsequent file weight should be higher and in order after the index file's weight. The title displays in the left nav.

The first line in content should be an H1 (#) or H2 (##), which displays as the name of the page for documentation.

For an example, see the `040_observability_monitoring folder` and files.

### Images

Save all images as .png files in the /static/images folder. To better organize, we recommend saving images in folders per lab. To embed an image in your lab, use this code:

```
![Alt Name](/images/folder-name/filename.png)
```

Here is an example:

```markdown
![Prod Account](/images/lab-monitoring/lab1-prod.png)
```

### Links

Markdown links in Hugo use the following format between files in this repo:

```markdown
[Name of Link](/###_folder_name/##_file_name.html)
```

Here is an example:

```markdown
[Set Up Sumo Logic](/030_self_guided_setup/38_sumo_setup.html)
```

To link to content outside of these files, use this format:

```markdown
[Name of Link](URL)
```

Here is an example:

```markdown
[Self-Paced Training](https://help.sumologic.com/01Start-Here/Quick-Start-Tutorials/SelfPacedTrainingFundamentals)
```

## Contribute Content

This repo uses Hugo. To contribute content, you need to fork and clone the repo, install a few applications in the cloned folder, then work in a branch. If new to Git and GitHub, we recommend installing [GitHub Desktop](https://desktop.github.com/).

### Fork and Clone the Repo

You should fork [this repo](https://github.com/aws-samples/aws-modernization-with-sumologic) and clone locally to begin. To add or update content, you will create a branch, make changes, commit updates, push to GitHub, and create a pull request (PR). This will generate a PR for AWS to review. When merged, documentation will rebuild and deploy.

1. You need a GitHub account.
1. Click the Fork icon on the top-right of the site and walk through prompts. This will create a copy on your account.
1. Click the **Code** drop down and select how you want to clone. An easy method is using [GitHub Desktop](https://desktop.github.com/).

### Install Requirements

Using a terminal application, change directory to the cloned repo. Install the following:

* [Homebrew](https://brew.sh/) for MacOS, commmand in terminal: 

    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```

* [Hugo], command in terminal: `brew install hugo`
* [Git], command in terminal: `brew install git`

### Create a Branch

To create a branch using GitHub Desktop:

1. Click **Current Branch** > **New Branch**.
1. Enter a name with dashes, no spaces, that describes the work.
1. Start working locally using apps like [VS Code](https://code.visualstudio.com/), [Sublime](https://www.sublimetext.com/), [Atom](https://atom.io/). You will see the branch name in the bottom of the application window.

### Build Hugo

1. To build, open a terminal (MacOS) or run prompt (Windows).
1. Change directory to the location you cloned the repo.
1. Enter the command: `hug server -D`

Hugo builds the site and deploys it to http://localhost:1313/. Open this site to review. 

### Additional Theme Information

This content uses this [repo branch](https://github.com/aws-samples/aws-modernization-workshop-base/tree/mp-workshops) as a base. For more information, review the readme.

This branch also contains the following static resources and scripts:

* static/css/mp-devops-series.css - This includes the CSS for the buttons on the AWS Request Credit Page.
* layouts/partials/custom-header.html - This injects both Marketo data tracking script to the head of every page in the workshop and inserting the various CSS files.

config.toml changes:
* defaultContentLanguage = "oyo". "oyo" is short for on-your-own.
* Setting defaultContentLanguageInSubdir to "false". This allows *.awsworkshops.io/ to default to the oyo lab.
* Setting disableLanguageSwitchingButton to false. This allows the ability to toggle between EE and oyo track in the navigation button
* Setting the languages parameters on L:82


## Finding contributions to work on
Looking at the existing issues is a great way to find something to contribute on. As our projects, by default, use the default GitHub issue labels (enhancement/bug/duplicate/help wanted/invalid/question/wontfix), looking at any 'help wanted' issues is a great place to start.


## Code of Conduct
This project has adopted the [Amazon Open Source Code of Conduct](https://aws.github.io/code-of-conduct).
For more information see the [Code of Conduct FAQ](https://aws.github.io/code-of-conduct-faq) or contact
opensource-codeofconduct@amazon.com with any additional questions or comments.


## Security issue notifications
If you discover a potential security issue in this project we ask that you notify AWS/Amazon Security via our [vulnerability reporting page](http://aws.amazon.com/security/vulnerability-reporting/). Please do **not** create a public github issue.


## Licensing

See the [LICENSE](LICENSE) file for our project's licensing. We will ask you to confirm the licensing of your contribution.
