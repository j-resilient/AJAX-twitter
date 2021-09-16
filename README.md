# AJAX Twitter
A simplified version of twitter meant to practice using JavaScript and jQuery for AJAX.  
[Project Specs](https://open.appacademy.io/learn/full-stack-online/javascript/ajax-twitter)  
  
# To Do
## Phase 1: Follow Toggle
Turn the follow button into a toggle that follows/unfollows a user.  
- Change app/views/follows/_form.html.erb so that we can use JS instead of just HTML  
- Create the FollowToggle class  
- Use said FollowToggle class in twitter.js so that webpack can transpile it
- Write FollowToggle#render
- Write FollowToggle#handleClick
- Refactor AJAX calls into api_util
- Freeze the follow/unfollow button so that people can't click it while our AJAX request is pending  
## Phase 2: UsersSearch
Create a real-time user search: every keypress typed by the user should show the matching users for the current input.  
- Review UsersController and search.html.erb
- Change search.html.erb so that we can use JS instead
- Create the UsersSearch class
- Write APIUtil#searchUsers(queryVal)
- Write UsersSearch#handleInput
- Modify UsersController to handle HTML and JSON requests
- Read about JBuilder
- Create a search.json view using jbuilder
- Write UsersSearch#renderResults
- Add follow toggle buttons to search results
- Style the default page font
- Add headers to app and search results page
- Style buttons
## Phase 3: TweetCompose
Update the tweet compose behavior.
- Update TweetsController to handle JSON requests
- Create a show view for tweets
- Create a jBuilder partial to get the tweet's info and info on the tweet's mentions
- Create TweetCompose class
- Write APIUtil#createTweet(data)
- Write TweetCompose#clearInput
- Write TweetCompose#handleSuccess
- Add counter to display how many remaining chars are available for tweet
- Style form
## Phase 4: TweetCompose: Mentioned Users
Rewrite to allow users to tag multiple users in a tweet.
- Write code to add mentions
- write code to remove mentions
- Update TweetCompose#clearInput to clear out selects
- Style mentions
## Phase 5: Infinite Tweets
Paginate tweets so they're not all sent at once.
- Update User model
- Modify feeds show view
- Update Feeds controller
- Write an InfiniteTweets class
## Phase 6: jQuery Triggering
Create a custom event so that we don't have to copy the code from InfiniteTweets to TweetCompose (because they're both trying to insert tweets into the feed).
- Create custom event so that TweetCompose triggers an insert-tweet event instead of inserting HTML itself
- Add listener for insert-tweet in InifiniteTweets
## Phase 7: Jbuilder Practice
Practice Jbuilder.
- Update Follows show
- Update Users show
- Write a Tweets index
## Phase 8: CSS
- Pick a font
- Style page layout
- Style the feed
- Style the user search page
- Style login/signup page