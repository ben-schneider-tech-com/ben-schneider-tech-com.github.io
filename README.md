# **How to Host Your Resume using Github Pages**
## **Purpose**
----------
This README describes the process for making your resume into a static website using Jekyll and how to host that website using Github pages. Also, this README explains how these practical steps are related to Etter's general principles of technical writing as described in *Modern Technical Writing: An Introduction to Software Documentation*.

## **Prerequisites**
-----------
- You must have an up-to-date resume formatted in markdown.
- You must have a Markdown editor

## **Instructions**
-----------
### **Creating a Jekyll static website for your resume**
 As Andrew Etter states, a static website is a good way to host resumes and documentation because it creates a centralized up-to-date resource for people to reference. You can just update the website instead of having to redistribute copies of documents. This makes maintaining changing resources like resumes and documentation easy.  
   
You can create your own static website by installing Jekyll and creating a new Jekyll project.  

1. Install Jekyll and Ruby on your system by [following these instructions](https://jekyllrb.com/docs/installation/)  
2. [Open a console in the directory you want your static website project to be located](https://tutorial.djangogirls.org/en/intro_to_command_line/)
3. Run `jekyll new resume` to create your static website project  

After running the above commands in a console, you should now have a Jekyll project on your system.  

### **Viewing your website in the browser**  
As is described in Andrew Etter's book, one of the advantages of using static websites is that they are fast and easy to work with locally. You can quickly see how your website looks without long and elaborate build processes.    

In this step you will view the website in the browser. This can be done by running a few simple commands as follows: 

1. [Navigate your console](https://tutorial.djangogirls.org/en/intro_to_command_line/) into the newly created project directory  
2. Run `jekyll serve --watch`  
3. Open the URL [`http://127.0.0.1:4000`](http://127.0.0.1:4000) in a browser  

After running these commands, the default Jekyll project template should be visible in your browser.

### **Adding your resume to your Jekyll website**  
As your resume is written in a lightweight markup language like Markdown, it easy to add your formatted resume to your static website. Jekyll can then easily turn your markdown resume into HTML for your website. That is what makes Markdown so good for creating web-hosted documents. This is why Andrew Etter advocates for using tools like Markdown for these kinds of documents.

 In this step, we will combine the markdown-formatted resume and the Jekyll project to create add your resume contents to the static website. This is done by copying your markdown resume into the Jekyll project, and editing some files in the Jekyll project.

1. Copy and paste your the body of your resume into the **index.markdown** file in the main project directory under the dashed line
2. Change the layout variable in the dashed line block from **home** to **default**
3. Write your contact information in the **about.markdown** file
4. Delete the **_posts** directory
5. Open the **config.yml** [yaml file](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started) in the main directory
6. Edit the **title** variable to be your name
7. Edit the **email** variable to be your email  
8. Delete the **description** variable
9. Rerun `jekyll serve --watch` to see your resume at [`http://127.0.0.1:4000`](http://127.0.0.1:4000)
10. Add a theme by following [this Github Pages tutorial](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll) **(optional)**    

After this step is completed, you should have your resume displayed in your Jekyll project. You accomplished this by editing the files in the Jekyll project to contain your resume and contact information.  

### **Hosting your Jekyll website in Github Pages**
Andrew Etter proposes using version-control like Git to control the source of your static website. This approach has several benefits. Git tracks changes made to documentation so you can always see how the documentation has been updated and what is new. Git also allows other members of the project to easily contribute to the project. All they need to do is make a pull request containing information to add to the static website.  

To host your static website on Github Pages, you will need to add it to a Github repository. This is done by creating a Github repository and using git to add the files of your project to the repository. This can be done as follows:  

1. [Download and install git](https://git-scm.com/downloads)
2. Create an account on [github.com](https://github.com/)
3. Navigate to [create token](https://github.com/settings/tokens/new) on Github
4. Create the token with the **repo** permission
5. Save the token on your computer
6. Click create repository
7. Name the repository *your_github_username.github.io*
8. Click **public repository**
9. Click **create repository**
10. Copy the URL under the under the *quick setup* section in the newly created repository
11. [Open a console](https://tutorial.djangogirls.org/en/intro_to_command_line/)
12. Run git clone with the first argument being the copied URL with your token and an @ sign prefixing the github.com part of the URL.  
**Note:** your command should look *something* like:  
`git clone https://ghp_7vPZBJGcmSWN0nsCVY7fjNCsmxWc6B4IGBaQ@github.com/ben-schneider-tech-com/ben-schneider-tech-com.github.io.git`  
13. Copy and paste the contents of your jekyll static website project into the newly created repository directory
14. Run `git add *`
15. Run `git commit -m "my resume website"`
16. Run `git push`
17. Go to **your_github_username.github.io** to see your website!
  
**Demo of creating a Github repository and using it to host a Jekyll website**  
![](https://github.com/ben-schneider-tech-com/ben-schneider-tech-com.github.io/blob/main/my_resume_demo.gif)  
  
Once this step is completed you will have your resume hosted on Github Pages. You will also have created a Github repository and added your Jekyll project files to that repository.  

## **More Resources**   
- **Markdown** is a simple but powerful markup tool for creating web documentation. An interactive tutorial on how to use markdown can be found [here](https://www.markdowntutorial.com/).  
- **Andrew Etter's book** [*Modern Technical Writing: An Introduction to Software Documentation*](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS) is a good introduction to the modern technical writing and documentation. Etter provides insight into both the tools and principles used in effective technical writing.  
- **To customize your website** you can create Jekyll [layouts](https://jekyllrb.com/docs/layouts/) and [themes](https://jekyllrb.com/docs/themes/). Alternatively, you can also use publicly available Jekyll themes, a tutorial on how to use these with Github Pages can be found [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll). 

## **Authors and Acknowledgments**
- Thank you to the [Hydejack Jekyll theme project](https://github.com/hydecorp/hydejack) for the theme used in my resume.
- Thank you to my group members: Sanskar Raval, Zil Patel and Aakash Chouhan for helping edit this README.

## **FAQ**

### **Why is Markdown better than a word processor?**
Markdown is a powerful, human-readable way of formatting test. Markdown is very portable and easy to host on websites. It is also very easy for many different contributors to work on a markdown document. If the document was written in a word processor it would require all contributors to have installed (or purchased) that word processor. Markdown allows for anyone to contribute to a centrally hosted web resource with minimal prerequisite software.

### **Why is my resume not showing up?**
This often happens when the Jekyll project files are copy and pasted into the wrong directory. Compare your Github repo to this project to make sure that the project files are arranged in the same way.  
This can also be caused by visiting the wrong URL make sure you are visiting `your_github_username.github.io`. The `your_github_username` field should be replaced by the name of your Github account.