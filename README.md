# ExerciseSaas-LabelDetection

## Table of Contents
1. [Create Java Maven Project](#1-create-java-maven-project)  	
2. [Configuration Set up in Google Cloud Console](#2-configuration-set-up-in-google-cloud-console)
3. [Create Application Access Page and its corresponding servlets](#3-create-application-access-page-and-its-corresponding-servlets)	

<br>

## 1. Create Java Maven Project

Create a Maven Java project in eclipse. Add the necessary dependencies in the <i>pom.xml</i>.<br>
google-cloud-vision - artifact is necessary for detecting labels.

## 2. Configuration Set up in Google Cloud Console
1. Create a new project.
![Project Creation](readMePics/image1.img) <br>
2. Enable Vision API.
3, Grant Service account to access the project.
4. Authenticating with Service account.
5. Verify the Service Account status.
6. create a key to request the vision api from your application.

## 3. Create Application Access Page and its corresponding servlets
 <b>Home.jsp</b> - Allows you to upload an image.<br>
 <b>Upload.java</b> - It's a servlet which recieves the request. Upon receiving the request, the image is convertes as blobbytes and is processed in the method getImageLabels() to fetch its labels using the google cloud vision api. The fetched results are redirected to the view - Labels.jsp<br>
 <b>Labels.jsp</b> - Returns the view of the image with its corresponing labels   
