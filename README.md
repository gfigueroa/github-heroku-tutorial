# Publish your website on the Internet with GitHub and Heroku

**TL;DR** This is a step-by-step tutorial for uploading your projects to [GitHub](http://github.com/) and hosting your static websites on [Heroku](http://heroku.com). We will use Git and the command line for doing tasks.

## I. Upload a project to GitHub
GitHub is a web-based Git or version control repository and Internet hosting service. In other words, it lets you upload all sorts of projects to their site and make them publicly available. You can upload websites, software projects, graphic design portfolios, or even your own collection of writings! GitHub is a great way of showing off your work to potential employers, universities or the public in general.

GitHub now also counts with an awesome new feature called [GitHub Pages](http://pages.github.com/), which can host one static website for free, but that's a topic for another day.

### 1. Create an account on GitHub
Sign up for a new account on [GitHub](http://github.com/).
*Make sure you confirm your email account before continuing.*

### 2. Create a GitHub repository for your project
If you are new on GitHub, you will see a screen like this, where you need to click "Start a Project":
![New Repository 1](./new_repo1.png)

If you already have other repositories on GitHub, you can create a new one by clicking on "New repository" as shown below:
![New Repository 1](./new_repo2.png)

We will now fill in some information about the new repository we are creating. In this tutorial, we will create a simple website on our computer and upload it to GitHub and Heroku.

For repository name, we will use `my-website`. In the description, we will write `A blank website for testing`, choose `Public` repository. Then, click on `Create repository`. 
**Note:** Unless you have previously created a repository with this name, everything should work out perfectly.

![Create Repository](./create_repo.png)

In the next screen, we will be provided with the URL for our newly created repository on GitHub. It should look something like this:
```
https://github.com/your-user-name/my-website.git
```

*Make not of this URL, as we will need it later!*

Our repository is now ready on GitHub for us to upload our files into it from our computer using Git.

### 3. Download and install Git on your computer
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. We will be using this tool to upload our projects to GitHub and Heroku.

#### Windows
Download the latest version of Git from [here](http://git-for-windows.github.io/).

Unless you know what you're doing, do not change any of the default Git settings when installing.
`Next->Next->Next->...->Install`

#### Mac
Follow the steps provided [here](http://www.atlassian.com/git/tutorials/install-git).
*Only follow the steps given in the section named **Git for Mac Installer**. Don't do the steps in the following sections (Install Git with Homebrew, etc.).*

#### Make sure Git is installed
Open the command line (Windows) or terminal (Mac) and enter:
```sh
$ git --version
```

You should see something like this (or a newer version):
```sh
$ git version 2.7.0
```

### 4. Upload your project

#### Create a blank website on your computer
In this tutorial, we are creating a new website to upload to GitHub and Heroku. You can skip this step if you wish to upload an already existing project or website.

Create a new folder on your computer called `My Website`. Inside that folder, add three files named `index.html`, `style.css`, and `script.js`. Your folder structure should look like this:
```
/My Website/
    ./index.html
    ./style.css
    ./script.js
```

We will only add some stuff into `index.html`, so open that file with your favorite text editor and add the following HTML code into it:
```html
<!DOCTYPE html>
<html>
	<head>
		<title>My Website</title>
	</head>
	<body>
		<h1>My Website</h1>
	</body>
</html>
```
Save and close the file.

#### Navigate to your project folder
Open the command line (Windows) or terminal (Mac) on your computer and navigate to your project folder.

If you are new to the Windows command line or Mac terminal, you can see the following steps to navigate to your project folder, otherwise you can skip the following step.

##### Windows
Click on the Start menu of your computer and type `cmd`, then press `Enter` on your keyboard. This will open up your command line.

If your website folder is not located on `C:\` drive, you must change the current drive you are on by entering the name of the drive followed by a colon (`:`):
```sh
$ d:
```
To get the full path of your website directory, an easy way is to open the Windows Explorer and go to the folder (mine is located on `D:\Comm Design\My Website`):
![Directory 1](./directory1.png)

Then, click on the navigation bar at the top and copy the whole path with `Ctrl + c`:
![Directory 2](./directory2.png)

Go back to the command line,type the following command, and press `Enter`:
```sh
$ cd paste-your-path-here
```
**Note:** To paste your path, you must right click on the command line and select `Paste` from the pop-up menu. You cannot do `Ctrl + v` here!

You can then make sure that you are on the right directory by entering the following command, which should list your folder contents:
```sh
$ dir
```

Your command line should look like this by now:
![CLI 1](./cli1.png)

##### Mac
Open the terminal by searching in the Finder and typing in `terminal`.

Navigate to your folder by using the `cd` command. For example, if the website folder is in my desktop in the directory `/Users/gfigueroa/Desktop/Comm Design/My Website`, then I need to type:
```sh
$ cd "/Users/gfigueroa/Desktop/Comm Design/My Website"
```
**Note:** Since my directory has some spaces inside it, I need to wrap it around double quotes `""`.

You can then make sure that you are on the right directory by entering the following command, which should list your folder contents:
```sh
$ ls
```

#### 

## II. Host a website on Heroku