# AWS-EC2-Website-Hosting




 # Project Implementation:

A.Setting Up Your EC2 Instance:

![image-125-1024x366](https://github.com/user-attachments/assets/562f0889-4847-4fc2-8e23-798242646dda)

When hosting your website, you need a virtual server on the cloud. AWS provides an EC2 instance as the virtual server.

To set up an EC2 instance, you will create a virtual machine (to host your website) in the cloud that you can access remotely. With an EC2 instance, you can install the server software and applications you need to host your website.

A. Open your favorite web browser, and sign in to your AWS Management Console.

B. Next, search for and select EC2 from the result list to navigate to the EC2 console.


C. On the EC2 console, click Launch Instance, and choose Launch Instance to begin creating your EC2 instance.


![image-126-1024x751](https://github.com/user-attachments/assets/2e87e95f-9088-4dd5-8276-4784e56b359b)


4. Configure the following Name and OS Image for your EC2 instance:

![image](https://github.com/user-attachments/assets/839d1f01-4318-4572-92c0-ce2fc7d0b0e9)
   

5. Scroll down and choose the Instance type that best suits your needs for hosting your website.

AWS offers a variety of instance types, ranging from the small (micro) size to the powerful xlarge size. The free tier t2.micro instance type is sufficient, but you may need to select a more powerful instance type as your website grows.

![image](https://github.com/user-attachments/assets/0238bf85-248a-49c3-9271-15ae70c396d3)



6. Next, select an existing security group under the Network settings section or create a new one. Security groups act as virtual firewalls to secure your instance from unauthorized access.

This tutorial uses the default security group, as shown below.

![image](https://github.com/user-attachments/assets/e12ae64b-7c41-4a7f-b65e-0a517f92b4f4)



7. Keep other settings as default, and click Launch under the Summary section (right pane).


![image](https://github.com/user-attachments/assets/dc891171-84c3-46a7-8eed-9d91c81102cf)


8. Lastly, navigate to the EC2 console, and you will see your new instance in the list, as shown below.

![image](https://github.com/user-attachments/assets/10d995c4-cbb7-45f3-99ec-19c80c66be8b)


Congratulations! You have successfully set up an EC2 instance to host your website.


B. Installing a Web Server to Host a Website on AWS EC2:
With your EC2 instance set up, you now need a way to deliver web content to users over the internet, a web server. As a software program, a web server on your EC2 instance allows you to host your website and make it accessible to users.

Many different web server options are available, including Apache, NGINX, and Microsoft IIS. But this tutorial uses Apache, one of the most popular and widely used web servers, open-source and highly configurable.

Related:
How to Install Apache on Ubuntu to Manage your Traffic

To install Apache as the web server on your EC2 instance, follow these steps:

1. On your Instances page, tick the box next to your EC2 instance, and click Connect to connect to the selected EC2 instance.

![image](https://github.com/user-attachments/assets/9d13362a-9880-4d55-9415-10bb4c87c405)



2. Next, keep the settings as default, and click Connect, which opens a console window where you can run commands to your EC2 instance remotely.


![image](https://github.com/user-attachments/assets/4665e92d-87aa-43f7-a22f-ec173013323b)




The output below signifies you have successfully connected to your EC2 instance.

![image](https://github.com/user-attachments/assets/2e197cc0-d365-4463-b4d0-143326c768fc)




3. Run the below command to gain root access and fully control your EC2 instance. Doing so lets you make any necessary changes or modifications to your web server.



sudo su
Once you gain root access, your prompt changes, like in the screenshot below.


![image](https://github.com/user-attachments/assets/9274f38d-30d5-4f0b-a979-c3d77de5ea7e)



4. Now, run the following yum command to update the list of available packages. This command ensures you have the latest version of packages and security updates.

![image](https://github.com/user-attachments/assets/435bf8f5-eb67-48f9-9f0d-8adb3a564fe7)


yum update -y

5. Once updated, run each command below to install the Apache web server (httpd) and the PHP 8.0 (php8.0) package from the amazon-linux-extras repository.


![image](https://github.com/user-attachments/assets/065c63d5-d264-40a1-8224-ab15fd2b3f44)

yum install httpd -y
sudo amazon-linux-extras install php8.0 -y

6. Now, run the below service commands to start the Apache web server (httpd) and check its status.

   
![image](https://github.com/user-attachments/assets/0b655a17-35f0-493a-ae52-5c7566397115)



7. Finally, open the Public IPv4 DNS of your EC2 instance in a new browser tab to request web content from the Apache web server.


![image](https://github.com/user-attachments/assets/518f17a0-e170-4713-832f-713bca5e78f5)


8. Website is live on web server :

   
![Screenshot 2024-12-12 081458](https://github.com/user-attachments/assets/d7bd8aba-5c30-4b6b-b91c-22c2476398e1)

   

