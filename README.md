# **How to Host Your Resume using Github Pages**
## **Purpose**
----------
This README describes the process for making your resume into a static website using Jekyll and how to host that website using Github pages. Also, this README explains how these practical steps are related to Etter's general principles of technical writing.

## **Prerequisites**
-----------
- You must have an up-to-date resume formatted in markdown.

## **Instructions**
-----------
### **Creating a Jekyll static website for your resume**
A static website is a good way to host resumes and documentation because it creates a centralized up-todate resource for people to reference. Instead of having to keep track of how you have distributed copies, you can just update the website. This makes maintaining changing resources like resumes and documentation easy. To create your static website do the following:
1. Install Jekyll on your system by [following these instructions](https://jekyllrb.com/docs/installation/)  
2. Open a console in the directory you want your static website project to be in
3. Run `jekyll new resume` to create your static website project

### **Viewing your website in the browser**  
One of the advantages of using static websites is that they are fast and easy to work with locally. You can quickly see how your website looks without long and elaborate build processes. To see your website, simply do the following:
1. Navigate your console into the newly created project directory  
2. Run `jekyll serve --watch`  
3. Open the url [`http://127.0.0.1:4000`](http://127.0.0.1:4000) in a browser  

### **Adding your resume to your Jekyll website**  
As your resume is written in a lightweight markup language like markdown, it easy easy to add your formatted resume to your static website. Jekyll can then easily turn your markdown resume into HTML for your website. Resources on how to customize your website more can be found under the *more resources* section of this README. You can add your resume to the Jekyll website as follows:
1. Copy and paste your the body of your resume into the `index.markdown` file in the main project directory under the dashed line
2. Change the layout varaible in the dashed line block from `home` to `default`
4. Write yuor contact information in the `about.markdown` file 
5. Open the `config.yml` [yaml file](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started) in the main directory
6. edit the `title` variable to be your name
7. edit the `email` variable to be your email  
8. delete the `description` variable
9. rerun `jekyll serve --watch` to see your resume at [`http://127.0.0.1:4000`](http://127.0.0.1:4000)

### **Hosting your Jekyll website in Github Pages**
By using version-control like Git to control the source of your static website has several benefits. Git tracks changes made to documentation so you can always see how the documentation has been updated and what is new. Git also allows other member sof the projec to easily contribute to the project. All they need to do is make a pull request containing information to add to the static website. By following the steps below you can put your website into version control and host it on Github Pages.
1. [Download and install git](https://git-scm.com/downloads)
1. Create an account on [github.com](https://github.com/)
2. Navigate to [create token](https://github.com/settings/tokens/new)
2. Create the token with the *repo* permission
4. Save the token on your computer
2. Click create repository
3. Name the repository with the name *your_github_username.github.io*
4. Click `public repository`
5. Click `create repository`
8. Copy the url under the under the *quick setup* section in the newly created repository
9. open a console
10. run git clone with the first argument being copied url with your token and an @ sign prefixing the guthub.com part of the url.  
Note: your command shoud look something like:  
`git clone https://ghp_7vPZBJGcmSWN0nsCVY7fjNCsmxWc6B4IGBaQ@github.com/ben-schneider-tech-com/website.git`  
11. Copy and paste the contents of your jekyll static website project into the newly created repository directory
12. run `git add *`
13. run `git commit -m "my resume website"`
14. run `git push`
15. Go to *your_github_username.github.io* to see your website!

![](https://github.com/ben-schneider-tech-com/ben-schneider-tech-com.github.io/blob/main/my_resume_demo.gif)

## **More Resources**   
- **Markdown** is a simple but powerful markup tool for creating web documentation. An interactive tutorial on how to use markdown can be found [here](https://www.markdowntutorial.com/).  
- **Andrew Etter's book** [*Modern Technical Writing: An Introduction to Software Documentation*](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS) is a good introduction to the modern technical writing and documentation. Etter provides insight into both the tools and principles used in effective techinal writing.  
- **To customize your website** you can create Jekyll [layouts](https://jekyllrb.com/docs/layouts/) and [themes](https://jekyllrb.com/docs/themes/). Alternatively, you can also use publicly available Jekyll themes, a tutorial on how to use these with Github Pages can be found [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll). 

## **Authors and Acknowledgments**
- Thank you to the [Hydejack Jekyll theme project](https://github.com/hydecorp/hydejack) for the theme used in my resume.
- Thank you to my group members: Sanskar Raval, Zil Patel and Aakash Chouhan for helping edit this README.

## **FAQ**

### **Why is Markdown better than a word processor?**
Markdown is a powerful, human-readable way of formatting test. Markdown is very portable and easy to host on websites. It is also very easy for many different contributers to work on a markdown document. If the document was written in a word processor it would require all contributers to have installed (or purchased) that word processor. Markdown allows for anyone to contribute to a centrally hosted web resource with minimal prerequisite software.
