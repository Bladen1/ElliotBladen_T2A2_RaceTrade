# README

Contents

1) The Problem

It's not so much what I’m trying to solve as much as it is innovating. Basically building an app where you can unlock a market. For years buying and selling race horses has been an expensive game. Made for the wealthy. Race horses can cost unto 1 million dollars at yearling sales. The average price that horses go for are around 100-200 thousand if you are looking for quality. Yes these prices can be broken down into smaller segments. Race syndicates can have up-to 20 member in them in NSW. For 200 grand horse, that’s still 20 thousand dollars that one has to pay? Thats still crazy expensive and still keeps the little guy out. RaceTrade is about to change this. The beta version which you will see today is a watered down version akin to gumtree. Here you will see how the basics works and all the in and outs the go with it. The alpha version, which will be worked on in the next few months is where the real idea lies. RaceTrade will be a market place where people come and buy and sell tokenised shares of racehorses. It unlocks and creates value in a 10 billion dollar industry. Shares in race horses that were ill liquid and hard to move now have the opportunity in getting sold with the ease of a clicking a button. 


2) Why the problem needs Solving

In the last few years apps like Robinhood and technologies like cryptocurrencies have given the average guy on the street access to participate in the market. This is where RaceTrade is angling their business on. With the advent of smartphones and ease of internet access people who have never been able to get quick access to the Stockmarket have now been able to participate in the Stockmarket. With technologies now being able too tokenise non fungible tokens, the time is now to open up an industry that has been stuck in web 1.0 technologies. 

3) Link to GitHub

https://github.com/Bladen1/ElliotBladen_T2A2_RaceTrade

4) Describition of the market place

The purpose of the site is to match buyers and sellers of racehorses. In todays market there are limited places where one can go and purchase micro racehorse shares. RaceTrade will change by creating an open market place where people can come together to buy and sell racehorses

Functionality will be based on a gumtree site layout. People will be able to post their horses for sale aswell as persuade or in buy horses that are listed for sale. I want to keep the site very clean and simple. A site where were I can scale in the next version of the project. Its important to keep things simple while I learn not only the ins and outs of ruby, but also the ins and outs of how this 2 sided market place will work.

Features will be minimal. Basic Home page where you can sign in and sign out. Once signed in you will either have a chance to Buy or sell. Selling will be redirected to a posting page where once can post the horse they have for sale.

Buying will be redirected to the posting page where all the horses that are for sale will be posted. The buyer will have the opportunity to research further buy selecting the post. The website will then re direct you to a page where you have an image and a detailed post about the horse.

I will build in a strip feature for payment. Will be simple and effective and basically just showcase the ease of use on the site.

Target Audience

There will be 3 types of users

The buyer - People who want to participate in on the industry with the fraction of the cost can now do so. People will be able own a fractionated share of a racehorse without having to pay tens of thousands of dollars to do so

The Seller - People who need access to cash now have the opportunity to do so. With the ability to list there shares of a racehorse online, they can get access to hundred if not thousands of potential racehorses

The trader/Speculator - With every market that gets formed you have speculators. People who try and make money playing both sides of the market

Age/Demographics

Horse racing being a male dominated industry, the site is mostly aimed at men. Thats not to say women will not participate. Their numbers will just be lower than the males. A 80/20 Split is the most likely outcome. Age will cater for a wide spectrum. The average age of a race owner would be 30. The aim of the the app is to get younger people involved. 18-30 is a age where young people are coming up and trying to make a living. Spending 20,000 on a share of a race horse is not possible. 2,000 is. The big advantage is that business dealing will be transacted across the net. Gen Z being the most internet savvy will complement the app and should have no problem interacting and using it. This opens up a market to them that once was never offered before.


TechStack

The software under detained to build the app was as follows

Ruby on Rails - The fundamental piece of software. Layed the foundation for everything.

Ruby - Ruby code embedded in rails

HTML - HTML was embedded in rails

CSS - CSS layout sheets organised the webpage layout

Heroku - Website deployment

Ruby Gems (Discussed in detail in the below paragraphs)

CanCanCan - Authorisation

Devise - Authentication

ActiveStorage - Image upload

Stripe - Payment Method

5) User Stories

User stories will intergrate into our target audience which is the buyer, the seller and the trader. Person1 will be the perspective of the buying type. Person 2 the perspective of the selling type and thirdly  Person 3 from 
the view of the trader

Person 1

As a young person I don’t have too much money. This site is great as its cheap enough to allow me to participate in the great game of horse racing. I’m now able to go watch my horse ran. My makes thinks its great

Person 2

I needed some quick cash. HorseTrade allowed me to sell some shares in my racehorse so I could use them on a Holiday I had planned. Hopefully when I come back I can re-invest and participate once again	

Person 3

Never before has a market being created for racehorses. There was a giant discrepancy in the market for one of the horses. I was able to buy some shares. They have doubled in 2 weeks.

6) Wireframes

Please view the the docs folder

7) ERD/Database Design Scheema

Please view the docs folder

The database schemes was setup with simplicity at its core. There are 3 main relationships working together on the site. The first main database schema is User. The user has all its usually components like email and password but is extriecaplabl linked to the users post. These are the sellers on the site. The seller list there horse for sale and will be required to fill out a heap of attributed relating to the sale of the horse. These include title of the horse, body of information, shares and price. It is linked with an image post of the horse.


8) High level Components and Project Models

MVC

The main controller consist of the post controller. Posting or buying or selling is the main function of the site. This controller regulates and updates any models that need to be changed. The main models that would contitually get updating are new and exisiting users who enter the site. Also new buy and sell updates/post is the main models that would be updated through the controller. I did add in the a pay controller at the end. It is half set up on the front end to show how shares could be purchased. It was not wired in on the backend so no changes would be made to the charges model. The main views to interact with both the model and controller are the home page, the buy page and the sell page. All these pages would get uploaded differently each time for model fetches different data.

CanCanCan (Admin)

The administrative or authorisation stack I chose to use CanCanCan. The gem installed allowed me to work with my authentication model and database systems. It was a massive help as it allowed me to switch and off links on the website on who and who could not view certain links on the web page. For example. Users who were the author of the post(sellers of the horse) were able edit their post at any time. If a post wasn’t issued/authored by them, no link appeared for them to edit their post. Even if it there was, access would still be denied. These links were shown on the detailed buy page and also the post page were all the shares of the horses were shown.

Devise (Authentication)
Devise was the gem I decided to use to create all my user models. It was a simple and easy gem to install. The gem allowed me give user authtiations with user_ids passwords and password retrievals. The users models interrelated with the post models as such so the post could be linked with a specific user on the website. 


Stripe(Payment)

The implementation of stripe was a simple front end interface for the user to interact with payment. I did not have time to construct the backend but installed the front end interface to give the user a feel of what to expect. Down the line on the main version I will have the stripe interface work with the user models.

ActiveStorage(Image upload)

Active storage was a unique component of the post models. The website need to have access to image upload so the users of the site could get a visual experience of what they were buying. The gem I used for this part of the project was active storage. I linked the gem to the post models as to give the post a unique id that the post could be related too.

9) Database Relations. (Please refer to the ERD)

One to One

Each user has a unique identifer. This unique indentifer is their email address. Each user id has a unique email address and each email address had a unique id. one to one

One to Many

A user in the system can make as many sell post as he/she likes. Each user ID or email indefify can have many sell posts. On the flip side it is a many to one relationship.Many sell posts can have only one unique identifer.




