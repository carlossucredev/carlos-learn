# Carlos Learn
Based on the **Hextra Starter Template.**
This repository contains the modifications made to the site (https://algosucreblog.netlify.app/),
a space dedicated to exploring ideas about programming, technology, critical thinking, and artificial intelligence.

You can check the original template repository for more information.
I accept pull requests, but avoid making massive changes: only small improvements or corrections are welcome.

## Local Development
### Prerequisites
**Recommended option**: Docker + Docker Compose
You can also install the dependencies manually if you prefer.
#### With Docker
 - Docker
 - Docker Compose
#### Local Installation (without Docker)
 - Hugo (extended version)
 - Go
 - Ruby
 - Git
### Using Docker
### 1. Clone the repository
```bash
git clone https://github.com/CarlosDanielSucre/algosucreblog.git
cd algosucreblog
```
#### 2. Start the development environment:

```bash
./scripts/dev.sh start
```
#### 3. Access the blog locally:
```bash
http://localhost:1313
```
#### Useful commands
```bash
./scripts/dev.sh logs           # View logs
./scripts/dev.sh stop           # Stop the environment
./scripts/dev.sh new-post       # Create a new post
./scripts/dev.sh generate-index # Generate post index
./scripts/dev.sh help           # Show all commands
```
### Local Installation (without Docker)
```bash
# Clone the repository
git clone https://github.com/carlossucredev/carlos-learn.git
cd carlos-learn

# Create new content
nvim content/2025/10/06/mi-post/index.md

# Generate index
cd content
./scripts/generate_index.rb

# Build the site
hugo

# Run local server
hugo server --logLevel debug --disableFastRender -p 1313
```
## How to Contribute
### 1. Fork and Clone
- Fork the repository
- Clone your fork locally
### 2. Set up your environment
- Use Docker (recommended) or install the dependencies locally
- Follow the instructions above
### 3. Make your changes
```
git checkout -b feature/new-functionality
# Make your modifications
./scripts/dev.sh start   # or hugo server to test locally
git commit -m "Add new functionality"
```
### 4. Create new posts

 **With Docker**:
```
./scripts/dev.sh new-post "Post Title"

```
 **Manual**:
```
mkdir -p content/2025/10/06/my-post
nvim content/2025/10/06/my-post/index.md
```

### 5. Post structure

```
---
title: "Post Title"
date: 2025-10-06T10:00:00-03:00
draft: false
description: "Brief description of the post"
tags: [programming, technology, artificial-intelligence]
categories: [analysis, opinion]
---
Content of the post here...
```

### 6. Submit Pull Request

```
git push origin feature/new-functionality
```
Then open a Pull Request on GitHub and clearly describe your changes.

### Project Structure
```
carlos-learn/
├── content/            # Posts and pages (Markdown)
├── layouts/            # HTML templates
├── assets/             # CSS, JS, images
├── hugo.yaml           # Hugo configuration
├── go.mod              # Go dependencies
├── scripts/            # Development scripts
├── Dockerfile          # Docker image
└── docker-compose.yml  # Docker orchestration
```
## Contribution Checklist

- [ ] I tested the changes locally (Docker or manual installation)
- [ ] I generated the index (./scripts/dev.sh generate-index)
- [ ] I verified that the site works correctly
- [ ] I followed the project conventions
- [ ] I documented any significant changes

## Contribution Guidelines

- Keep changes small and focused
- Always test before submitting
- Use descriptive commit messages
- Respect the style of existing code
- For large changes, open an issue first

## License

**License:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
This work is licensed under a **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License**.