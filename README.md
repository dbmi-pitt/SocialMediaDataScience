# Social Media Data Science

An exploration of the use of APIs, natural language, and text
processing to study online interactions via social media.  

Designed as a self-study, this module will take you through the process of retrieving, storing and analyzing tweets. Topics will include qualitative annotation, natural language processing, and classification using basic machine-learning methods. 

Content is provided in the form of [Jupyter notebooks](http://www.jupyter.org).  If you need an introduction to Jupyter, you can see the [official documents](https://jupyter-notebook.readthedocs.io/en/latest/) or this [Medium article](https://medium.com/analytics-vidhya/comprehensive-beginners-guide-to-jupyter-notebooks-for-data-science-machine-learning-3289f746856e). 

You can run these notebooks on a jupyterhub server - potentially one provided by your course - or on your own computer, appropriately configured with Python and other libraries. See [Part 0](SocialMedia%20%-%20Part%0.ibynp) for information on Python modules that you will need.

The remainder of this document will discuss how to use these modules for your class work.

# Using the module

The following steps describe how to use these modules in a Jupyter environment.


## 1.  Get a Twitter Developer account

Completing these modules requires a Twitter account with develop privileges. To do this, you can either create an individual Twitter account or join an organization account created by an instructor. As of October 2018, individual developer accounts require an approval process that has taken two weeks or longer, making educational group accounts an attractive option. 

Instructions for both approaches are given below, based on Twitter facilities as of October 2018. Although every attempt will be made to keep these materials up to date, please note that details may change. If any aspect of this document seems out of date, please file a GitHub issue. 

### 1.1 Creating an individual Developer Accouunt

To create an individual developer account:

1. Go to [Twitter's developer site ](Developer.twitter.com)
2. Click on the "Apply" link. You wil be required to login to Twitter if you haven't already done so
3. Complete the application. When asked for Account details, select "I am requesting access for my own personal use". 
4. Fill out the form and indicate as best possible what your are building - say you are exploring the application of natural language processing and machine learning to Tweets.
5. Submit the forms and wait for approval. 

Please note that approval might take two weeks or more.

### 1.2 Using a class/organization account

If you are an instructor, please visit the [Twitter for education playbook](https://developer.twitter.com/en/docs/basics/developer-portal/guides/twitter-for-education) and follow the instructions. As part of this process, you will collect Twitter Ids from your students and provide them to Twitter for access. 

Note that you will be asked to verify that you are a legitimate human educator.

If you are a student, work with your instructor to ensure that they create an appropriate account and invite you to the resulting organization.

## 2. Create a github or gitlab account

[Github](https://www.Github.com) and [GitLab](https://www.gitlab.com) are two popular community sites based on the Git source-code control system. We're going to use Git to create your own local copy of these modules, and to store any changes. We'll tell you a bit about it here, but there's much more to learn -  for more information on Git, see [git-scm.com](https://git-scm.com/).

For now, go to either [Github](https://www.Github.com) or [GitLab](https://www.gitlab.com) and create an account. Remember your account name.

## 3. Create a new repository in your GitHub or GitLab.com

The Jupyter notebook exercises for these models are contained in a GitHub repository - a collection of related files managed using the Git source code control system. To do your work for these modules, you will need your own personal copy of this repository, stored in your GitHub or GitLab account.  Below, we give different descriptions for GitHub and GitLab.

### 3.1 If you are using GitHub

To do this in GitHub will require three browser windows:

1. The first should be point at the GitHub.com repository that this file is in. You're probably on that page right now as you read this file. 
2. The second should be on your GitHub home page. 
3. The second window should be on your Jupyter notebook home page.

Once this is setup, we can go to work. 

1. In the window on your GitHub home page, to to the "+" sign on the upper-right and select "New Repository".  Type in the name "SocialMediaDataScience", mark the repository as "private", and hit "Create repository". This will take you to another page. Most of this page can be ignored, but there will be a link toward the top of the page listed under "Quick setup". Make a note of this link.  For more detailed information on creating GitHub reositories, see [Creating a new repository](https://help.github.com/articles/creating-a-new-repository/).

2. Go to your Jupyter home page. Click "New" on the top right, and select "Terminal" [Terminal](images/new-terminal.png). This will create a linux command-line terminal window in the browser.
3. From the home page of this repository, press the "Clone or Download" button [fork](images/fork-clone.jpg). This will lead to the display of the Git URL for the repository (it will probably look something like https://github.com/dbmi-pitt/SocialMediaDataScience.git). Copy this URL.
4. type "git clone --bare " followed by the URL of the repository. For example, "git clone --bare https://github.com/dbmi-pitt/SocialMediaDataScience.git". This will create a new directory named "SocialMediaDataScience.git"
5. Go into the new directory - "cd SocialMediaDataScience.git"
6. Grabbing the address of the new repository that you created in step one, run "git push --mirror " followed by the repository name. For example "git push --mirror https://github.com/harryhoch/SocialMediaDataScience.git" (with "harryhcoh" replaced by your user name"). You will have to provide a user name and password. At this point, the code will be added to your repository on GitHub. Go back to refresh the GitHub page. You will see the files.
7. In the terminal window, go up to the top-level directory by running "cd .."
8. Remove the directory that was created for when you ran "git clone". You can do this by running "rm -rf .." followed by the directory name. For example, "rm -rf SocialMediaDataScience.git"
9. Get the URL of the new repository in GitHub ("https://github.com/harryhoch/SocialMediaDataScience.git", as modified for your GitHub user name).

### 3.2 If you are using GitLab
1. Go to your GitLab homepage.
2. Click "+" in the top menu bar.
3. Select "New Project"
4. Click "Import Project" and then "Git Repo by URL"
5. At the top of the page containing this document, click on "Clone or download". Copy this URL
6. Paste this URL into the "Git repository URL" textbook on the GitLab import page.
7. Click "create project".  You can keep the repository to start.
8. You'll see a message indicating that something is happening.
9. When it is done, go to your home page. You should see a new repository. Go to the home page of that repository.  There will be a box under the repository title that says "SSH" with a URL next to it. Click on the "SSH" button to change it to "HTTPS".
10. Copy the URL next to the "HTTPS" button.

## 4. Clone the repository

At this point, you should have the URL for your own personal copy of this repository. You will now need to clone it into your Jupyter environment.

1. Go to your Jupyter home page. Click "New" on the top right, and select "Terminal" [Terminal](images/new-terminal.png). This will create a linux command-line terminal window in the browser.
2. run "git clone .." followed by the URL of your repository. You will need to provide your GitHub or GitLab user name and password.
3. In a new browser tab (or in an existing browser tab if you already have it open), go to the home page of your Jupyter environment. You will see a new directory, likely entitled "SocialMediaDataScience". This is where you will do your work.

## 5. Start a Jupyter notebook and do your work.

Here, you're going to start working in the Notebooks. 

1. From the Jupyter home page, select the folder "SocialMediaDataScience".
2. You'll see several files listed, including notebooks with names like "SocialMedia - Part 0.ibpynb", with numbers indicating part 0 - part 5. 
3. Click on "Part 0" and start the notebook.
4. Read through and execute the code in the notebook, going from part 0 to part 5 in order.  You can add cells to experiment and run code as you like.
5. You will be asked to create API Keys for Twitter and to save them in the notebooks. Please do that where indicated.
6. Each part of the module will have exercises, with cells inidicating where you should submit answers. Use these parts of the notebook to work on the exercises and to show your work. 
7. Every once in a while, you will want to hit "Save and Checkpoint" to save your work. This will also happen automatically, but it doesn't hurt to do it manually as well.
8. Each of the 5 parts has one or more exercises to go through, with indications of where your work should be added. Add cells and show the proper execution of your code, saving the worksheets when you are done.

## 6. Consider pushing

As you do your work on these modules, you will change the notebook and add file to the directory. To keep track of these artifacts, you will need to "push" them back on to GitHub/GitLab. To do this, follow these instructions:

1. From the Jupyter homepage, create a terminal window. As described above, Click "New" on the top right, and select "Terminal" [Terminal](images/new-terminal.png).
2. In the terminal window, change into the directory for this project - "cd SocialMediaDataScience" 
3. Run "git status". This will tell you which files have been added or modified.
4. For each file listed under "git status", type "git add .." followed by the filename, and then press return. This will prepare all of the files to be added or revised in the repository.
5. type "git commit -m'some message'",where you can replace 'some message' with an informative message. For example, you might say 'git commit -m'finished part 1'". 
6. Type "git push origin" and press return. You may see a warning message (which you can ignore). You will then be asked for your GitHub/GitLab user name and password.
7. Go to your home page on GitHub/GitLab and look at the repository. You will see the updated changes.

## 7. Finish up

When you are done with all of the exercises, you will proceed as follows:

1. Edit all of the files to remove your API keys
2. Push your work (as in Step 6, above)
3. Make the repository public, as in the following directions
4. Send the repository link to your instructor. 

### 7.1 Making a GitHub repository public

1. From the repository home page, click on the "Settings" gear icon.
2. Scroll to the "Danger Zone" box
3. Click on "Make public" and follow the irections.


### .7.2 Making a GitLab repository public
1. On the project page, click on "Settings" on the left bar. 
2. Click on "General" 
3. Find "Permissions" and click on "Expand"
4. Go to "Project visibility" and change it to "Public"
5. Click "Save Changes".

