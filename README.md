# Hissain.github.io

Personal portfolio and technical blog of Sazzad Hissain Khan, built with **Jekyll** and **Decap CMS**.

## 🚀 Running Locally

To test the site on your machine before pushing:

### 1. Prerequisites
- **Ruby** (version 2.7 or higher)
- **Bundler** (`gem install bundler`)

### 2. Install Dependencies
Run this once to install the required Ruby gems (Jekyll, etc.):
```bash
bundle install
```

### 3. Start the Server
Run this command to start the local server:
```bash
bundle exec jekyll serve
```

Access the site at: `http://localhost:4000`

## ✍️ Content Management

- **Admin Panel**: To test the CMS locally, you need [npx](https://nodejs.org/en/) installed.
  ```bash
  npx decap-server
  ```
  Then visit `http://localhost:4000/admin`.

- **Manual**: Create files in `_posts/` with the format `YYYY-MM-DD-title.md`.

## 🛠️ Deployment

Simply push to the `main` branch. GitHub Pages will build and deploy the site automatically.
