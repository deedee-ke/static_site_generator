# Static Site Generator

A lightweight static site generator built in Bash that converts Markdown files to HTML. Perfect for creating simple blogs and documentation sites.

## Features

- Convert Markdown to HTML
- Template-based page generation
- Support for metadata in content files
- Automatic index page generation
- File watching for development
- Simple deployment process

## Project Structure

```
.
├── content/        # Markdown content files
├── src/            # Source scripts
├── static/         # Static assets (CSS, images)
├── template.html   # HTML template
├── main.sh         # Main script
└── test.sh         # Test script
```

## Prerequisites

- Bash (4.0 or higher)
- `pandoc`
- `inotify-tools` (for file watching)
- `rsync` (for deployment)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/deedee-ke/static_site_generator.git
   cd static_site_generator
   ```

2. Install dependencies:

   - **For Ubuntu/Debian:**
     ```bash
     sudo apt-get install pandoc inotify-tools rsync
     ```
   - **For macOS:**
     ```bash
     brew install pandoc fswatch rsync
     ```

## Usage

### Basic Usage

Generate your site:

```bash
./main.sh build
```

Watch for changes during development:

```bash
./main.sh watch
```

### Content Creation

Add Markdown files to the `content/` directory:

```markdown
---
title: My First Post
date: 2023-12-01
---

# Hello World

This is my first blog post.
```

### Customization

Edit `template.html` to change the site's layout:

```html
<!DOCTYPE html>
<html>
<head>
    <title>{{title}}</title>
</head>
<body>
    {{content}}
</body>
</html>
```

## Testing

Run the test suite:

```bash
./test.sh
```

## Contributing

1. Fork the repository.
2. Create your feature branch:
   ```bash
   git checkout -b feature/awesome-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add some awesome feature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature/awesome-feature
   ```
5. Open a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

## Acknowledgments

- Boot.dev for project inspiration
- Contributors and maintainers
