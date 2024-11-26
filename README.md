# What is the Cloud Resume Challenge and why did I do it?

The Cloud Resume Challenge is a project that has the goal of helping whoever completes it gain skills in cloud computing, web development, and infrastructure management. To complete this challenge, I had to create a fully cloud-hosted resume with a visitor count that automatically updates using different AWS services, including S3, Lambda, DynamoDB, code the resume in HTML, as well as set up automation and the infrastructure through Terraform.

I decided to take on this challenge to start learning more about what is the “cloud.” Whenever reading news articles or any technological development, there is always mention of “cloud computing” or networking and while I had a slight understanding of these two items, I did not really understand them in depth. This project offered me the opportunity to not only learn about the cloud from a conceptual level but also create something tangible and have a portfolio piece that I can look at and show future employers. Completing the Cloud Resume Challenge not only helped me accomplish my goal but also gave me the motivation to continue my learning about this technology that is so central to our lives.

# Services Used and What They Were Used For

The Cloud Resume was broken up into three different components: the frontend, backend, and the infrastructure. Bucketing this challenge into three separate parts helped not only with understanding what each of the specific services is used for and how they interact with the other ones, but it also helped with troubleshooting any errors that came about. For all these steps, I used Continuous Integration and Continuous Development through GitHub Actions to publish it to a public repository. This helped me automate the development process.

## 1. Frontend: This was used to display the resume as a static website, what the end user would see.

- **HTML & CSS:**
  - I started with the HTML file as this would be what the end user is seeing. To help with the coding of this and the styling, I utilized the help of Claud AI to get a professional looking website.
  
- **AWS S3:**
  - I had to deploy it as a static website on AWS S3 to host the resume online. This service was both cost-effective as well as scalable, making sure the resume could be accessed whenever.
  
- **CloudFront:**
  - I used CloudFront to cache my website and to make sure it was secure over HTTPS.
  
- **AWS Route 53:**
  - After buying the custom domain name (samuelnielsen.com) from Namecheap, I linked the website using Route 53. To do this, I ensured that the domain name would point to my CloudFront cache, making accessing the website both easy and fast.

## 2. Backend: This managed the dynamic part of the website, specifically the visitor count.

- **AWS Lambda:**
  - I implemented a serverless function with AWS Lambda to manage the visitor count. The function was written in Python and executed every time the site was accessed.

- **DynamoDB:**
  - I used DynamoDB, a NoSQL Database, to store and retrieve the visitor count data.

- **API Gateway:**
  - This was used as the interface between the front and backend. It triggered the Lambda function to get to work and update the visitor count on the front end.

## 3. Infrastructure as Code

- **Terraform:**
  - To automate the deployment of cloud resources, I used Terraform. This tool allowed me to define the AWS resources in my configuration, ensuring that the environment could be replicated or modified easily, reducing human error, and speeding up the deployment process.

# Challenges I Faced

The project was not without its challenges, which improved my troubleshooting skills. Two of the main issues that I faced helped me not only understand what issues I might face on the job but also gave me a better understanding of my computer’s systems.

- **Command Line Issues:** I faced problems running certain functions through the command line, even with administrator privileges. This led me to explore firewall settings and BIOS adjustments, which was a new area for me.

- **Simple Fixes:** Many problems, such as a typo in the Lambda function or needing to invalidate the CloudFront cache, turned out to have simple solutions. This experience reminded me that oftentimes most problems have a simple fix.

# What I Learned and Reflections on This Process

This project has easily been the most impactful that I have taken on during my undergraduate career. Not only did it provide hands-on experience with the services listed above, but I also learned troubleshooting, and the initial parts of automation which I plan to continue learning about to become more efficient professionally.

Additionally, this project highlighted the importance of security. Setting up MFA and managing IAM roles on AWS showed me how easy it was to skip this step but also how important it is to protect your personal information and user data.

# Conclusion

After completing this challenge, I feel confident not only in my understanding of the cloud and what it is, but I also am confident in the skills that I have gained from this to go forward and take on new projects.

Looking forward, I not only plan to continue to build out new features on my cloud resume such as a geo tracker and more analytics, but I also plan to continue working within AWS to build new projects. The lessons and skills that I learned from this challenge will help me with whatever avenue I decide to pursue both after college and with future technical projects.

Check out the website here(http://samuelnielsen.com/)! And please check out the other repositories below!

- [Frontend](https://github.com/sambidiah/cloud_resume_frontend)
- [Backend](https://github.com/sambidiah/cloud_resume_backend)
- [IaC](https://github.com/sambidiah/cloud_resume_infrastructure)
