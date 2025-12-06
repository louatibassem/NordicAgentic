# NordicAgentic Blog

A lightweight, premium PHP blog designed for easy hosting and updates.

## Structure
- **`index.php`**: Homepage. Lists all posts from the `posts/` directory.
- **`post.php`**: Displays a single blog post.
- **`contact.php`**: Contact information page.
- **`posts/`**: Directory containing blog posts as JSON files.
- **`assets/`**: CSS styles and Images.
- **`includes/`**: Reusable header and footer files.

## How to Add a New Blog Post
1. Create a new `.json` file in the `posts/` folder.
   - Naming convention: `YYYY-MM-DD-your-title.json` (e.g., `2025-12-01-new-ai-features.json`).
2. Copy the following template into the file:
   ```json
   {
       "title": "Your Blog Title Here",
       "date": "2025-12-01",
       "image": "assets/images/your-image.jpg",
       "excerpt": "A short summary of the post that appears on the homepage.",
       "content": "<p>Your main content goes here. You can use HTML tags like <b>bold</b>, <i>italic</i>, and lists.</p>"
   }
   ```
3. Upload any images used to `assets/images/`.
4. The new post will automatically appear on the homepage!

## Hosting on GoDaddy
1. Upload all files and folders to your `public_html` directory using GoDaddy's File Manager or FTP.
2. Ensure your domain points to this directory.
3. No database configuration is required.
