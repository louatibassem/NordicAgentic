# NordicAgentic Website Deployment & Maintenance Manual

This guide explains how to upload your website to GoDaddy and how to add new blog posts in the future.

## 1. How to Upload to GoDaddy

Your website is built with **Static HTML**, which makes it very fast, secure, and easy to host. You do not need a database or PHP configuration.

### Prerequisites
- You need your GoDaddy account credentials.
- You need access to the **File Manager** (usually via cPanel or the Hosting Dashboard).

### Steps
1.  **Log in to GoDaddy** and navigate to your **My Products** page.
2.  Find your **Web Hosting** plan and click **Manage**.
3.  Open the **cPanel Admin** (or just **File Manager** directly if available).
4.  In the File Manager, navigate to the **`public_html`** folder. This is the root folder for your website.
    *   *Note: If you have existing files there (like a default "Coming Soon" page), you may want to delete them or move them to a backup folder.*
5.  **Upload the Files**:
    *   Click the **Upload** button.
    *   Select and upload the following files from your computer:
        - `index.html` (This is your Home/Blog page)
        - `contact.html`
        - `intune-ignite-2025.html`
        - `microsoft-365-intune-scale.html`
    *   **Upload the Assets**:
        - You need to upload the `assets` folder. In cPanel, you usually cannot upload a folder directly.
        - **Tip**: On your computer, right-click the `assets` folder and choose **Send to > Compressed (zipped) folder**. This creates `assets.zip`.
        - Upload `assets.zip` to `public_html`.
        - Right-click `assets.zip` in cPanel and choose **Extract**. This will create the `assets` folder with all your CSS and images.

6.  **Verify**:
    - Visit your domain name (e.g., `www.nordicagentic.com`). You should see your new site!

---

## 2. How to Manually Add a Blog Post

Since this is a static site, adding a post involves creating a new HTML file and linking to it from the homepage.

### Step 1: Create the New Post File
1.  On your computer, make a copy of an existing post file (e.g., copy `intune-ignite-2025.html`).
2.  Rename the copy to a URL-friendly name for your new post (e.g., `my-new-feature.html`).
3.  Open `my-new-feature.html` in a text editor (like Notepad, VS Code, or Sublime Text).
4.  **Update the Content**:
    - Change the `<title>` tag near the top.
    - Update the **Date** (`<div class="post-meta">...</div>`).
    - Update the **Main Heading** (`<h1>...</h1>`).
    - Update the **Image** (`<img src="...">`). *Make sure to put your new image in `assets/images/` first!*
    - Update the **Body Text** inside `<div class="post-content">`. You can use `<p>` for paragraphs, `<h3>` for subheadings, and `<ul><li>` for lists.
5.  Save the file.

### Step 2: Add the Post to the Homepage
1.  Open `index.html` in your text editor.
2.  Find the `<div class="blog-grid">` section.
3.  You will see blocks of code representing each post (starting with `<a href="...">` and ending with `</a>`).
4.  **Copy** the first block (the most recent post).
5.  **Paste** it right at the top of the `blog-grid` (so it appears first).
6.  **Update the Link**: Change `href="..."` to your new file (`my-new-feature.html`).
7.  **Update the Card Details**:
    - Change the Image Source (`src`).
    - Change the Date.
    - Change the Title.
    - Change the Excerpt (the short summary text).
8.  Save `index.html`.

### Step 3: Upload Changes
1.  Go back to GoDaddy File Manager.
2.  Upload your new file (`my-new-feature.html`).
3.  Upload the updated `index.html` (overwrite the old one).
4.  If you added a new image, upload it to the `assets/images` folder.

**Done!** Your new post is live.
