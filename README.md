## Brief of the Repository 
This repo contains the simple Jenkinsfile that was used to Practice the different types of Build Triggers.

## Procedure for the Execution
So, first create a Git repository on GitHub. So log into your GitHub account and create a new repository. Click on new. You can create repository with any name.  Just a simple jenkinsfile and we'll create repository. Okay, so repository is created and we will be using the SSH link. So before we clone this Git repository we need to store our SSH keys in our GitHub account. If you already did this in  you can just directly start cloning this. 

If you have not done it, then create the SSH keys open git bash in Windows Macs open terminal and the command SSH-keygen. So it'll generate the private and the public key. Then just hit enter until the keys gets created and you should find the keys in your home directory, ~/.SSH and you should see the public key and the private key. We will take the content of the public key we'll copy this content public key (again and not the private key). Private key is a very long one. So copy the public key go to your GitHub account, go to settings. This is the accounts setting, not the repository settings. So you need to click over your profile and come to the settings and go to SSH and GPG keys. Click on new SSH key here and give a title. And will just say my laptop and I'm going to paste the public key here.
Again, public key, not the private key here. Add SSH keys. Enter the password if it asks. Okay, public key stored.

Now let's go to a repository that we just created. And click over here on SSH. And you need to use this link not the HTTPS, SSH link. Just copy it and go to Git Bash. Create a directory in F. You can create it anywhere, go to the created  directory and type  Git clone and paste the URL (shift + Insert) Enter. It'll ask you. Say yes, so you cloned the repository. You should see it over there. Now we'll place a jenkinsfile into this. This is will be a very very simple jenkinsfile.

```bash
pipeline {
	agent any
	stages {
		stage('Build') {
			steps{
				sh 'echo "Build completed."'
			}
		}
	}
}
```

which will just print a message. You can use any editor of your choice and will have this code over there. 

## PIPELINE EXPLANATION
Pretty simple pipeline agent, any stages, only one stage. Stage name I have given As build. Step is just to echo this message. So we really not doing any build part over here we are just using the simple jenkinsfile. 


Now you can store your original jenkinsfile which we already created, but for now, just keep it simple. Just create the simple jenkinsfile and save it. 
In our repository, while saving the file say file type all files and file name will be Jenkinsfile, J capital. Save it. Okay, once you save this file, and if you'd like to use VIM editor, whatever editor just create the jenkinsfile in the repository. Yeah, just jenkinsfile. 
Okay. Now we'll say 

```bash
git add .
```

```bash
git commit -m "any message you want"
```

```bash
git push
```
Okay, that's done. 
