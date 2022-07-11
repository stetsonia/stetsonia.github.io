
 https://squidfunk.github.io/mkdocs-material/getting-started/
 https://squidfunk.github.io/mkdocs-material/customization/ 

 ----------------------------------------------------------------------------
 
 Browse to: https://stetsonia.github.io/

 ----------------------------------------------------------------------------
 
 # Create virtual environment in current directory
 f:
 mkdir mkdocs
 cd mkdocs
 where python3
 python3 -m virtualenv venv
 
 # Active virtual environment
 "./venv/Scripts/activate.bat"
 
 # Install mkdocs-material
 pip install mkdocs-material

 # Go to the directory where you want your project to be located and enter:
 mkdocs new .
 
  .
  ├─ docs/
  │  └─ index.md
  └─ mkdocs.yml
 
 # Simply add the following lines to mkdocs.yml to enable the theme. 
 theme:
  name: material
 
 # Install language support for VS code 
 https://squidfunk.github.io/mkdocs-material/creating-your-site/#minimal-configuration  
 
 # MkDocs includes a live preview server, so you can preview your changes as you write your documentation. 
 # The server will automatically rebuild the site upon saving. 
 # Start it with:
 mkdocs serve
 
 # If you're only interested in the current page, the --dirtyreload flag will make rebuilds much faster:
 mkdocs serve --dirtyreload
 
 Browse http://127.0.0.1:8000/
 
 # Advanced configurations
 # https://squidfunk.github.io/mkdocs-material/creating-your-site/#minimal-configuration
 Changing the colors
 Changing the fonts
 Changing the language
 Changing the logo and icons
 Ensuring data privacy
 Setting up navigation
 Setting up site search
 Setting up site analytics
 Setting up social cards
 Setting up tags
 Setting up versioning
 Setting up the header
 Setting up the footer
 Adding a git repository
 Adding a comment system
 Building for offline usage

 # Supported Markdown extensions that are natively integrated with Material for MkDocs
 https://squidfunk.github.io/mkdocs-material/setup/extensions/
 
 # When you're finished editing, you can build a static site from your Markdown files with:
 mkdocs build
 
 The contents of this directory make up your project documentation. 
 There's no need for operating a database or server, as it is completely self-contained. 
 The site can be hosted on GitHub Pages, GitLab Pages, a CDN of your choice or your private web space.

 # Github Pages 
 https://pages.github.com/
 
 # Create in your github account a new repository: username.github.io
 
 f:\mkdocs
 git init
 git add --all
 git commit -m "Initial commit"
 git branch -M main
 git remote add origin https://github.com/stetsonia/stetsonia.github.io.git
 git push -u origin main
 
 # Goto settings / Pages / Source and select 'gh-pages' as your branch
 
 Browse to: https://stetsonia.github.io/
 
 # If you prefer to deploy your project documentation manually, you can just invoke the 
 # following command from the directory containing the mkdocs.yml file:
 mkdocs gh-deploy --force
 
 -----------------
 
 Publish the site to Github Pages
 
 # Clone the repository
 git clone https://github.com/username/username.github.io
 
 # Create a file
 cd username.github.io
 echo "Hello World" > index.html
 
 # Push it
 git add --all
 git commit -m "Initial commit"
 git push -u origin main
 
 https://username.github.io.
 
 -----------------------------------------------------------------------------

 Commands
 
 mkdocs new [dir-name]  - Create a new project.
 mkdocs serve           - Start the live-reloading docs server.
 mkdocs build           - Build the documentation site.
 mkdocs -h              - Print help message and exit.

 -----------------------------------------------------------------------------
 
 mkdocs with Docker
 
 # Install mkdocs-material with Docker
 docker pull squidfunk/mkdocs-material
 
 # Start mkdocs 
 docker run --rm -it -v "%cd%":/docs squidfunk/mkdocs-material new .
 
 