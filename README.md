Creating a static travel blog website using Jekyll in IBM Cloud involves several steps. Jekyll is a popular static site generator that can help you create a simple and efficient website. Here's a step-by-step guide on how to do it:

## Step 1: Set up your IBM Cloud Account

If you don't already have an IBM Cloud account, you'll need to sign up for one. Go to the IBM Cloud website and follow the instructions to create an account.

**Step 2: Install Jekyll**

Before you start creating your travel blog website, you need to have Jekyll installed on your local machine. You can install Jekyll using RubyGems by running the following command in your terminal:

```bash
gem install jekyll bundler
```

**Step 3: Create a New Jekyll Project**

Once Jekyll is installed, you can create a new Jekyll project for your travel blog. Navigate to the directory where you want to create your project and run the following command:

```bash
jekyll new mytravelblog
```

Replace `mytravelblog` with the name of your project.

**Step 4: Customize Your Blog**

You can customize your blog by editing the configuration file (`_config.yml`) and the templates in the `_layouts` and `_includes` directories. You can also add your own CSS styles and images to the project.

**Step 5: Add Blog Posts**

To add blog posts, create Markdown (.md) files in the `_posts` directory. Each file should have a filename in the format `YYYY-MM-DD-title.md`, and it should contain the content of your blog post in Markdown format.

**Step 6: Test Your Website Locally**

You can test your website locally by running the following command in your project directory:

```bash
bundle exec jekyll serve
```

This will start a local web server, and you can preview your website by opening a web browser and navigating to `http://localhost:4000`.

**Step 7: Set Up IBM Cloud**

Before deploying your website, you'll need to set up an IBM Cloud environment. If you haven't already, you can create a space in IBM Cloud and set up the Cloud Foundry CLI for deployment.

**Step 8: Deploy Your Website to IBM Cloud**

To deploy your Jekyll website to IBM Cloud, follow these steps:

1. Build your website using Jekyll by running the following command:

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

2. Log in to IBM Cloud using the Cloud Foundry CLI by running:

```bash
cf login
```

3. Push your website to IBM Cloud by running:

```bash
cf push mytravelblog -b staticfile_buildpack
```

Replace `mytravelblog` with your desired app name.

**Step 9: Access Your Live Website**

Once your website is successfully deployed, you can access it using the URL provided by IBM Cloud. Your travel blog is now live and accessible to the world.

**Step 10: Update Your Blog**

You can continue to update your blog by adding new posts or making changes to the site's content and layout. Remember to rebuild and redeploy your website when you make changes to see them reflected on the live site.

That's a high-level overview of creating a static travel blog website using Jekyll in IBM Cloud. Be sure to refer to the official Jekyll and IBM Cloud documentation for more detailed information and troubleshooting.