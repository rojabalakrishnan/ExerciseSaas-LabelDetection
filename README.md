# ExerciseSaas-LabelDetection

The application requires users to upload an image, after uploading the image is sent to _Google Cloud Vision API_ which detects and classify multiple objects within the image as labels.

## Table of Contents
1. [Create Java Maven Project](#1-create-java-maven-project)  	
2. [Configuration Set up in Google Cloud Console](#2-configuration-set-up-in-google-cloud-console)
3. [Create Application Access Page and its corresponding servlets](#3-create-application-access-page-and-its-corresponding-servlets)

<br>

## 1. Create Java Maven Project

Create a Maven Java project in eclipse. Add the necessary dependencies in the <i>pom.xml</i>.<br>
google-cloud-vision - artifact is necessary for detecting labels.

## 2. Configuration Set up in Google Cloud Console
#### 1. Create a new project. <br>
![Project Creation](https://github.com/rojabalakrishnan/ExerciseSaas-LabelDetection/blob/main/Images/Screen%20Shot%202020-11-09%20at%205.25.14%20PM.png) <br>
#### 2. Enable Vision API. <br>
![Screen Shot 2020-11-09 at 5.25.49 PM.png](https://github.com/rojabalakrishnan/ExerciseSaas-LabelDetection/blob/main/Images/Screen%20Shot%202020-11-09%20at%205.25.49%20PM.png)<br>
#### 3. Grant Service account to access the project.
![Screen Shot 2020-11-09 at 5.26.58 PM.png](https://github.com/rojabalakrishnan/ExerciseSaas-LabelDetection/blob/main/Images/Screen%20Shot%202020-11-09%20at%205.26.58%20PM.png) <br>
#### 4. Authenticating with Service account.
![Screen Shot 2020-11-09 at 5.27.22 PM.png](https://github.com/rojabalakrishnan/ExerciseSaas-LabelDetection/blob/main/Images/Screen%20Shot%202020-11-09%20at%205.27.22%20PM.png) <br>
#### 5. Verify the Service Account status.
![Screen Shot 2020-11-09 at 5.27.42 PM.png](https://github.com/rojabalakrishnan/ExerciseSaas-LabelDetection/blob/main/Images/Screen%20Shot%202020-11-09%20at%205.27.42%20PM.png) <br>
#### 6. create a key to request the vision api from your application.
![Screen Shot 2020-11-09 at 5.27.56 PM.png](https://github.com/rojabalakrishnan/ExerciseSaas-LabelDetection/blob/main/Images/Screen%20Shot%202020-11-09%20at%205.27.56%20PM.png) <br>

## 3. Create Application Access Page and its corresponding servlets
 <b>Home.jsp</b> - Allows you to upload an image.<br>
 <b>Upload.java</b> - It's a servlet which recieves the request. Upon receiving the request, the image is converts as blobbytes and is processed in the method getImageLabels() to fetch its labels using the google cloud vision api. The fetched results are redirected to the view - Labels.jsp<br>
 ![Screen Shot 2020-11-09 at 8.20.22 PM.png](https://github.com/rojabalakrishnan/ExerciseSaas-LabelDetection/blob/main/Images/Screen%20Shot%202020-11-09%20at%208.20.22%20PM.png) <br>
 <b>Labels.jsp</b> - Returns the view of the image with its corresponding labels   
 ![Screen Shot 2020-11-09 at 8.20.56 PM.png](https://github.com/rojabalakrishnan/ExerciseSaas-LabelDetection/blob/main/Images/Screen%20Shot%202020-11-09%20at%208.20.56%20PM.png) <br>
