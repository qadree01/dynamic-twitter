# dynamic-twitter

For this project, you need to build a Dynamic Twitter App

Think of this as your "Web Development" Final Project! This will be your hardest challenge so far, so take your time. 

 

Mock JSON
Ok. Instead of using a real API (due to rate limiting issues, credentials, and APIs changing over time...) you will use a mock JSON response to build a Twitter timeline.

What is mock JSON? Simply put, it's a JavaScript object that's the same shape (key and value properties) as a real response would be.

For example, a single Tweet might be represented like so in JSON:

var tweet = {

    userName: "@elonmusk",
    displayName: "Elon Musk",    
    text: "I love Bitcoin",
    timestamp: "March 4, 2021",

}

Many front end developers work with mock JSON before "connecting" their apps to the back end, so it's good practice!

You will find a two user objects in the downloadable file, which are mock JSON -- both of these user objects contain an array of tweets

Next, we'll take advantage of these!

 
"Rendering" JSON to HTML
When we convert data to elements displayed in a browser, it's called rendering.

So we have our mock JSON which represents a user's timeline that we want to render as HTML.

The goal is to create these HTML Elements from mock JSON dynamically, using JavaScript. 

In other words, DO NOT write the tweets, username, or any profile data directly in your HTML -- otherwise it won't be "dynamic" (and won't work for different profiles).

After this section (and the previous problem), We know how to do this. Select DOM elements, create them, set innerText, and add classes as necessary!

Ok, how do you know what to write in directly HTML, vs JavaScript?

Think of it this way: any elements that require JSON data, should be created with JavaScript.

I might sound like a broken record here, but you need to understand this before starting :)

Ok, let's get started now.

 

Specs
Ok, back to building our Dynamic Twitter App

What we want to do is copy the profile page from Twitter

Elon Musk is a good example (assuming his profile is active) 

https://twitter.com/elonmusk

 

Before you freak out, I've removed some of the "unnecessary" elements from the design and attached an image you can work from.

In this attached image, you'll notice the fields that match closely with our mock JSON in index.js (for example, follower count, following, and tweets)

These are the dynamic elements we want to create with JavaScript!

So let's get started in the next section

 

💡 This seems like a lot, but stay calm, you have learned all of this

💡 Your last project will be really helpful. Re-use the code and watch the videos again if need-be

💡 Can you use jQuery for this one? Yes. If you feel more comfortable with it.

💡 As usual, Google is your friend!

 

Steps
1. Right now we just have a JS file, let's create an HTML file (with boilerplate), a CSS file, and then import everything correctly.

2. Now let's create our non-dynamic elements with HTML and CSS. Focus on the containers, or main sections we see on the page. Specifically...

a single content column we can "center" inside body,
A header container
A cover photo container (we can set with a background image)
profile details container
tweets container
💡 These containers are the same HTML and CSS we've been doing for quite a while now. You've already done projects with this!

4. Once your containers are done (or entire page with placeholder elements, depending on your approach) it's time to start rendering dynamic DOM elements

Choose a single user object -- either user1 or user2

Start from the dynamic elements in the header -- where it says...

Elon Musk 13.6k tweets

...and work you way down from there.

For each element, you'll need to: 

Select a container to append to
Get the "value" from your mock JSON. (ex. user1.userName)
create a new element, and set its textContent (alternatively you can use `back ticks` and set a big innerHTML string, as we did in the last project)
append the element to the page, and test that it's working!
💡 This is the hard part, remember, you can reference your code from the project we just did

💡 Create the styles for dynamic elements as you go. Remember you can create a class in style.css and then classList.add when you create the element.

💡 How about the .length property to get the number of tweets?

💡 Remember, use a loop to render one tweet at a time, and then append it to your tweet container

💡 The rest is up to you, just go through the dynamic elements one by one until the design is complete

5. Good job... take a break, get a coffee, and then come back for the final challenge

Now, we want to make things fully dynamic. 

Take a look at the URL of your live server in the browser, now paste the following query string at the end of it, and watch what happens:

?user=user1

That's right: nothing. But we can use this in our JavaScript code to dynamically load profiles.

So, refactor your code to do the following

Read the query string from the URL (Google how to do this)
Based on the query string value, render the User Object of that profile
If the query string is ?user=user1, render the user1 object
If the query string is ?user=user2, render the user2 object
Both profiles should load with no issues, including all profile data, images, and tweets.
 

💡 You will need to both user objects into a larger object called "users" -- this will allow you to retrieve a specific user with its name as a key ( ex users[userName] )

💡 This new large users object is functioning the same way as a database! Our query is the key and our database gives us back user data. Pretty cool right? 

Congratulations, you have complete your first real, dynamic web app! 
