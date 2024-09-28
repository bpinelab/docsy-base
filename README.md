# doc-base README

This repository is a template for documentation created using
[https://github.com/google/docsy-example](https://github.com/google/docsy-example).

The directory structure is as follows:

```bash
.
├── CONTRIBUTING.md
├── Dockerfile
├── LICENSE
├── README.md
├── .github/workflow
│   └── gh-pages.yml
├── assets
│   └── scss
├── config.yaml
├── content
│   ├── en
│   ├── fa
│   └── no
├── docker-compose.yaml
├── docsy.work
├── docsy.work.sum
├── go.mod
├── go.sum
├── hugo-disabled.toml
├── hugo.yaml
├── layoutst
├── netlify.toml
├── package-lock.json
├── package.json
├── public
└── resources
```

## Directory Structure and Description

### Root Level Files and Directories

- `CONTRIBUTING.md`: Contains guidelines for contributing to the project. Edit
  this file to update contribution guidelines.
- `Dockerfile`: Defines the Docker image for the project. Edit this file to
  change the Docker build configuration.
- `LICENSE`: Contains the license information for the project. Edit this file to
  update the licensing terms.
- `README.md`: Provides an overview of the project. Edit this file to update the
  project description and usage instructions.

### Directories and Their Contents

- `.github/workflow`: Configuration file for generating githab pages using
  Github Actions. Edit this file to change Github Actions workflow settings.

- `assets`

  - `scss`: Contains SCSS files for styling. Edit these files to update the
    project's styles.

- `config.yaml`: Configuration file for the project. Edit this file to change
  site-wide settings.

- `content`

  - `en`: Contains English content files. Edit these files to update the English
    documentation.
  - `fa`: Contains Farsi content files. Edit these files to update the Farsi
    documentation.
  - `no`: Contains Norwegian content files. Edit these files to update the
    Norwegian documentation.

- `docker-compose.yaml`: Defines services for Docker Compose. Edit this file to
  change the Docker Compose configuration.

- `docsy.work`: A file related to the Docsy theme. Typically, you don't need to
  edit this file directly.

- `docsy.work.sum`: A file related to the Docsy theme. Typically, you don't need
  to edit this file directly.

- `go.mod`: Defines the Go module for the project. Edit this file to manage Go
  dependencies.

- `go.sum`: Contains checksums for Go dependencies. This file is automatically
  updated when you run `go mod tidy` or `go get`.

- `hugo-disabled.toml`: A configuration file for Hugo. Edit this file to change
  Hugo settings if it's enabled.

- `hugo.yaml`: Another configuration file for Hugo. Edit this file to change
  Hugo settings.

- `layoutst`: Contains custom layouts for the site. Edit these files to change
  the site's layout.

- `netlify.toml`: Configuration file for Netlify. Edit this file to change
  Netlify deployment settings.

- `package-lock.json`: Automatically generated file that locks the versions of
  dependencies. This file is updated when you run `npm install`.

- `package.json`: Defines the Node.js dependencies and scripts for the project.
  Edit this file to manage Node.js dependencies and scripts.

- `public`: Contains the generated static site. Typically, you don't need to
  edit this directory directly.

- `resources`: Contains resource files for the project. Edit these files to
  update project resources.

For details on each directory and file, please refer to the comments and
documentation within each file.

## Publishing to GitHub Pages

To automatically publish this repository to GitHub Pages, follow these steps:

1. **Push the Repository to GitHub**:

- If you haven't already, push your local repository to GitHub.

  ```sh
  git remote add origin https://github.com/your-username/your-repository.git
  git push -u origin main
  ```

1. **Configure GitHub Pages**:

- Go to your repository on GitHub.
- Click on the `Settings` tab.
- Scroll down to the `Pages` section in the left sidebar.
- Under `Source`, select the branch you want to publish (`gh-pages`).
- Click `Save`.

1. **Verify Deployment**:

- After a few minutes, your site should be published at
  `https://your-username.github.io/your-repository/`.
- You can check the status of the deployment in the `Actions` tab of your
  repository.

1. **Custom Domain (Optional)**:

- If you want to use a custom domain, go to the `Pages` section in the
  `Settings` tab.
- Enter your custom domain and follow the instructions to configure your DNS
  settings.

By following these steps, your documentation will be automatically published to
GitHub Pages whenever you push changes to the specified branch.
