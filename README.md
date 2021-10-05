# LeDataSciFi-2022

This repo is the 2022 edition of LeDataSciFi. The [ledatascifi.github.io](https://ledatascifi.github.io) repo hosts the website, but simply redirects to the cover page for _**this**_ repo. In future years, make a new years' website as a new repo by cloning this one (don't forget the GH action that deploys it!), and alter the redirect from the ledatascifi.github.io to the new website. 

- Greatly simplified course/website structure - now everything is in one book (this repo!), which can be ported from year to year with simpler updates. The only portion of class _**outside**_ this repo is
    - the org's has teams for discussion and many repos for assignments, etc
    - coursesite to send out assignment links, Zoom links, and schedule office hours appointments from within the Lehigh "gates"
    - the schedule and weekly tasks that are embedded in the dashboard page are an excel file on my computer
- Now using `jupyter-book` 0.8.3 instead of 0.6.4, which are incompatible.
    - **As of fall 2021, `jupyter-book` is on 0.11. This might change a lot of behavior. 😨**
- To build the book for _**local**_ viewing (quicker dev cycles than waiting for website to refresh):
    - `cd <>/ledatascifi-2022` 
    - (Recommended) Remove the existing `LeDataSciFi-2022/_build/` directory
    - `jupyter-book build ./`
    - A fully-rendered HTML version of the book will be built in the `_build/html/` folder.
- To update website: Simply push or pull the main branch of the repo. A GitHub actions workflow (`.github/workflows/deploy.yml`) automatically builds and pushes the book in the `gh-pages` branch, and GitHub pages will update the website in <5 minutes. 
- Book formatting is controlled by
    - `_config.yml` for most settings
    - `_toc.yml` lays out the book table of contents, ie the left nav bar
    - `_static/*` - any css or js I want to add to modify the base styling goes here

## Credits

This project is created using the excellent open source [Jupyter Book project](https://jupyterbook.org/) and the [executablebooks/cookiecutter-jupyter-book template](https://github.com/executablebooks/cookiecutter-jupyter-book).


