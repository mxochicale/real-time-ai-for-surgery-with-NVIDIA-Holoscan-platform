# Contributing to `real-time-ai-assistance-for-surgery-with-NVIDIA-Holoscan-platform`

👍🎉 First off, thanks for taking the time to contribute! 🎉👍

When contributing to this repository, please first discuss the change you wish to make via issue, instant message in clara-agx chatbox, or any other method with the owners of this repository before making a change. 
Please note we have a [code of conduct](.github/CODE_OF_CONDUCT.md), please follow it in all your interactions with the project.

## :octocat: Setting up project locally. 
1. Generate your SSH keys as suggested [here](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
2. Clone the repository by typing (or copying) the following lines in a terminal
```
git clone git@github.com:mxochicale/real-time-ai-for-surgery-with-NVIDIA-Holoscan-platform.git
```

## New issues
* Open an issue (bug report, feature request, or something is not working): https://github.com/mxochicale/real-time-ai-for-surgery-with-NVIDIA-Holoscan-platform/issues/new
* Workflow for issue management 
```mermaid
  flowchart TD;
      Z[Bug Reported] -->A[...];  
      A[Bug resolution] -->B(Testing OK?);
      B--Yes-->C[Prepare commit];
      B--No-->D[Reopen issue];
      D----> A[Bug resolution];
      C ----> E[Request Review];
      E ----> F[Commit changes];
      F --> H[Merge PR and close issue]
```  

## Committing and pushing changes 
1. Clone this repo 
```
git clone git@github.com:mxochicale/real-time-ai-for-surgery-with-NVIDIA-Holoscan-platform.git
``` 
2. Create new branch using issue number
```
git checkout -b ISSUENUMBER-branch-name 
```
3. Commit changes and push to your branch
```
git add .
git commit -m 'short message (#ISSUENUMBER)'
git push origin ISSUENUMBER-branch-name
```
4. Submit a Pull Request against the `main` branch. 

## Pull Request (PR)
1. Select branch that contain your commits.
2. Click `Compare and pull request` and create PR for the associated branch.
3. Type a title and description of your PR and create PR
4. Please keep your PR in sync with the base branch.
```
git checkout main
git pull origin main
git checkout RB 
git rebase main
git push --force origin RB
```
5. Run `pre-commit` to tidy up code and documentation (see next section). 
6. Request a PR review.
See [collaborating-with-pull-requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests) for further details.

