# NanbyoData Public Data

[NanbyoData](https://nanbyodata.jp/) public content repository.

## Managed Content

- News
- Research activities
- FAQ
- News and research activity tags
- Team member information
- Team member images

## Directory Structure

```text
posts/                  News source files
research-activities/    Research activity source files
static/data/
  news.json              Generated news data
  research-activities.json  Generated research activity data
  tags.json              Tag configuration
  faq.json               FAQ
  members.json           Team member information
static/img/members/      Team member images
scripts/                 JSON generation scripts
.github/workflows/       GitHub Actions
```

## Branching Workflow

- `dev`: For testing in the development environment
- `main`: For the production environment

As a general rule, apply changes to the `dev` branch first and verify them. Then, create a pull request and merge the changes into `main`.

## Updating Content

### News

Edit the Markdown files in `posts/ja/` and `posts/en/`.

When changes are pushed, GitHub Actions automatically generates `static/data/news.json`.

### Research activities

Edit the Markdown files in `research-activities/ja/` and `research-activities/en/`.

When changes are pushed, GitHub Actions automatically generates `static/data/research-activities.json`.

### FAQ

Edit `static/data/faq.json` directly.

### Tags

Edit `static/data/tags.json` directly.

### Team Information

- Member information: `static/data/members.json`
- Member images: `static/img/members/`

For `image_name` in `members.json`, specify the filename of the image placed in `static/img/members/`.

## Important Notes

- Do not edit `news.json` or `research-activities.json` directly because they are generated automatically.
- The contents of this repository are public. Do not commit files containing confidential or personal information.
- Verify how the content is displayed in the development environment before deploying it to production.
