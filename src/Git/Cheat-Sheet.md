## Git Cheat Sheet

Git is most widely used version control system. In my point of view, every developer should know how to use Git. There are a lot of different ways to use Git: original command line tools and Gui based Git clients. (such as *SmartGit*, *SourceTree* etc.). But command line is the only place you can run all Git commands.

<dl>
  <dt>git config</dt>
  <dd>The first thing you should configure your identity: email and name. You can configure your identiy either for all repositories of your computer or for a single repository. To configure identity for single repository, use the following command:
    
  > ```Assembly
  > git config user.email "Your Email Address"
  > git config user.name "Your User Name"
  
  To configure identity for all repositories, You just need to add `--global` after `git config` like
  
  > ```Assembly
  > git config --global user.email "Your Email Address"
  > git config --global user.name "Your User Name"
  
  You can even check your configuration settings, you need to use the `git config --list` command to view the settings for the current repository. You can also retrieve a single configuration using the the `git config user.name` command. To view the global configuration, you need to add `--global` after `git config`.
  </dd>
  <dt>git init</dt>
  <dd>It can be used to convert an unversioned project to a Git repository or initialize a new, empty repository. Most other Git commands are not available outside of an initialized repository, so this is usually the first command you'll run in a new project.
  </dd>
  <dt>git clone</dt>
  <dd>It create a local copy of a Git repository on your computer. Use the following command to clone a repository:

  > ```Assembly
  > git clone https://github.com/<USERNAME>/<REPOSITORY>.git

  The above command will clone `master` branch of the repository. It is also possible to specificy a branch name when clone a repository like
  
  > ```Assembly
  > git clone -b <BRANCH> https://github.com/<USERNAME>/<REPOSITORY>.git
  </dd>
  <dt>git branch</dt>
  <dd>To delete a local branch, run this command
  
  > ```Assembly
  > git branch -D <BRANCH_NAME>

  To rename a local branch, run the following command.

  > ```Assembly
  > git branch -m <NEW_BRANCH_NAME>
  </dd>
  <dt>git tag</dt>
  <dd>To cretae a tag, run this command.

  > ```Assembly
  > git tag <VERSION>

  To create tag on old commit, run the following commans.

  > ```Assembly
  > git tag <VERSION> <COMMIT_NO>
  
  To include description with your tag, run the following command.

  > ```Assembly
  > git tag -a <VERSION> -m "<MESSAGE>"

  To push the tag(s) to remote, use the following command.

  > ```Assembly
  > git push origin <VERSION> # to push a single tag
  > git push origin --tags # to push all tags`
  </dd>
</dl>
