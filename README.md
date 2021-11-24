## Sumo Logic AWS Observability Labs

This repo provides Sumo Logic AWS Observability lab and training guides. 

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

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the [LICENSE file](LICENSE) for details.

