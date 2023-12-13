# flask_5_tailwind

## Cloud CDN & Video Hosting 

### Create a Storage Account on Azure

<img width="1132" alt="Screenshot 2023-12-12 at 22 03 42" src="https://github.com/ktdutta/flask_5_tailwind/assets/141374153/e973165b-fa85-493c-9c56-156de795024b">


### Create a Container 

This container will basically act like a drop box where we have the ability to upload and store different types of data formats. In this assignment we will be using this container to store the video we would like to host in our CDN. 

<img width="1140" alt="Screenshot 2023-12-12 at 22 19 47" src="https://github.com/ktdutta/flask_5_tailwind/assets/141374153/586696d2-1cd4-48b6-b296-aac967e65d7b">


### Create CDN 

Create a front door endpoint by going to the Front Door and CDN tab on the Security + Networking menu on the left side and creating a CDN. This CDN will host the video as our flask application. In order to host the video the endpoint hostname followed by the file being hosted. 

Here is the link of the CDN hosting the video being used for the created Flask Application: 
https://kd-cdn.azureedge.net/keerthana-flask-app/Welcome%20Back,%20Seawolves!.mp4

<img width="1440" alt="Video Hosted in CDN" src="https://github.com/ktdutta/flask_5_tailwind/assets/141374153/a47933b2-2fa9-4f8e-8265-c3b7de3253b4">


## Flask App with Tailwind CSS

I created a Flask Application which is a Welcome to Stony Brook University webpage. Within the webpage in the header I created two tabs to direct the user to more information regarding Stony Brook University: About and Campus. I originally attempted to navigate the ‘About’ tab to the official stonybrookuniversity.edu website however the website was not allowing me to connect this to my web application. Instead I decided to have the ‘About’ tab to navigate to the Stony Brook University wikipedia page. Additionally, I also had the ‘Campus’ tab navigate to the campus digital map. 

To add to the application in the body, I decided to host a Welcome to Stony Brook University video I downloaded from the Stony Brook University youtube page on the CDN I created. I then added this video to the webpage. 

In the footer I decided to add the Stony Brook University Logo in order to make the website seem more official. 

I used tailwind in order to help design the website to make liking by experimenting with color, font, spacing, and more. 

<img width="996" alt="tailwind" src="https://github.com/ktdutta/flask_5_tailwind/assets/141374153/0a333b3d-1e8e-42ef-b670-e3f77c0a7715">


## Cloud Deployment 

#### Installing Azure CLI 


```curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash```

#### Check Installation 


```az```

#### Giving Shell Permission to connect with Microsoft Azure Account 


```az login --use-device-code```

  It will ask for your password followed by an authentication code to sign into Microsoft Azure


##### Subscription IDs


```az account list --output table```


#### Set the Appropriate Subscription Name (Azure for Students)


```az account set --subscription (insert subscription ID)```


#### Deploy Application Using Azure 


```az webapp up --resource-group (insert group name) --name (insert your app name) --runtime <(Insert language)> --sku <(insert service plan)>```


## Documenting Errors

After completing the deploying process I accessed the link to my deployed application however I kept running into a 500 internal server error. 

<img width="990" alt="Server Error" src="https://github.com/ktdutta/flask_5_tailwind/assets/141374153/74ef7afa-5bc7-4b5f-9eda-c04b4598a15a">


In order to troubleshoot I tried to run and deploy the flask application with the message ‘hi’ instead of rendering it to the index_tailwind.html file. When I did this the flask application ran fine, which tells me there must be an issue with the code in the index_tailwind.html file which I am in the process of identifying. 
