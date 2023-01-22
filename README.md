# Markdown and MkDocs

Generate html site with documentation in Markdown

## Getting started

Enter into site: https://squidfunk.github.io/mkdocs-material/ and execute the Getting started or execute the next steps:

>Prerequisites: `Python` and `pip` installed  

1. Install MkDocs, mkdocs-material, and languages package
```
pip install mkdocs
pip install mkdocs-material
pip install mkdocs[i18n]
```
2. Create your site with mkdocs-material
```
python -m mkdocs new <name_site>
```
3. in `mkdocs.yml` paste:
```
theme:
  name: material
```
4. Execute the command in te path of `mkdocs.yml` for open the site:
```
python -m mkdocs serve
```
5. Build 
```
python -m mkdocs build
```
> Open the browser in: `http://localhost:8000/`

The before steps create the next structure:
```
 mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
```

-----------------------------

## Personalize the site:

For initialize, paste the next code into `mkdocs.yml`:
```yml
# Project information
site_name: Example_doc
site_url: https://github.com/xlavm/Markdown
site_author: Luis Angel Vanegas Martinez
site_description: >-
  Create a documentation of example

# Repository
repo_name: xlavm/Markdown
repo_url: https://github.com/xlavm/Markdown
edit_uri: ""

# Copyright
copyright: Copyright &copy; 2021 LAVM

# Customization
extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/xlavm
    - icon: fontawesome/brands/gitlab
      link: https://gitlab.com/xlavm
    - icon: fontawesome/brands/docker
      link: https://hub.docker.com/u/xlavm
    - icon: fontawesome/brands/facebook
      link: https://www.facebook.com/xlavm1/
    - icon: fontawesome/brands/linkedin
      link: https://linkedin.com/in/squidfunk/
    - icon: fontawesome/brands/youtube
      link: https://www.youtube.com/channel/UCsFxicrm7ysiQk9jZ2WZNtg?view_as=subscriber
    - icon: fontawesome/brands/instagram
      link: https://instagram.com/squidfunk

theme:
  name: material
  language: en
  features:
    - navigation.tabs
    - navigation.sections
``` 
-------------------------
## Structure of site in Markdown
```
mkdocs.yml                          # The configuration file
    docs/                           # Principal folder
        index.md                    # homepage and nav 1
        Menu 2/                     # nav 2 and section 1
            contenido 2/            # section 2 
```
