# Running

To run the MkDocs site locally for development and testing purposes, follow these steps:

1. Open your terminal or command prompt and navigate to the root directory of your MkDocs project.

2. Run the following command to start the MkDocs development server:

```
mkdocs serve
```

This command will build the project's documentation site and start a local development server, typically at `http://localhost:8000`.

3. Open your web browser and visit `http://localhost:8000` to view the documentation site.

The MkDocs development server will automatically detect changes made to the project files and rebuild the site accordingly. You can continue editing your Markdown files or configuration settings, and the changes will be reflected in the browser upon saving the modified files.

4. To stop the development server, simply press `Ctrl+C` in the terminal or command prompt.

Note that the `mkdocs serve` command is primarily used for local development and testing purposes. When you're ready to deploy the documentation site to a hosting platform or a GitHub Pages repository, you'll need to use the `mkdocs build` command to generate the static HTML files, and then follow the deployment instructions specific to your hosting environment.
