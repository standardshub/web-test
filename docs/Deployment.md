# Deployment

This document describes deployment process.

The site is hosted on AWS S3. S3 has a feature to publish static sites in
buckets. See [How do I configure an S3 Bucket for static website
hosting?](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/static-website-hosting.html)
for how it works.

The deployment process is implemented as GitHub Actions. See
[`.github/workflows`](../.github/workflows).

## Environments

There are two environments for the site:

- `dev`
- `production`

Each environment has its own S3 bucket. `mywebtest` for `dev`, and
`mywebprod` for `production`.

When a change is pushed to `dev` branch, the GitHub Actions will deploy the
change to `dev` environment.

When a change is pushed to `master` branch, the GitHub Actions will deploy the
change to `production` environment. Thus, the change will be published to the
production.
