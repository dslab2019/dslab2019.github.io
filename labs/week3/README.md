# Week 3 Data Science Lab

## Collaborative Data Science

### 1 - Gitlab setup

Go over to <https://git-dslab.epfl.ch/> and create an account with your EPFL e-mail.
This instance of gitlab resides within EPFL premises, so to access it
from outside the campus network, you'll need a VPN
(<https://epnet.epfl.ch/cms/site/network/lang/en/Remote-Internet-Access>).
Please note that the accounts are not sync’d with EPFL accounts, so you should use another password.

### 2 - Getting the project stub

Go to <https://git-dslab.epfl.ch/dslab2019/week3-git> and click on 'Fork'.

After setting up an SSH key pair (<https://docs.gitlab.com/ee/gitlab-basics/create-your-ssh-keys.html>),
you can now clone the project on your machine.

```bash
$ git clone git@git-dslab.epfl.ch:<group>/week3-git.git
```

### 3 - Recover the project

The repository is a very simple project for computing the Fibonacci’s sequence, following test driven development. But the project owner did some mistakes and didn’t leave the repository in a working shape.

Your mission is to recover all the files (using only git commands) and push it back to your forked repository. To check if you recovered all the files, you can run the test file, all 3 tests must pass.

This exercise doesn’t require special python library and only needs git to be setup, so you don’t need the virtual machine at this stage.
