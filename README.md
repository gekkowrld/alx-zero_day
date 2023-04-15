# Welcome

I'm going to recreate the step by step guide given by alx on how to go about the first project. I'm going to talk about the following concepts:

>> - [Creating a Personal Token](#creating-a-personal-token) _needed only once until it expires_
>> - [Cloning Your repository from github](#cloning-your-repository-from-github) _needed only once per repository_
>> - [Adding files to the git](#adding-files-to-the-git) _Frequently needed per major change_
>> - [Committing files to git](#committing-files-to-git) _Frequently needed per major change_
>> - [Pushing the files to github](#pushing-the-files-to-github) _Frequently needed per major change_

If you don't know how to create a repository (or 'repo' for short) then you can follow the instructions from [official github docs](https://docs.github.com/en/get-started/quickstart/create-a-repo)

## [Creating a Personal Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

The first step is to create a personal token. This is like your identity on github. You have to use this to authenticate. There are two types of tokens.

>> 1. Fine-grained personal token
>> 2. Classic personal token

In ALX the recommended token is Classic personal token, so I'm going to use that. **Note that the fine grained can be used too.**

Follow the instructions on [this page](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) to create your github token.

## Cloning Your repository from github

The second task is to clone your git repository. This maybe the most confusing part.

You can alternatively follow the steps outlined in the [official github docs](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)

1. Go to the part labeled Code
   ![An image with a icon labelled code](https://docs.github.com/assets/cb-20363/mw-1000/images/help/repository/code-button.webp)

2. Click on it, then choose the option https
    ![An image with a highlighted copy icon from github](https://docs.github.com/assets/cb-88716/mw-1000/images/help/repository/https-url-clone-cli.webp)
3. Copy the url code then come to your sandbox or whichever place you want to clone it to.

   ```bash
   git clone https://ghp_nuTr9KEvPLaYus24d5WMVXv5LSwrh2Lh5Kv@/github.com/gekkowrld/alx-zero_day.git
   ```

>> The format should be similar, the `git clone` statement first then `https://your_personal_token` then the rest of the github details `/gihub.com/gekkowrld/alx-zero_day.git`
>>> **The personal token used here is not valid personal token for security purposes**

## Adding files to the git

First cd to your repository

```bash
cd alx-zero_day
```

Then create the files as instructed

```bash
# First create a file
touch README.md

# Add content to it. There are many ways to do this but let's use the required way
echo 'My first readme' > README.md 

# Check the contents of the file
cat README.md
```

Before adding anything to git, we are told to update our identity. This is crucial because it is what git will use to identify us.

Add an email

```bash
git config --global user.email "you@example.com"
```

>> Replace the "you@example.com" with your actual email. For those who opted for private email, you can use it here instead of the actual email

Add a username

```bash
git config --global user.name "Your Name"
```

Here your username can be anything you want. BUt for consistency use your name or your github username

Now we have to check and see our details just to be sure

```bash
# To see your username
git config --get user.name

# To see your email
git config --get user.email
```

Now let's add the newly created file to git

```bash
git add .

# The git add tells git to add every file in this current repository/folder to git. The '.' is a git expansion for current directory
```

## Committing files to git

Let's commit the changes to git so that we don't loose them.
It is important to always use descriptive commits. Writing good commit messages can help you and your future self. You can refer to the [conventionalcommits.org](https://www.conventionalcommits.org/en/) for tips.

```bash
# We are going to use the specific commit message because it is the one given by ALX
git commit -m 'My first commit'
```

## Pushing the files to github

The final step is to push.

```bash
# The git push doesn't take any arguments
git push
```

There is a prompt to input your username and password. Your password is your token that you created. There will be no visible indicator that you have entered the password. This is normal, just press enter.

And **voila** you have pushed your repository and file to git.

## Git pull

```bash
git pull
```

This is only needed when a change was done elsewhere other than the current working platform/station

If you encounter any problem feel free to open an [issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue).
