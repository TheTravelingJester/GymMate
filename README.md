# GymMate

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
GymMate is an application that helps people find workout buddies near them. Users can anonymously swipe through other users profiles and send friend requests. Users can chat with their friends and motivate each other by challenging each other at the gym.    

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:** Fitness Social Media
- **Mobile:** iOS Devices
- **Story:** Many people have gained some quarantine weight the past year and are struggling to lose it because it is so easy to lose motivation when we are all stuck at home. GymMate connects people with workout partners which will help people stay motivated and focused so they can reach their goals together!
- **Market:** Free/Paid Plans, Ads 
- **Habit:** GymMate is an app that people would use daily to meet and chat with other Gym Mates. 
- **Scope:** Our goal is to get 100 people to register an account and use our application. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can resister a new account
* User can Log On
* User can find Gym Buddies
* User can add Gym Buddies as Friends
* User can chat with friends
 

**Optional Nice-to-have Stories**

* User can create a calender view to schedule training at gym
* User can post pictures onto feed 

### 2. Screen Archetypes

* Register/Login
   * User can Register or login
* GymMate Finder  
   * Gymmate finder section a map with your location as well as gyms around ur area
* User Profile
   * user can swipe through other users who are looking for a gym mate and send friend requests
* Chat 
   * Chat section allows user to chat with friends and schedule gym training appointment

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Register or login
* GymMate finder - swipe through users looking for gym mate
* Profile
* chat section - chat with friends

**Flow Navigation** (Screen to Screen)

* Register or login
  * profile
* GymMate finder
  * Send Friend Request
  * Chat 
* Profile
  * calender with upcoming gym appointments
* chat section
  * User Profile
  * Gym Mate Finder

## Wireframes
[Add picture of your hand sketched wireframes in this section]
<img src="https://user-images.githubusercontent.com/69356399/114112182-dbd50d80-98a9-11eb-9cc5-1d39487fb139.png" width=600>

### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 
### Models

#### User Account
|Property |Type	|Description|
|---------|-----|-----------|
|username|String|unique username|
|password|String|user selected password|
|userProfilePicture|File|user selcted profile picture|
|userGym|String|user selected gym|

#### Friend
|Property |Type	|Description|
|---------|-----|-----------|
|friendRequest|Pointer|pending requests|
|friendAccept|Pointer|accpeted friends|

#### Chat
|Property |Type	|Description|
|---------|-----|-----------|
|objectId	|String	|unique id for user chat|
|author	|Pointer |person sending the message|
|text|String	|the message itself|
|recipient|Pointer|person receiving the message|

#### Posts
|Property |Type	|Description|
|---------|-----|-----------|
|objectId	|String	|unique id for the user post (default field)|
|author	|Pointer |to User	image author|
|image	|File	|image that user posts|
|caption	|String	|image caption by author|
|commentsCount|	Number	|number of comments that has been posted to an image|
|likesCount	|Number	|number of likes for the post|
|createdAt	|DateTime	|date when post is created (default field)|
|updatedAt	|DateTime	|date when post is last updated (default field)|


### Networking
- So far we have implemented the design of the Signin and Signup Page and will implement authentication by sending request to firebase to validate the Username and password that has been inputted to retrieve the users account.
- Get Request for Authentication during Sign in. 
- Post Request for registering a user and storing the users profile on firebase.
- Update Request for updating user profile. 
![Screen Shot 2021-04-15 at 10 50 57 PM](https://user-images.githubusercontent.com/69356399/114964608-122c0300-9e3d-11eb-8299-d263d0c757e1.png)

