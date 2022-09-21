# HackathonRepo
Repository for our hackathon team to collaborate on.


## Branches
### Overview

- A branch can be seen as a clone, or version, of the `main` branch
- The `main` branch is essentially the live, most up to date working version of the code, and so should be treated with love and care!
- It's similar to the ICW database arrangement where ICW live is (hopefully) always working and any changes that are made will have been developed in the ICW dev database. This is equivalent to branching off of `main`, carrying out some development and testing, and then merging your branch back to `main`, or, integrating your changes from ICW dev back to ICW live


## Commits
### Overview

- When working on a git repository on your machine, the repository is saved locally but it's tracked by git (your local git repo will have a hidden .git folder which does this)
- Committing is the mechanism by which you 'save' your script changes while working in a git repository so that git is aware of the changes, until you make a commit your changes cannot be recorded in the repository
- Note, there are a couple of sub-mechanisms in the process of committing, it's worth having a little look at the git documentation and I'm happy to demonstrate in person, I just think I'll confuse you guys/myself trying to explain it on here!


## Push/Pull
### Overview

- Pushing is the mechanism by which you send your commits to the repository, so the commit records the changes and the push sends them off to remote so that they can be viewed by anyone with access, whether that's on your branch, somebody else's, or `main`
- Pulling is the mechanism by which you update your local repo with any commits that have been made elsewhere, it's useful to do this every now and then so that you can get an updated version of the repo and any changes made by others
- A pull request is a specific action where you are essentially requesting that `main` branch pulls your changes/commits, updating main in the process. Some context is given below


## Example process

Let's say you want to start working on a python script in a git repository with your team, the first thing you'll want to do is clone the repository, which is basically saving the repository locally to your machine (not to be confused with the cloning that occurs when making a branch), there are a number of ways you can clone from github, check the documentation/google and just save it in a sensible purpose made folder.

Once the git repo is on your local machine, you want to start working on the script and so the next step is to create your own branch away from `main`. Name it something useful like your name so we know whose work it is, or alternatively name it the specific feature that you are working on (this is probably more helpful).

So now you are coding on your own branch, at the time of branching it will look exactly identical to `main`, but as changes are made, both to your branch as well as `main`, they will obviously start to look different.

You add 10 lines of code to the script in your branch so it's time to make a commit, this will depend on if you're working in the command line, VSCode, SageMaker etc. but the underlying steps are all the same. Once you've made the commit and pushed it to your branch, those 10 lines of code will be saved in your branch, you should be able to see the 10 new lines if you visit the repository on the github website and select your branch (note that you may not always want to push after a commit, this is dependent on a number of things such as the readiness of the code and which branch you're working on among others).

If you're satisfied with your changes and you think it's suitable for production (maybe you even ran some tests) then it's time to merge your branch back to `main`. Depending on the preset permissions, this is usually done by a 'pull request' which could require any number of code reviewers before your push is accepted and 'merged' back to the `main` branch. 

If `main` has not been edited while you were away coding (or at least any edits were made to other sections of the script, or other scripts in the repository) then this should be a smooth process and the 'main' branch will be updated, but if there were changes pushed to `main` that interfere with what you have done then you'll have what's called a merge conflict on your hands! The interface here can be confusing but basically it asks you to edit your changes so they don't clash, or alternatively to choose between your version of the disputed section or the already existent version. This is not ideal but it's not the end of the world, it's a good idea to speak to the user whose changes you have clashed with in order to work out what's the best thing to do.

Something to note here is that if you do not get updates from `main` (pull from `main`) and send updates to `main` (push to `main`) relatively frequently (obviously dependent on how much your team is working) then you will run into lots of merge conflicts and other conflict-related nightmares.


## Notes

- I apologise for bits of this that might be unclear, I've done my best but I'm no expert!
- No matter how much I read about git when I was first learning, it never made any sense to me until I actually started using it and destroyed countless repositories with scary error messages and conflicts, so I would suggest trying it out or watching a run through just so you can see it in action
- And of course feel free to ask me any questions, no guarantees but I'll do my best to answer, I find Google very helpful when I'm lost 
