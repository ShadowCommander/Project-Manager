# Project Condor

> A GitHub App built with [Probot](https://github.com/probot/probot)

Project Condor is a GitHub App that creates and moves project cards when a matching label is added to an issue.

The labels and their corrisponding columns can be configured in a `.github/config.yml` file placed in a repo or in a `.github` project in an organization:

```yaml
Project-Condor:
  org: Project-Condor-Test
  project: 1
  inbox: Inbox
  labels:
    To do: To do
    In progress: In progress
    Done: Done
```

The `org` is either the name of the organization or `null`. If `org` is `null` the app searches the current repo for the project.

The `project` is the project number in the url. If `project` is `null` the app chooses the first open project.

The `inbox` is the name of the column that the app will put any new issues that are created. If `inbox` is `null` cards are not created for new issues.

`labels` is the dictionary of label names and the corrisponding column. (`labelName`: `columnName`)

## Setup

For repos, put the config file in the repo at `.github/config.yml`.

For organizations, put the config file in `.github/config.yml` in a `.github` repo. (e.g. `organization/.github/.github/config.yml`)

 ```sh
# Install dependencies
npm install

# Run the bot
npm start
```

## Contributing

If you have suggestions for how Project Condor could be improved, or want to report a bug, open an issue! We'd love all and any contributions.

For more, check out the [Contributing Guide](CONTRIBUTING.md).

## License

[ISC](LICENSE) © 2019 ShadowCommander <10494922+ShadowCommander@users.noreply.github.com>
