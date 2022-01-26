---
title: "Configure GitHub"
chapter: true
weight: 16
---

## Configure GitHub

To set up and configure GitHub with Sumo Logic, you will runn an automated script using a curl command in a terminal or command line. The script prompts for information configured during [setup](/035_github/33_access_keys.html).

Run the following command:

```
sh -c "$(curl -sSL https://raw.githubusercontent.com/SumoLogic/sumologic-solution-templates/github_getting_started_guide/software-development-optimization-terraform/scripts/getting-started)" -- github
```

Enter your GitHub and Sumo Logic information at the prompts:

1. Enter the GitHub personal access token you created in [Create a Sumo Logic access key](/035_github/33_access_keys.html#create-a-sumo-logic-access-key).

1. Enter the name of the GitHub organization you would like to collect GitHub data on.

    ![Access Token](/images/github/github-access-token.png)

1. Enter the Sumo Logic Personal Access Token you created in [Create a GitHub personal access token](/035_github/33_access_keys.html#create-a-github-personal-access-token).

1. Enter the region you created your Sumo Logic account in. [Use this API best practices doc to determine which region code to provide](https://help.sumologic.com/APIs/General-API-Information/Sumo-Logic-Endpoints-and-Firewall-Security#how-can-i-determine-which-endpoint-i-should-use)

    ![Access Token](/images/github/sumo-logic-access-token.png)

The script will download a specific version of Terraform and dependent plugins and apply Terraform code. The Terraform installed **will not** interfere with any existing installations of Terraform.

If the script completes, you will have a new folder called **Software Development Optimization** in your Sumo Logic Personal folder. There will be a collection of GitHub dashboards that will populate as you and your team use GitHub.