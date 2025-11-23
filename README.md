# GitLab webhook batch replacement

Batch replace webhooks for multiple GitLab projects using GitLabForm.  Useful when the webhook URL or secret needs to be updated.

<https://gitlab.com/brlin/gitlab-webhook-batch-replacement>  
[![The GitLab CI pipeline status badge of the project's `main` branch](https://gitlab.com//badges/main/pipeline.svg?ignore_skipped=true "Click here to check out the comprehensive status of the GitLab CI pipelines")](https://gitlab.com/brlin/gitlab-webhook-batch-replacement/-/pipelines) [![GitHub Actions workflow status badge](https://github.com/brlin-tw/gitlab-webhook-batch-replacement/actions/workflows/check-potential-problems.yml/badge.svg "GitHub Actions workflow status")](https://github.com/brlin-tw/gitlab-webhook-batch-replacement/actions/workflows/check-potential-problems.yml) [![pre-commit enabled badge](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white "This project uses pre-commit to check potential problems")](https://pre-commit.com/) [![REUSE Specification compliance badge](https://api.reuse.software/badge/gitlab.com/brlin/gitlab-webhook-batch-replacement "This project complies to the REUSE specification to decrease software licensing costs")](https://api.reuse.software/info/gitlab.com/brlin/gitlab-webhook-batch-replacement)

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

## Licensing

Unless otherwise noted([comment headers](https://reuse.software/spec-3.3/#comment-headers)/[REUSE.toml](https://reuse.software/spec-3.3/#reusetoml)), this product is licensed under [the 3.0 version of the GNU Affero General Public License](https://www.gnu.org/licenses/agpl-3.0.html), or any of its more recent versions of your preference.

This work complies to [the REUSE Specification](https://reuse.software/spec/), refer to the [REUSE - Make licensing easy for everyone](https://reuse.software/) website for info regarding the licensing of this product.
