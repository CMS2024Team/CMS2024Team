# Deployment Process 

## Project Development & Deployment Workflow

This document outlines the step-by-step process for developing and deploying the JCUB Students Board WordPress site. It includes guidelines on setting up the new environment,
and deployment strategies to ensure a smooth running of the site.

## Tools and Techniques Used

### 1. Project Management

#### a) Slack
- Utilized for team communication and document sharing.
- https://cms24jcu.slack.com/archives/C07CAMVJB3L


#### c) GitHub
- Code hosting, version control, and issue tracking.
- https://github.com/CMS2024Team/CMS2024Team/

#### d) WhatsApp
- Used for coordination, quick message relay and responses, and discussions.

### 2. Version Control

- **Tool:** GitHub
- **Hosting:** cloudaccess
- **Domain:** https://jcu-student-board.cloudaccess.host/

**Branching Strategy:**
- **Master/Branch (site):** Reflects the production-ready state, serving as the deployment branch for the live site.
- https://github.com/CMS2024Team/CMS2024Team/tree/master
  
- **Main/Branch (site):** Integration branch for ongoing development.
- https://github.com/CMS2024Team/CMS2024Team/tree/main

---

## Testing

### Visualization of Theme and Testing

- Custom theme created with PHP, JavaScript, and CSS.
- Implement changes in a controlled manner to ensure they do not adversely affect user experience.
- Check responsiveness, layout, and functionality across different devices and browsers.

### Plugin Update and Testing

- Test compatibility and impact of plugins before updating.
- Create a backup and test updates on a staging site.
- Apply updates on the live site after verification to ensure smooth functionality.

### Content



---

**Deployment Process**

To install and run this site successfully, You need to do the following:
We have given two options to choose from. These options are:
1. Importing the WordPress XML file provided on the GitHub repository
2. If you find it difficult to perform **Option 1 ->** to import the XML file on your new WordPress project then do the following:
    1. Clone the repository. The repository link is: https://github.com/CMS2024Team/CMS2024Team.git
    2. We believe you already have a domain. Now, you need to upload the files you downloaded earlier to your new domain name.
    3. Go to the CPanel of your domain and create a database and a database user. Grant all the root privileges to the user. 
    4. The downloaded package includes WordPress installation as well. This means you don’t need to install WordPress on your new domain.
    5. First, connect to your domain name using an FTP client. Once connected, make sure that the root directory of your website is empty.
    6. After that, you can upload the archive and installer files to the root directory. This is usually called public_html.
    7. Once both files have finished uploading, you are now ready to unpack WordPress.
    8. Open a new browser tab and go to the following URL: http://"your_domain"/installer.php
    9. The installer will look for the archive file and then automatically select options for you on the screen.
    10. Scroll down a little to enter the information for the database you created in the previous step.
    11. Duplicator will now attempt to connect to the database using the information you provided.
    12. Upon success, it will show you a Validation Pass. Otherwise, it will show you a warning with details on how to fix it.
    13. Duplicator will now start importing your WordPress website. Once finished, you will see a success message with an Admin Login button.
    14. Duplicator will automatically update URLs to your new domain name. You can now click on the ‘Admin Login’ button to complete the next steps.

  ** In case you experience Error 301, Do the following:**
  Edit the WordPress .htaccess file

This will be located in the same directory as your wp-includes or wp-admin folder. Open the .htaccess file and paste the following lines of code at the very top:

#Options +FollowSymLinks
RewriteEngine on
Unchanged: RewriteRule ^(.*)$ http://www."your_domain".com/$1 [R=301,L]

Hurray!!!! You are good to Go. 

## Web Pages Development & Deployment

### Responsibilities:

- **Paul Kemboi:**
  - Home, Events, News & Updates.

- **Timothy Kipkosgei:**
  - About Us, Services, Get Involved.

- **Victor Kipkosgei Rutto:**
  - Contact Us, Resources.
 
- **Anthony Kibet Metto:**
  - Contact Us, Resources.

- **Zadok Kipkemoi:**
  - Contact Us, Resources.

### Design Responsibilities:


- **Site Map:** Jashan

### Testing Responsibilities:

- **Theme Developer & Tester:** Paul Kemboi
- **Web Pages & Content Tester:** 
- **Site Map Tester:** 
-** Plugins, Github Master and Documentation **: Timothy Kipkosgei

---

## Automation

### CI/CD Pipeline
 
- CI/CD automates the process of integrating code changes and deploying applications, ensuring faster delivery and higher quality. 
- It enables continuous testing and monitoring, allowing teams to identify and resolve issues quickly.

**Conclusion:**
This documented workflow serves as a guide for new users to successfully contribute and add updates, test changes, and deploy them seamlessly for the James Cook University Brisbane Student Board.
