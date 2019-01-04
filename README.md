# Social Media Data Science

An exploration of the use of APIs, natural language, and text
processing to study online interactions via social media.  

Designed as a self-study, this module will take you through the process of retrieving, storing and analyzing tweets. Topics will include qualitative annotation, natural language processing, and classification using basic machine-learning methods. 

Content is provided in the form of [Jupyter notebooks](http://www.jupyter.org).  If you need an introduction to Jupyter, you can see the [official documents](https://jupyter-notebook.readthedocs.io/en/latest/) or this [Medium article](https://medium.com/analytics-vidhya/comprehensive-beginners-guide-to-jupyter-notebooks-for-data-science-machine-learning-3289f746856e). 

You can run these notebooks on a jupyterhub server - potentially one provided by your course - or on your own computer, appropriately configured with Python and other libraries. See [Part 0](SocialMedia%20%-%20Part%0.ibynp) for information on Python modules that you will need.

Data science modules developed by the University of Pittsburgh Biomedical Informatics Training Program with the support of the National Library of Medicine data science supplement to the University of Pittsburgh (Grant # T15LM007059-30S1).

Developed by Harry Hochheiser, harryh@pitt.edu. All errors are my responsibility.

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

The remainder of this document will discuss how to use these modules for your class work.

# Using the module

The following steps describe how to use these modules in a Jupyter environment.

## 1. Access your Jupyter configuration.

These exercises will be completed using [Jupyter](http://jupyter.org) computational notebooks. There are two ways that you might do this:

1. In a server environment provided by your instructor and/or institution
2. On your own computer.

Furthermore, there are multiple ways that you can do this:
1. Using traditional Jupyter notebooks
2. Using [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/), an alternative interface with features similar to those of an integrated development environmnent.

In either case, it is important to get the right version of Python. As of October 2018, Python 3.6 is necessary, along with several libraries (listed below in Section 3.3). The need to have the appropirate Python version will be mentioned below when we discuss the use of the notebooks.

## 1.1 To use a server environment.

To use the server environment, you will need to follow directions from your instructor or mentor as to how to access appropriate local computing facilities. Reiterating the point made above, please be sure that your instructor and computing staff configure the servers for Python 3.6.

## 1.2 To install on your own computer

Installation on your own computer is not difficult for those who are familiar with some amount of command line operation and software configuration. 

This installation generally requires 3 components:

* Python 
* Jupyter tools
* Additional Python libraries (described below in 1.3)

There are a variety of ways to accomplish these tasks. Here, we will focus on one approach that has proven relatively straightforward - the [miniconda](https://conda.io/miniconda.html) tool. Go the miniconda site and follow the installation instructions.  

Once you have miniconda installled, you will need to install Python 3.6 and Jupyter tools.  Gergeley Szerovay's article [Why you need Python environments and how to manage them with Conda](https://medium.freecodecamp.org/why-you-need-python-environments-and-how-to-manage-them-with-conda-85f155f4353c) provides a good explanation of how this can be done. Once you complete the installation of the basic notebooks, you can [install JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html) if desired.

## 1.3 Python Packages

There are several add-on Python libraries that are used in these modules:

* [NumPy](http://www.numpy.org) - for preparing data for plotting
* [Matplotlib](https://matplotlib.org) - plots and garphs
* [jsonpickle](https://jsonpickle.github.io) for storing tweets. 
* [spaCy](https://spaCy.io/) - an NLP toolkit.
* [scikit-learn](http://scikit-learn.org) for machine learning
* [tweepy](http://www.tweepy.org) for retrieving Tweets via the Twitter API.

If you are using an installation provided by your instructor, please work with your instructor to install these libraries correctly. If you are using your own equipment, you will need to follow the instructions given with your tools, such as miniconda, to complete the installation. 

## 2.  Get a Twitter Developer account

Completing these modules requires a Twitter account with develop privileges. To do this, you can either create an individual Twitter account or join an organization account created by an instructor. As of October 2018, individual developer accounts require an approval process that has taken two weeks or longer, making educational group accounts an attractive option. 

Instructions for both approaches are given below, based on Twitter facilities as of October 2018. Although every attempt will be made to keep these materials up to date, please note that details may change. If any aspect of this document seems out of date, please file a GitHub issue. 

### 2.1 Creating an individual Developer Accouunt

To create an individual developer account:

1. Go to [Twitter's developer site ](Developer.twitter.com)
2. Click on the "Apply" link. You wil be required to login to Twitter if you haven't already done so
3. Complete the application. When asked for Account details, select "I am requesting access for my own personal use". 
4. Fill out the form and indicate as best possible what your are building - say you are exploring the application of natural language processing and machine learning to Tweets.
5. Submit the forms and wait for approval. 

Please note that approval might take two weeks or more.

### 2.2 Using a class/organization account

If you are an instructor, please visit the [Twitter for education playbook](https://developer.twitter.com/en/docs/basics/developer-portal/guides/twitter-for-education) and follow the instructions. As part of this process, you will collect Twitter Ids from your students and provide them to Twitter for access. 

Note that you will be asked to verify that you are a legitimate human educator.

If you are a student, work with your instructor to ensure that they create an appropriate account and invite you to the resulting organization.

## 3. Create a github or gitlab account

[Github](https://www.Github.com) and [GitLab](https://www.gitlab.com) are two popular community sites based on the Git source-code control system. We're going to use Git to create your own local copy of these modules, and to store any changes. We'll tell you a bit about it here, but there's much more to learn -  for more information on Git, see [git-scm.com](https://git-scm.com/).

For now, go to either [Github](https://www.Github.com) or [GitLab](https://www.gitlab.com) and create an account. Remember your account name.


## 4. Create a new repository in your GitHub or GitLab.com

The Jupyter notebook exercises for these models are contained in a GitHub repository - a collection of related files managed using the Git source code control system. To do your work for these modules, you will need your own personal copy of this repository, stored in your GitHub or GitLab account.  Below, we give different descriptions for GitHub and GitLab.

### 4.1 If you are using GitHub

To do this in GitHub will require three browser windows:

1. The first should be point at the GitHub.com repository that this file is in. You're probably on that page right now as you read this file. 
2. The second window should be on your Jupyter notebook or JupyterLab home page.

Once this is setup, we can go to work. 

1. In the window on your GitHub repository page, press the "fork" button, found just below your avatar and user name in the title bar. It will ask you "Where should we fork this repository?". Choose the selection corresponding to your GitHub user name. The system will ask you to wait, and it will point you to a new page with a copy of this repository under your account. This is now your repository to use as you will, without any fear of damaging the main repository.
2. On this page, there is a ["Clone or download" button](images/fork-clone.png). Click on this button and copy the link that shows up. You will need this URL in step 5.

### 4.2 If you are using GitLab
1. Go to your GitLab homepage.
2. Click "+" in the top menu bar.
3. Select "New Project"
4. Click "Import Project" and then "Git Repo by URL"
5. At the top of the page containing this document, click on "Clone or download". Copy this URL
6. Paste this URL into the "Git repository URL" textbook on the GitLab import page.
7. Click "create project".  You can keep the repository to start.
8. You'll see a message indicating that something is happening.
9. When it is done, go to your home page. You should see a new repository. Go to the home page of that repository.  There will be a box under the repository title that says "SSH" with a URL next to it. Click on the "SSH" button to change it to "HTTPS".
10. Copy the URL next to the "HTTPS" button. You will need this URL in step 5.

## 5. Clone the repository

At this point, you should have the URL for your own personal copy of this repository. You will now need to clone it into your Jupyter environment.

1. Go to your Jupyter home page. Click "New" on the top right, and select ["Terminal"](images/new-terminal.png). This will create a linux command-line terminal window in the browser. Alternatively, if you are using JupyterHub, press the "Terminal" button in the Launcher screen.
2. run "git clone .." followed by the URL of your repository. You will need to provide your GitHub or GitLab user name and password.
3. In a new browser tab (or in an existing browser tab if you already have it open), go to the home page of your Jupyter environment. You will see a new directory, likely entitled "SocialMediaDataScience". This is where you will do your work. If you are using JupyterLab, this directory will appear in the file browser on the left.

## 6. Start a Jupyter notebook and do your work.

Here, you're going to start working in the Notebooks. 

1. From the Jupyter home page, select the folder "SocialMediaDataScience." If you are using JupyterLab, you'll see this folder listed on the file chooser on the left-hand side.
2. You'll see several files listed, including notebooks with names like "SocialMedia - Part 0.ibpynb", with numbers indicating part 0 - part 5. 
3. Click on "Part 0" and start the notebook.
4. Read through and execute the code in the notebook, going from part 0 to part 5 in order.  You can add cells to experiment and run code as you like.
5. You will be asked to create API Keys for Twitter and to save them in the notebooks. Please do that where indicated.
6. Each part of the module will have exercises, with cells inidicating where you should submit answers. Use these parts of the notebook to work on the exercises and to show your work. 
7. Every once in a while, you will want to hit "Save and Checkpoint" to save your work. This will also happen automatically, but it doesn't hurt to do it manually as well.
8. Each of the 5 parts has one or more exercises to go through, with indications of where your work should be added. Add cells and show the proper execution of your code, saving the worksheets when you are done.


If you ever have trouble running the code, it may be because you are running the wrong version of Python. To change this, look under the "kernel" menu on the notebook page. Select it and switch to a kernel that specifies Python 3.6. This should be clear somewhere in the program name. If this doesn't work, you might have to ask your instructor (if you are using an environment provided by the school) or revisit your installation to ensure that you are using Python 3.6.

## 7. Consider pushing

As you do your work on these modules, you will change the notebook and add file to the directory. To keep track of these artifacts, you will need to "push" them back on to GitHub/GitLab. To do this, follow these instructions:

1. From the Jupyter homepage, create a terminal window. As described above, Click "New" on the top right, and select "Terminal" [Terminal](images/new-terminal.png).
2. In the terminal window, change into the directory for this project - "cd SocialMediaDataScience" 
3. Run "git status". This will tell you which files have been added or modified.
4. For each file listed under "git status", type "git add .." followed by the filename, and then press return. This will prepare all of the files to be added or revised in the repository.
5. type "git commit -m'some message'",where you can replace 'some message' with an informative message. For example, you might say 'git commit -m'finished part 1'". 
6. Type "git push origin" and press return. You may see a warning message (which you can ignore). You will then be asked for your GitHub/GitLab user name and password.
7. Go to your home page on GitHub/GitLab and look at the repository. You will see the updated changes.

## 8. Finish up

When you are done with all of the exercises, you will proceed as follows:

1. Edit all of the files to remove your API keys
2. Push your work (as in Step 6, above)
3. Make the repository public, as in the following directions
4. Send the repository link to your instructor. 

### 8.1 Making a GitHub repository public

1. From the repository home page, click on the "Settings" gear icon.
2. Scroll to the "Danger Zone" box
3. Click on "Make public" and follow the irections.


### 8.2 Making a GitLab repository public
1. On the project page, click on "Settings" on the left bar. 
2. Click on "General" 
3. Find "Permissions" and click on "Expand"
4. Go to "Project visibility" and change it to "Public"
5. Click "Save Changes".

# Final Notes.

These insturctions are, we think, accurate at the time of writing. Please submit issues with any difficulties or inaccuracies. 
