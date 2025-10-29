# The Devigner Blog

Welcome to The Devigner Blog! This is where code and design come together. We share practical tips, tutorials, and inspiration for people who love both.

## Features

- **Jekyll Static Site Generator**: Fast, secure, and SEO-friendly blog
- **Decap CMS Integration**: User-friendly content management system for easy blog post creation
- **Responsive Design**: Mobile-friendly layout that works on all devices
- **Clean & Modern UI**: Professional design with custom styling
- **SEO Optimized**: Built-in SEO tags and sitemap generation
- **RSS Feed**: Automatic feed generation for subscribers

## Getting Started

### Prerequisites

- Ruby 3.0 or higher
- Bundler gem

### Installation

1. Clone this repository:
```bash
git clone https://github.com/ThangChiDoan/the-devigner-blog.github.io.git
cd the-devigner-blog.github.io
```

2. Install dependencies:
```bash
bundle install
```

3. Run the development server:
```bash
bundle exec jekyll serve
```

4. Open your browser and navigate to `http://localhost:4000`

## Using Decap CMS

### Accessing the Admin Panel

Once the site is deployed, you can access the Decap CMS admin panel at:
```
https://your-domain.com/admin/
```

### Authentication Setup

To use Decap CMS in production, you'll need to set up authentication:

1. **For GitHub Pages with GitHub Backend:**
   - Uncomment the GitHub backend configuration in `/admin/config.yml`
   - Set up OAuth authentication following [Decap CMS GitHub Backend Guide](https://decapcms.org/docs/github-backend/)

2. **For Netlify with Git Gateway:**
   - Deploy your site to Netlify
   - Enable Identity and Git Gateway in Netlify dashboard
   - The default configuration is already set up for this

### Creating Blog Posts

1. Log in to the admin panel at `/admin/`
2. Click on "Blog Posts" collection
3. Click "New Blog Post"
4. Fill in the post details:
   - Title
   - Publish Date
   - Author
   - Tags
   - Content
5. Click "Publish" to create the post

## Project Structure

```
.
├── _config.yml          # Jekyll configuration
├── _layouts/            # Page layouts
│   ├── default.html     # Default layout with header/footer
│   └── post.html        # Blog post layout
├── _posts/              # Blog posts (Markdown files)
├── admin/               # Decap CMS admin panel
│   ├── config.yml       # CMS configuration
│   └── index.html       # Admin interface
├── assets/              # Static assets
│   └── css/
│       └── style.css    # Custom styles
├── about.md             # About page
├── blog.html            # Blog listing page
├── index.html           # Homepage
├── Gemfile              # Ruby dependencies
└── .gitignore           # Git ignore rules
```

## Customization

### Updating Site Information

Edit `_config.yml` to update:
- Site title and description
- Contact email
- Social media usernames
- URL and baseurl

### Styling

Customize the look and feel by editing:
- `/assets/css/style.css` - Main stylesheet
- `/_layouts/*.html` - Page layouts

### Adding Pages

Create new pages by adding HTML or Markdown files in the root directory with front matter:

```yaml
---
layout: default
title: Your Page Title
permalink: /your-page/
---

Your content here...
```

## Deployment

### GitHub Pages

1. Push your code to a GitHub repository
2. Go to repository Settings > Pages
3. Set source to the main branch
4. Your site will be available at `https://username.github.io/repository-name/`

### Netlify

1. Connect your GitHub repository to Netlify
2. Set build command to: `bundle exec jekyll build`
3. Set publish directory to: `_site`
4. Deploy!

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests.

## License

This project is open source and available under the MIT License.

