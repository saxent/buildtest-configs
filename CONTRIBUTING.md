Want to contribute back to buildtest and make this project a success? 
Please follow the instructions below, we would love to get your feedback to help
improve this project and be meaningful.

## Preparation

### Fork the buildtest-configs

First, you will need to fork [buildtest-configs from GitHub](https://github.com/HPC-buildtest/buildtest-configs).

You might need to setup your SSH keys in your profile if you are using ssh 
option for cloning. For more details on setting up SSH keys in your profile, 
follow instruction found in 
https://help.github.com/articles/connecting-to-github-with-ssh/

SSH key will help you pull and push to repository without requesting a 
credential. If you dont have a Github account, please register an account so 
you can fork this repo.

After creating your fork copy, clone your fork buildtest-framework repo

```bash
git clone git@github.com:YOUR\_GITHUB\_LOGIN/buildtest-configs.git
```


### Sync devel branch from upstream

The devel from upstream will get Pull Requests from other contributors, in-order
 to sync your fork with upstream repo, first you need to add a new remote ``upstream``
 that can be done as follows :

```bash
cd buildtest-configs
git remote add upstream git@github.com/HPC-buildtest/buildtest-configs.git
```

Next we sync local ``devel`` branch with upstream. Make sure you are in ``devel`` branch before
pulling changes

```bash
git branch devel
git checkout devel
git fetch upstream devel
git pull -r upstream devel
```

Once the changes are pulled locally you can push the changes for devel branch to your 
fork at GitHub

```bash
git checkout devel
git push origin devel
```

Do this same operation with master if you want to sync it with upstream repo

### Feature Branch

Please make sure to create a new branch when adding and new feature. Do not push 
to **master** or **devel** branch on your fork or upstream. 

Create a new branch as follows

```bash
cd buildtest-configs
git checkout devel
git checkout -b featureX
```

Once you are ready to push to your fork repo do the following

```bash
git push origin featureX
```

Once the branch is created in your fork, you can create a PR to the ``devel`` branch.


### Review

Someone from the **buildtest team** will review the PR and get back to you with 
the feedback. If the reviewer requests some changes, then the user is requested 
to make changes and update the branch used for sending PR

If a PR is closed and you want to make slight adjustment, just open the PR and 
make the change in your branch. If everything looks fine and PR is merged, you 
can delete your local branch.
