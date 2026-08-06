<p align="center">
  <a href="https://sabrinacardoso.com">
    <img
      src="https://raw.githubusercontent.com/marinellibr/portfolio-sabrina-resources/refs/heads/main/images/header-logo.png"
      alt="Portfolio Sabrina"
    />
  </a>
</p>

<h1 align="center">
Portfolio Sabrina — Resources
</h1>

<p align="center">

![GitHub](https://img.shields.io/badge/GitHub-Repository-black?logo=github)
![Assets](https://img.shields.io/badge/Static-Assets-blue)
![Images](https://img.shields.io/badge/Images-Versioned-success)
![Media](https://img.shields.io/badge/Media-Library-orange)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

</p>

---

## Overview

**Portfolio Sabrina Resources** is the centralized media repository used by the Portfolio Sabrina platform.

Instead of storing images and downloadable files directly inside the frontend application, all static resources are versioned independently inside this repository.

This approach keeps application bundles smaller, simplifies editorial workflows and allows content updates without requiring frontend changes.

The repository acts as the platform's media library.

---

# Live Application

Website

https://sabrinacardoso.com

Frontend

https://github.com/marinellibr/portfolio-sabrina-frontend

Backend

https://github.com/marinellibr/portfolio-sabrina-backend

---

# Purpose

This repository stores:

- Project images
- Mockups
- Banners
- Drawings
- Curriculum files
- Social sharing images
- Logos
- Future downloadable resources

The repository intentionally contains **no application logic**.

Its responsibility is limited to versioning and distributing media assets consumed by the frontend and backend.

---

# Architecture

```text
                Portfolio Platform

        ┌────────────────────────────┐
        │ Angular Frontend           │
        └─────────────┬──────────────┘
                      │
                      │ requests images
                      ▼
        ┌────────────────────────────┐
        │ Resources Repository       │
        │                            │
        │ Images                     │
        │ Documents                  │
        │ Mockups                    │
        │ Logos                      │
        │ Curriculum                 │
        └────────────────────────────┘
```

---

# Repository Structure

```text
images/

banner.png

header-logo.png

projects/

creamy/

itau/

...

curriculum/

curriculum-pt.pdf

curriculum-en.pdf

social/

open-graph.png

twitter-card.png

logos/

...
```

---

# Why a Separate Repository?

Keeping assets outside the frontend provides several advantages.

### Independent Releases

Images can be updated without rebuilding the Angular application.

### Smaller Bundles

Large media files are not included inside the frontend build.

### Better Version Control

Every asset change becomes a Git commit.

### Editorial Workflow

Designers and content editors can update resources without modifying application code.

### Cleaner Source Tree

Frontend repositories remain focused on source code rather than binary assets.

---

# Integration

The frontend consumes these assets dynamically.

Typical use cases include:

- Project galleries
- Hero banners
- Portfolio cards
- Resume downloads
- Social preview images

The backend also references this repository when resolving downloadable resources such as multilingual curriculum files.

---

# Asset Guidelines

Recommended formats

Images

- PNG
- SVG
- WebP

Documents

- PDF

Avoid

- PSD
- AI
- ZIP
- Large uncompressed images

Images should be optimized before being committed.

---

# Naming Convention

Examples

```text
banner-home.png

header-logo.png

project-creamy-cover.png

project-creamy-gallery-01.png

curriculum-en.pdf

curriculum-pt.pdf
```

Avoid

```text
IMG001.png

Screenshot (12).png

final-final.png

new-image.png
```

Consistent naming simplifies maintenance and automated lookup.

---

# Best Practices

- Prefer WebP whenever possible.
- Keep original editable files outside this repository.
- Avoid duplicate images.
- Optimize image dimensions before upload.
- Use descriptive filenames.
- Group assets by project.
- Keep social images separated.
- Maintain multilingual documents together.

---

# Future Improvements

- Automatic image optimization
- CDN integration
- Thumbnail generation
- Asset metadata
- Image manifests
- Integrity verification
- Responsive image variants
- Asset indexing

---

# Related Projects

Frontend

https://github.com/marinellibr/portfolio-sabrina-frontend

Backend

https://github.com/marinellibr/portfolio-sabrina-backend

---

# Author

**Luiz Marinelli**

Senior Frontend Engineer

GitHub

https://github.com/marinellibr

LinkedIn

https://linkedin.com/in/luizmarinelli

---

This repository is part of the **Portfolio Sabrina Platform**, where frontend, backend and static resources evolve independently while remaining fully integrated through a shared architecture.
