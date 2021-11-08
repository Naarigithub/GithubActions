# GithubActions

**self-hosted runners**: Self-hosted runners offer more control of hardware, operating system, and software tools than GitHub-hosted runners provide.

- We can install our required software which is in our local.
- We can choose OS not offered by git hub hosted runners.
- These can be physical, virtual ,on-prem or in cloud.

**Self hosted runners levels:**
Repository level : These are dedicated to a single  repository.
Organisation level : These are process jobs for multiple repositories in organisation.
Enterprise  level: These runners can be assigned to multiple  organisations in an enterprise  account.

- When a new version  is  released , the runner application updates automatically  itself 
- Self hosted runner is automatically removed  form GitHub if it is not connected  to GitHub actions for more that 30 days.

**limits on GitHub Actions usage when using self-hosted runners:**

Workflow run time - Each workflow run is limited to 72 hours. If a workflow run reaches this limit, the workflow run is cancelled.

Job queue time - Each job for self-hosted runners can be queued for a maximum of 24 hours. If a self-hosted runner does not start executing the job within this limit, the job is terminated and fails to complete.

API requests - You can execute up to 1000 API requests in an hour across all actions within a repository. If exceeded, additional API calls will fail, which might cause jobs to fail.

Job matrix - A job matrix can generate a maximum of 256 jobs per workflow run. This limit also applies to self-hosted runners.

Workflow run queue - No more than 500 workflow runs can be queued in a 10 second interval per repository. If a workflow run reaches this limit, the workflow run is terminated and fails to complete.
