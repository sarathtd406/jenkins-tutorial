## Jenkins with CI/CD pipeline

#### Learn how to setup jenkins container, create CI/CD pipeline with Git repository, commit code to Git and trigger build.


#### Let's get started !!

Jenkins runs on Java, you need either latest version of Java Development Kit (JDK) or Java Runtime Environment (JRE).

- Open a command prompt by typing cmd in the search bar and press Enter.
- Run the following command:
```java -version```

![image](https://user-images.githubusercontent.com/84066151/170506498-31b4f64d-ea78-48f8-a9c1-12f7494d846f.png)

If Java isn't installed, the output is a message stating that Java isn't recognized as an internal or external command.

### Download Java
Download the latest Java Development Kit installation file for Windows 10 to have the latest features and bug fixes.

- Using your preferred web browser, navigate to the [Oracle Java Downloads page](https://www.oracle.com/java/technologies/downloads).
- On the Downloads page, click the x64 Installer download link under the Windows category.

![image](https://user-images.githubusercontent.com/84066151/170507901-cc93af1b-1eb7-4cac-8ac5-d7b522555ad0.png)


### Install Java

Step 1: Run the Downloaded File
Double-click the downloaded file to start the installation.

Step 2: Configure the Installation Wizard. (follow the configuration wizard with default settings)

### Set Env Variables

**Step 1**: Add Java to System Variables

1. Open the Start menu and search for environment variables.

2. Select the Edit the system environment variables result.

![image](https://user-images.githubusercontent.com/84066151/170520130-73d4fe6e-3b6d-4004-a580-8aab48757285.png)

3. In the System Properties window, under the Advanced tab, click **Environment Variable**

![image](https://user-images.githubusercontent.com/84066151/170520332-44b6d5cf-54ff-4ce2-8dda-07855850c599.png)

4. Under the System variables category, select the Path variable and click Edit:

![image](https://user-images.githubusercontent.com/84066151/170520678-ed52d4d4-816a-438f-81d2-6d74d4779f27.png)

5. Click the New button and enter the path to the Java bin directory:

![image](https://user-images.githubusercontent.com/84066151/170521052-a3a2899f-9d21-46af-aab3-6cf69d1f4f19.png)

6. Click OK to save the changes and exit the variable editing window.


**Step 2**: Add JAVA_HOME Variable

Some applications require the JAVA_HOME variable. Follow the steps below to create the variable:

1. In the Environment Variables window, under the System variables category, click the New… button to create a new variable.

![image](https://user-images.githubusercontent.com/84066151/170521370-849c9955-8b58-43df-804d-1b8e23f91683.png)

2. Name the variable as JAVA_HOME.

![image](https://user-images.githubusercontent.com/84066151/170521817-da7aec1b-d1f8-4844-8c16-b7e4ab01d202.png)


### Verify Java Installation

- Run the following command:
```java -version```

![image](https://user-images.githubusercontent.com/84066151/170522262-756b59b3-c522-47d3-a195-07c17fa75f3b.png)


### Install Jenkins

1. Download official Jenkins from [download page](https://www.jenkins.io/download/). 

![image](https://user-images.githubusercontent.com/84066151/170524843-4a1630de-0139-4050-8e11-9fc381e76734.png)

2. Once the download is complete, run the jenkins.msi installation file.

3. The setup wizard starts. Click Next to proceed.

![image](https://user-images.githubusercontent.com/84066151/170525724-2914db4a-5e74-42e2-8afb-f975975847d9.png)

4. Select the install destination folder and click Next to continue.

![image](https://user-images.githubusercontent.com/84066151/170525886-b0cc4049-5334-4ce2-9b37-2be2f38df38b.png)

5. Under the **Run service as a local or domain user option**, enter the domain username and password for the user account you want to run Jenkins with. Click **Test Credentials** to verify the login data, then click **Next** to proceed.

![image](https://user-images.githubusercontent.com/84066151/170528165-2ed6986c-3966-472a-8d83-cc7f1a7be883.png)

6. Enter the port number you want Jenkins to run on. Click **Test Port** to check if the selected port is available, then click **Next** to continue.

![image](https://user-images.githubusercontent.com/84066151/170528556-889e0228-5a61-4a0a-b46b-4aff3c2bd139.png)

7. Select the directory where Java is installed on your system and click Next to proceed.

![image](https://user-images.githubusercontent.com/84066151/170528834-9bb5b1ee-e5f2-497a-b71a-ffd8d8e732dc.png)

8. Select the features you want to install with Jenkins and click Next to continue.

![image](https://user-images.githubusercontent.com/84066151/170528962-4d67a0c9-ff72-4147-aa56-37b299a2f4f0.png)

9. Click Install to start the installation process.

![image](https://user-images.githubusercontent.com/84066151/170529091-62772ada-bc4d-4203-a1b2-f1d1a3eb1cea.png)

10. Once the installation is complete, click Finish to exit the install wizard.

![image](https://user-images.githubusercontent.com/84066151/170529220-00e5586c-31cd-4658-97af-249de2f81ddc.png)



![image](https://user-images.githubusercontent.com/84066151/170546510-b68cd268-041e-4474-a5bc-e9300d9d7ab9.png)


### Login to Jenkins

1. Let's open up the browser and type ```localhost:8080```. This is the port we exposed our jenkins.

2. Copy and paste the password generated during jenkins initialization under Administrator password and click on continue.

"C:\ProgramData\Jenkins\.jenkins\secrets\initialAdminPassword"

###  Getting Started Jenkins

Now, we are in the Jenkins Getting Started page as shown below. Let's select **Install suggested plugins** by jenkins community. 

Even you can know the jenkins version mentioned at the bottom of this page. **Version - Jenkins 2.332.3**

<img width="1144" alt="image" src="https://user-images.githubusercontent.com/84066151/168869366-a98a7bc5-e7b7-4d7e-8d72-96ebb194b5cc.png">

**Wait until the plugins are installed. **

<img width="1177" alt="image" src="https://user-images.githubusercontent.com/84066151/168870697-e0ce6139-5ae4-4154-9776-2e4d9a379602.png">

We can install other plugins later as well.


### Create Admin user 

As shown in below image,

1. Enter username
2. Enter password
3. Enter full name
4. Enter email id

Click on **Save and Continue**

<img width="1155" alt="image" src="https://user-images.githubusercontent.com/84066151/168871607-3a951b2a-6f1b-4c3a-9efd-f7d1b3041498.png">


### Set Instance URL

Let us leave the default URL setting and click on **Save and Finish**

<img width="1133" alt="image" src="https://user-images.githubusercontent.com/84066151/168872166-615320ce-61db-41a7-8ef9-18a91b17ccf4.png">

### Ready to use

Click on **Start using Jenkins**

<img width="1157" alt="image" src="https://user-images.githubusercontent.com/84066151/168872400-fac7f418-b78f-4f8d-afe1-b1aaa9870859.png">


**Welcome to Jenkins**

<img width="1432" alt="image" src="https://user-images.githubusercontent.com/84066151/168872577-6dbdf5ef-f511-4828-b0fd-604bd408efb9.png">


### Create Multibranch pipeline with Git




### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/sarathtd406/jenkins-tutorial-101/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
