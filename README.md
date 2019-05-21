# Intro to APIs & Axios

## In this lesson we'll learn
- Basic differences between clients and servers
- Introduce the concept of HTTP GET requests
- Introduction to APIs
- Introduction to asynchronous JS and Axios
- Make our first GET request with Axios

## Clients and Servers
The world wide web is basically just an interconnected network of client devices and servers. 

We use the word **"client"** to refer to a computer connected to the internet that is being used by a human. Clients would include your laptop, your smart phone, your Apple TV, etc. 

![](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/Client-server-model.svg/1200px-Client-server-model.svg.png)

A **"server"** is a computer who's primary purpose is just to store data. Humans don't normally interact with a server directly, so they have almost no interface. They often kind of ook like a VCR:

![](https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcRBQ6I4NzSHMvx7Wrdyy4BfY-HV1pY5Iji10WFRDs1AxPfvv8BgRoNPCDEM-pLNaRaIwlAr8LPzvS89M5xTKOY6g0aWKjRhNdsuy9zaZ99eWFLgffpM2Il-Zw&usqp=CAc).

You may be more familiar seeing them stacked in a cluster, like this:
![](https://5.imimg.com/data5/FD/SW/MY-37259883/computer-server-500x500.jpg)

## HTTP Requests
Client computers have interfaces with which humans can interact. When people are using such a device to interact with an app, these interactions can be boiled down to four core actions:
- Creating new data
- Reading existing data
- Updating existing data
- Deleting existing data

Apps that allow users to do these four actions are known as CRUD apps.

#### WE DO: What are examples of each of these 4 CRUD actions on Facebook?

When we perform one of these four CRUD actions, we're making a an HTTP request to a server to fulfill our specified action. HTTP stands for **H**yper**T**ext **T**ransfer **P**rotocol. You can think of HTTP as a set of rules for transferring data over the web. There are four types of HTTP requests that connect with our four user interactions:

- POST request == Create data
- GET request == Read data
- PUT request == Update data
- DELETE request == Delete data (whoa! who knew!?!)

![](https://res.cloudinary.com/briandanger/image/upload/v1558470312/Screen_Shot_2019-05-21_at_4.24.21_PM_jgcf1q.png)

The server will "respond" with either a success or error message and by either doing or not doing the action requested. There are a number of factors affecting success that we will discuss at greater length in the future.

We'll need to wait until we learn backend database languages before we can Create, Update, or Delete data from a database; however, fortunately, we can Read existing data with just JavaScript, so for now, we'll focus on how we can us JS to request data from servers that our users can read, watch, and listen to.

## APIs
APIs are basically databases hosted on web servers that have data that is available for public use. This may not sound particularly exciting at first, but APIs are actually one of the most useful tools in web development.

#### API Example - OpenWeatherMap
Imagine you're building a hiking app. You might want to have information about the weather available when your users are planning when and where they're going to hike. Without access to a weather database, providing this information to your users would be nearly impossible. 

Fortunately, we have [the Weather API](https://openweathermap.org/api). When you send an HTTP GET request to this API, it will respond back to you with whatever weather data you requested, allowing you to display that information in your app for your users.

There are LOADS of APIs on the web, ranging from those containing extremely helpful information like the weather, financial data, and government data to those containing really fun info like a database of Jeopardy questions or breweries or Star Wars info.

Okay, you've sold us... APIs sound great. How do we use them?

## Axios
Axios is a very popular JavaScript library you can use to perform HTTP requests. 

Because axios is a library, you have to first add it to your project. There are two ways to do this:
- You can install it directly through the command line using `npm install axios` 
- or you can link to the axios library in the head section of your HTML page with `<script src="https://unpkg.com/axios/dist/axios.min.js"></script>`.

Once you've added axios to your project, you'll have access to the axios object and axios specific methods. In particular, you'll have quick methods for all four of our CRUD actions / HTTP request methods:

- you can CREATE with `axios.post()`
- you can READ with `axios.get()`
- you can UPDATE with `axios.put()`
- you can DELETE with `axios.delete()`





