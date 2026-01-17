# Shubham Gogri - Portfolio

Personal portfolio website showcasing ML engineering projects, publications, and experience.

**Live Site:** [shubhamgogri.github.io](https://shubhamgogri.github.io)

## Tech Stack

- Jekyll static site generator
- Minimal Mistakes theme (remote)
- GitHub Pages hosting
- Custom SCSS styling

## Local Development

```bash
# Using Docker (recommended)
docker run --rm -v "$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll jekyll serve

# Or with Ruby installed
bundle install
bundle exec jekyll serve
```

Site will be available at `http://localhost:4000`

## Structure

```
_pages/         # Main pages (about, experience, projects, etc.)
_posts/         # Blog posts
_projects/      # Project collection
_includes/      # Custom template overrides
_sass/custom/   # Custom styling
assets/         # Images, CSS, documents
```

## License

Content and design by Shubham Gogri. Theme: [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes).
