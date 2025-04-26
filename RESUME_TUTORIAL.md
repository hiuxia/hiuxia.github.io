# Resume Website Building Tutorial

This tutorial will guide you through understanding, customizing, and deploying the resume website you've cloned.

## 1. Project Composition

This resume project is based on Jekyll, a static site generator that transforms plain text into static websites. Here's the structure:

- **_config.yml**: Configuration file for the Jekyll site
- **index.md**: Main content of your resume/portfolio
- **_layouts/**: Contains HTML templates (default.html) that define the site structure
- **_sass/**: Contains SCSS files for styling
- **css/**: Contains the main SCSS file that imports styles from _sass
- **Gemfile & Gemfile.lock**: Ruby dependency management files
- **resume.pdf**: Your resume in PDF format
- **_site/**: Generated static website files (created when building)

## 2. Function of Each Component

### Key Files and Directories

- **_config.yml**: Controls site-wide settings including:
  - Personal information (name, social links)
  - Site title and URL
  - Navigation menu items
  - Footer settings

- **index.md**: The main content file written in Markdown with YAML front matter. Contains:
  - Your personal information
  - Academic/professional background
  - Publications
  - Teaching experience
  - Service activities
  - Awards and honors

- **_layouts/default.html**: The HTML template that defines the structure of your page, including:
  - Header and navigation
  - Content section that displays your markdown content
  - Footer

- **_sass/**: Contains modular SCSS files for styling:
  - **_style.scss**: Main styling rules
  - **icons.scss**: CSS for social media icons
  - **tables.scss**: Table formatting
  - **typography.scss**: Text styling
  - **vars.scss**: Color and size variables

- **resume.pdf**: PDF version of your resume that visitors can download

- **Gemfile**: Lists the Ruby gems (dependencies) needed for the Jekyll site

## 3. How to Modify for Personal Use

### Basic Customization

1. **Edit _config.yml**:
   - Change `title` to your name
   - Update `url` to your GitHub Pages URL
   - Modify `author` with your name
   - Update social media links (GitHub, LinkedIn, etc.)
   - Edit navigation items as needed

2. **Update index.md**:
   - Replace personal information (name, position, institution, email)
   - Update your bio in the "About Me" section
   - Add your own publications, teaching experience, etc.
   - Maintain the Markdown formatting (headings with ##, lists with -)

3. **Replace resume.pdf**:
   - Add your own PDF resume (keep the same filename or update the link in _config.yml)

### Advanced Customization

1. **Modify the Layout**:
   - Edit `_layouts/default.html` to change the page structure
   - Add new sections or modify existing ones

2. **Customize Styling**:
   - Edit files in `_sass/` to change colors, fonts, spacing, etc.
   - The main styling is in `_style.scss`
   - Color variables are in `vars.scss`

3. **Add New Pages**:
   - Create new .md files in the root directory
   - Include YAML front matter at the top of each file:
     ```
     ---
     layout: default
     ---
     ```

## 4. Deploying to GitHub Pages

1. **Create a GitHub Repository**:
   - Create a new repository named `yourusername.github.io`
   - This specific name is required for your user GitHub Pages site

2. **Push Your Code**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/yourusername/yourusername.github.io.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Navigate to Settings > Pages
   - Under "Source", select "main" branch
   - Click Save

4. **Wait for Deployment**:
   - GitHub will automatically build and deploy your site
   - It usually takes a few minutes
   - You can check the status in the GitHub Pages section of repository settings

5. **Access Your Site**:
   - Your site will be available at `https://yourusername.github.io`

### Troubleshooting Deployment

If your site doesn't appear or looks incorrect:

1. Check the GitHub Actions tab for any build errors
2. Make sure your repository is named exactly `yourusername.github.io`
3. Verify that GitHub Pages is enabled in repository settings
4. Ensure your `_config.yml` has the correct URL

## Local Development

To preview changes before pushing to GitHub:

1. Install Ruby and Jekyll:
   ```bash
   # macOS (using Homebrew)
   brew install ruby
   gem install bundler jekyll
   ```

2. Run the site locally:
   ```bash
   cd yourusername.github.io
   bundle install
   bundle exec jekyll serve
   ```

3. View your site at `http://localhost:4000`

This allows you to make changes and see them instantly before deploying.

## Tips for Maintaining Your Resume Site

- Regularly update your publications and experiences
- Keep your PDF resume in sync with the website content
- Consider adding project pages or a blog section as your career progresses
- Use branches for testing major changes before deploying to main 