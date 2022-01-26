---
title: "Set Up Access Keys"
chapter: true
weight: 14
---

## Set Up Access Keys

### Create a Sumo Logic access key

Create an access key to programatically manage your Sumo Logic account following these instructions: [Manage all users’ access keys on Access Keys page](https://help.sumologic.com/Manage/Security/Access-Keys#manage-all-users%E2%80%99-access-keys-on-access-keys-page).

{{% notice note %}}
Copy your access ID and key to another location. You will need them in a later step.
{{% /notice %}}

![Access Key](/images/trial/create-access-key.gif)

### Create a GitHub personal access token

In order to create a webhook that will send data to your Sumo Logic account, the automation in this guide will need an access token for your GitHub account. For more information, see [GitHub Creating a Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token).

1. Visit your [Personal Access Tokens page](https://github.com/settings/tokens) in your GitHub account.

1. Create an access token with the following permissions:

   - read:org
   - admin:repo_hook
   - admin:org_hook

{{% notice note %}}
Copy your access token to another location. You will need it in a later step.
{{% /notice %}}