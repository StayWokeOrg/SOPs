# Contributing

Contributions are welcomed and encouraged! Here's how you should contribute to repositories in this organization:

- Contact one of the repository owners to be added as a contributor.
- Open an issue in the repository describing the feature you intend to work on. Ex: "Add support for calling City Representatives".
- Check out a new branch for this feature from the repository's `development` branch. Ex: `git checkout -b call-city-reps`.
- Do your work on that branch.
- When your changes are ready to be merged, open a pull request from your feature branch to the repo's `development` branch.
- In the comments of your Pull Request, point out which issue you've resolved and how.

## In-depth fork and pull request walkthrough

If you want to contribute code to one of the projects, here's an in-depth guide for how to set up your fork and your local environment.

### Forking the repo

For example, if you want to work on the `general-congress-hotline` project, first visit its [page on GitHub](https://github.com/StayWokeOrg/general-congress-hotline), and click the "Fork" icon in the upper right of the page. This will create a fork of the project under your user account.

### Cloning it locally

Next, clone your local version down to your local machine.

```bash
git clone git@github.com:mattstauffer/general-congress-hotline.git
```

You now have a local representation of *your* fork.

### Keeping in sync with the source

In order to make it easy to keep your fork in sync with the original, add the original as a remote:

```bash
git remote add upstream https://github.com/StayWokeOrg/general-congress-hotline.git
```

You can now see that you have two "remotes" that your local repo is pointed towards: `origin`, which points to your repo, and `upstream`, which points to the original. We'll get to *why* in a bit.

### Spinning up a branch

Since you want to branch from the `development` branch, make sure you're on the `development` branch and it's up-to-date with the source repo. If you just forked it, it always will be--but if there have been a lot of changes to the original repo since you forked it, yours might be out of sync. Here's how to get yours in sync:

```bash
git checkout development
git fetch upstream
git merge upstream/development
git push origin development
```

Now you can spin up your new branch:

```bash
git checkout -b my-feature-name
```

Make your changes, commit them, and push up to your *local* repo for that branch:

```bash
touch new-file.text
git add new-file.txt
git commit -m "Added new-file.text"
git push origin my-feature-name
```

Now, you can create a PR in the GitHub user interface. Visit your repo and click the "New Pull Request" button, and you can create your PR from there.

Make sure to explain the purpose, context, and anything else necessary for reviewers to understand the PR. See GitHub's "[How to write the perfect pull request](https://github.com/blog/1943-how-to-write-the-perfect-pull-request)".
