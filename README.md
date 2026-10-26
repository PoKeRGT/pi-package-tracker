# Pi Package Tracker

A GitHub Actions workflow that monitors newly created TypeScript repositories for Pi packages.

## What it does

Every day at 08:00 UTC, the workflow:

1. Searches GitHub for repositories created during the previous day that mention `pi-package`.
2. Checks each repository's root `package.json`.
3. Keeps repositories whose `keywords` array includes `pi-package`.
4. Creates a GitHub issue listing the verified packages.

No issue is created when no matching packages are found.

## Running manually

Open the repository's **Actions** tab, select **Daily Pi Packages Monitor**, and choose **Run workflow**.

The workflow requires permission to read repository contents and create issues.
