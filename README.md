# Joltin' Joe's Hot Sauce - GitHub Pages Site

A Jekyll-based static site for hosting on GitHub Pages for free.

## Quick Start - Deploy to GitHub Pages

### Method 1: Using GitHub Website (Easiest)

1. **Create a new repository on GitHub:**
   - Go to https://github.com/new
   - Name it `yourusername.github.io` (replace `yourusername` with your actual GitHub username)
   - Make it public
   - Don't initialize with README (we already have files)

2. **Upload your files:**
   - Click "uploading an existing file"
   - Drag and drop ALL the files from this folder
   - Commit the changes

3. **Enable GitHub Pages:**
   - Go to your repository Settings → Pages
   - Under "Source", select "Deploy from a branch"
   - Select the `main` branch and `/ (root)` folder
   - Click Save

4. **Wait a few minutes** and your site will be live at `https://yourusername.github.io`

### Method 2: Using Git Command Line

```bash
# Initialize git in this directory
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit"

# Add your GitHub repository as remote (replace with your URL)
git remote add origin https://github.com/yourusername/yourusername.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Then enable GitHub Pages in repository Settings → Pages.

## Customizing Your Site

### Update Site Information

Edit `_config.yml` and change:
- `title`: Your site name
- `email`: Your email address
- `description`: Site description
- `url`: Your GitHub Pages URL (e.g., `https://yourusername.github.io`)

**Important:** After editing `_config.yml`, you must restart Jekyll if testing locally.

### Add Your Content

1. **Homepage:** Edit `index.md`
2. **About Page:** Edit `about.md`
3. **Blog Posts:** Add files to `_posts/` folder

### Creating Blog Posts

Create a new file in `_posts/` with this format: `YYYY-MM-DD-title.md`

Example: `2026-02-14-my-hot-sauce-journey.md`

```markdown
---
layout: post
title: "My Hot Sauce Journey"
date: 2026-02-14
categories: story
---

Your content here...
```

### Adding Images

1. Put images in `assets/images/`
2. Reference them in your markdown:

```markdown
![Alt text](/assets/images/your-image.jpg)
```

### Customize Colors/Styling

Edit `assets/css/style.css` to change colors, fonts, and layout. The current theme uses red (#d32f2f) for hot sauce branding.

## Testing Locally (Optional)

If you want to preview your site before pushing to GitHub:

### Install Jekyll

**On Mac/Linux:**
```bash
# Install Ruby (if not installed)
# Then install Jekyll
gem install bundler jekyll

# Install dependencies
bundle install

# Serve the site
bundle exec jekyll serve
```

**On Windows:**
- Download Ruby from https://rubyinstaller.org/
- Install Jekyll: `gem install bundler jekyll`
- Run: `bundle install` then `bundle exec jekyll serve`

Visit `http://localhost:4000` to see your site.

## Project Structure

```
.
├── _config.yml          # Site configuration
├── _layouts/            # HTML templates
│   ├── default.html     # Main layout
│   └── post.html        # Blog post layout
├── _posts/              # Blog posts
│   └── 2026-02-13-welcome.md
├── assets/
│   ├── css/
│   │   └── style.css    # Styles
│   └── images/          # Put images here
├── index.md             # Homepage
├── about.md             # About page
├── blog.md              # Blog listing page
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Adding More Pages

Create a new `.md` file in the root directory:

```markdown
---
layout: default
title: Products
permalink: /products/
---

# Our Products

Your content here...
```

## Troubleshooting

**Site not updating?**
- Changes can take 1-2 minutes to appear
- Check the Actions tab in GitHub for build errors
- Make sure you pushed your changes to the `main` branch

**404 Error?**
- Verify GitHub Pages is enabled in Settings
- Check that your repository is named correctly
- Wait a few minutes after first deployment

**Styles not loading?**
- Check that `_config.yml` has the correct `baseurl` and `url`
- Clear your browser cache

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)

## Support

For issues with this template, check:
- GitHub Pages status: https://www.githubstatus.com/
- Jekyll documentation: https://jekyllrb.com/

---

**Next Steps:**
1. Update `_config.yml` with your information
2. Edit the content in `index.md`, `about.md`, and blog posts
3. Add your images to `assets/images/`
4. Push to GitHub and enable GitHub Pages
5. Your site will be live for free! 🌶️
