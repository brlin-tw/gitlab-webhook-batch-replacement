# GitLab webhook batch replacement

Batch replace webhooks for multiple GitLab projects using GitLabForm.  Useful when the webhook URL or secret needs to be updated.

<https://gitlab.com/brlin/gitlab-webhook-batch-replacement>

\#gitlabform \#gitlab \#webhook \#automation

## Usage

### Prerequisites

The following prerequisites are required before using this product:

* [Install GitLabForm](https://gitlabform.github.io/gitlabform/installation/)
* Acquire a [GitLab Personal Access Token](https://docs.gitlab.com/user/profile/personal_access_tokens/) with the `api` scope.
* You have network connectivity to the target GitLab instance.

### Process

Refer to the following process for using this product:

1. Download the release archive from [the Releases page](https://gitlab.com/brlin/gitlab-webhook-batch-replacement/-/releases).
1. Extract the release archive.
1. Edit [the `config.yml` file](config.yml) to set the GitLab URL, Personal Access Token, and desired webhook configurations.  The default configuration sets up a Rocket.Chat webhook for all accessible projects.
1. Run the following command to apply the configuration:

   ```bash
   gitlabform ALL
   ```

## Known issues

GitLab REST API (and thus GitLabForm) does not support masking webhook secrets at the moment(2025/11/23).  Therefore it cannot be used if you require masked secrets for webhooks.

## References

The following materials are referenced during the development of this project:

* [GitLabForm](https://gitlabform.github.io/gitlabform/)  
  Explains the basic concepts of GitLabForm.
* [💾 Installation - GitLabForm](https://gitlabform.github.io/gitlabform/installation/)  
  Explains how to install and run GitLabForm.
* [Configuration reference - GitLabForm](https://gitlabform.github.io/gitlabform/reference/)  
  Explains the basic concepts of GitLabForm configuration.
* [Webhooks - GitLabForm](https://gitlabform.github.io/gitlabform/reference/webhooks/)  
  Explains how to configure webhooks using GitLabForm.
* [Add a webhook to a project | Project webhooks API | GitLab Docs](https://docs.gitlab.com/api/project_webhooks/#add-a-webhook-to-a-project)  
  Explains the available attributes when creating a webhook via the GitLab API.
