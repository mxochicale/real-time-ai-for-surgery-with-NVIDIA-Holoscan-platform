# Setting up slides in quarto and github
The following are few steps to setup your quarto slides in github pages.

*  Create templates, ci workflows and adds code of conduct
```
.
├── CODE_OF_CONDUCT.md
├── ISSUE_TEMPLATE
│   ├── bug_report.md
│   ├── feature_request.md
│   └── not_working.md
├── pull_request_template.md
└── workflows
    └── publish-quarto.yml

2 directories, 6 files
```

* Create scalfolding project in the main branch

```
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── slides
    ├── _extensions
    │   └── quarto-ext
    │       └── fontawesome
    │           ├── assets
    │           │   ├── css
    │           │   │   └── all.css
    │           │   └── webfonts
    │           │       ├── fa-brands-400.ttf
    │           │       ├── fa-brands-400.woff2
    │           │       ├── fa-regular-400.ttf
    │           │       ├── fa-regular-400.woff2
    │           │       ├── fa-solid-900.ttf
    │           │       ├── fa-solid-900.woff2
    │           │       ├── fa-v4compatibility.ttf
    │           │       └── fa-v4compatibility.woff2
    │           ├── _extension.yml
    │           └── fontawesome.lua
    ├── favicon.svg
    ├── figures
    │   └── 00_template-vector-images
    │       ├── Makefile
    │       ├── outputs
    │       │   └── README.md
    │       ├── README.md
    │       ├── references
    │       │   └── README.md
    │       └── vectors
    │           └── drawing-v00.svg
    ├── index.qmd
    ├── _quarto.yml
    └── README.md
```


* first commit
```
git add .
git commit -m ':fire: 1st commit: adds scalfolding for slides #0'
git branch -M main
git push -u origin main
```

* Create gh-pages branch
```
git checkout --orphan gh-pages 
#An orphan branch is not connected to the other branches and commits, and its working tree has no files at all. 
#See [here](https://git-scm.com/docs/git-checkout) for more info.
git reset --hard
git commit --allow-empty -m "Initializing gh-pages branch"
git push origin gh-pages
git checkout main
#https://jiafulow.github.io/blog/2020/07/09/create-gh-pages-branch-in-existing-repo/
```

* Settting up gh-pages
    * Go to [settings/pages](https://github.com/mxochicale/real-time-ai-for-surgery-with-NVIDIA-Holoscan-platform/settings/pages)
    * In `Build and deployment` go to Branch and select gh-pages: `/(root)` and click `SAVE`

* Commiting and pushing changes
```
git add .
git commit -m 'add message with CI to deply gh-pages #ISSUE_NUMBER'
git push origin main
```

