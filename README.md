[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/isPhTOcA)

# **About Wizard Portal**
This is a fan website dedicated to all the enthusiasts of Hogwarts Legacy. Here, you will find a collection of information, news, and resources related to the game, allowing you to immerse yourself in the magical world of Hogwarts.

If you're interested in checking it out, here's the link for you
**[Wizard Portal](https://wizardportal.site)**.


# **Documentation**
## **1. Creating Branch, Adding Files, and Committing Changes on GitHub.**

    This guide will walk you through the steps to create a new branch in a GitHub repository, add files, commit changes, push to GitHub, create a pull request, and merge it into the main branch (usually main) using the terminal and git commands from VS Code.

Before you start, make sure you have the following prerequisites:

- Git
- Visual Studio Code (VSCode)
- Extension VSCode : **Github Pull Request and Issue**

### **Step 1 : Create a New Branch**

1. Open the GitHub repository in VS Code by using the "Clone Repository".  
2.  On VS Code open the Terminal and Run the following command to create a new branch:
    ```
    git branch -c local-branch
    ```

3. Replace `local-branch` with an appropriate name for the branch you want to create.

    ![create Branch](/git-img/Artboard-1.png)


4. Ensure that you are in correct working branch by Running this command :
    ```
    git branch
    ```
    ![Check Branch](/git-img/Artboard-2.png)

5. If you are still in main branch, change your branch to the local-branch by running this command:
    ```
    git checkout local-branch
    ```
    ![Move Branch](/git-img/Artboard-3.png)

#### **Step 2 : Add Files and Commit**
 1. Create or copy the files you want to add to the repository in your local working directory.

2. Go back to the terminal and run the following command to add the file to the list of changes:
     ```
     git add file-name
     ```
     Replace `file-name` with the name of the file you want to add. If you want to add all files at once, use the command :
     ```
     git add .
     ```

     ![Add Files](/git-img/Artboard-4.png)

3. Next, run the following command to commit the changes:
     ```
     git commit -m "Descriptive commit message"
     ```
     Replace `"Descriptive commit message"` with a descriptive message that explains the changes you made.

     ![Commit Changes](/git-img/Artboard-6.png)

### **Step 3 : Push to GitHub**

1.   After committing the changes, run the following command to push the changes to the GitHub repository:

    ```
    git push origin head
    ```
    ![Push Changes](/git-img/Artboard-7.png)

    `push origin head` means that the changes were pushed to the GitHub repository in current working branch.  It prevents you from pushing to the wrong remote branch by accident.

### **Step 4 : Create Pull Request and Merge Branch from VS Code**

1. First you need to install the extension : **Github Pull Request and Issue** into your VS Code.
    ![Install](/git-img/Artboard-8.png)

2. Open the extension and fill the **Title** and **Description** form based on your needs. Then click **Create**.

    ![Push Changes](/git-img/Artboard-9.png)

3. A new pull request will be created, you need to assign the task to someone in your organization or you can assign that to yourself.

4. Make sure you have clean breanch without conflict. You continue by click **Merge Pull Request** and then click **Create Merge Commit**

    ![Open Pull Request](/git-img/Artboard-10.png)
    ![Merge Commit](/git-img/Artboard-11.png)

5. Once you have merged the branch, you can delete the branch by clicking **Delete branch**

    ![Delete Branch](/git-img/Artboard-12.png)

Congratulations! you have been successfully merged `local-branch` into `main` branch on your Github Repository.

## **2. Deployment With Netlify, Custom Domain and Setting DNS with Cloudflare.**
    This documentation will guide you through the process of registering with Netlify, connecting it to your GitHub repository, enabling automatic deployment, and changing the domain. Follow the steps below to complete the task.
### **Step 1: Registration on Netlify**
1. Open https://www.netlify.com/ in your browser.
2. Click the "Sign up" button to create a new account or "Login" if you already have the account. You can choose various options for creating a new account with email, gitlab or bitbucket account.
![Register](/git-img/netlify-1.png)
3. Follow the provided registration steps.
4. After signing up, you will be directed to the Netlify dashboard.

### **Step 2 : Connecting to GitHub Repository**
1. In the Netlify dashboard, click the "Add new site" button.
2. Select "Deploy with GitHub".
3. Grant the necessary permissions to access your repository.
    ![Connect](/git-img/netlify-2.png)
4. Choose the repository you want to connect.
5. Configure the deployment settings according to your needs, such as the branch to deploy and the build command to execute.
    ![Deploy](/git-img/netlify-3.png)
6. Click the "Deploy site" button to initiate the initial deployment process.
7. Once your repository is connected, Netlify will automatically trigger deployments whenever changes occur in your GitHub repository.

### **Step 3: Buy Custom Domain**
    This guide provides step-by-step instructions on how to configure a custom domain. Before proceeding with the steps below, make sure you have purchased a custom domain from Niaga Hoster or any other domain registrar.

1. Open https://www.niagahoster.co.id/ in your web browser.
2. Look for the "Domain" feature on the Niagahoster homepage.
3. Enter the domain name you desire in the domain search box.
Example: yourdomainname.com.
4. Click the "Check now" button to check the availability of the domain.
5. If the domain you want is available, select it and click the "Choose" button.
    ![Choose Domain](/git-img/niaga-1.png)
6. Niagahoster will display additional information about the selected domain, such as price and additional options.
7. Set the domain rental period according to your preference.
8. After you click "Choose" button you will be proceed to the payment process.
     ![Payment](/git-img/niaga-2.png)
9. In the payment page, select the payment method you prefer (such as bank transfer, credit card, or e-wallet).
10. Fill in the required payment information.
11. Double-check your order and ensure that all details are correct.
12. Once you're ready, click the or "Checkout Now" button to complete the purchase.
13. Follow the further instructions from Niagahoster to finalize the payment process. 

### **Step 4: Add Custom Domain to Netlify**
1. In the Netlify dashboard, select the site for which you want to change the domain.
    ![Domain](/git-img/netlify-4.png)
2. Click the "Domain settings" button.
3. Choose the "Add custom domain" option.
4. Enter the domain you want to use.

### **Step 5 : DNS Configuration in Cloudflare**
1. Open https://www.cloudflare.com/ in your web browser.
2. If you don't have an account, sign up for a new account on Cloudflare.
    ![Add Cloudflare](/git-img/netlify-5.png)
3. Add your domain to your Cloudflare account.
4. Cloudflare will provide you with several DNS configuration details that you need to set up.
    ![Domain](/git-img/netlify-6.png)

5. In your domain registrar's service, change the nameservers of your domain to the Cloudflare nameservers provided.
    ![Domain](/git-img/netlify-7.png)
6. Return to the Cloudflare dashboard and select the newly added domain.
7. Configure the DNS by adding the required DNS records according to Netlify's instructions.
For example, add a CNAME record to point the domain to Netlify.

Once the DNS configuration is complete, you will receive email from Cloudflare confirms that your domain has been successfully activated.

Cloudflare will start managing the DNS for your domain. Make sure to follow the specific instructions provided by Cloudflare as the steps may vary slightly depending on their interface.

The process will take a few minutes to complete or in 24 hours maximum.
