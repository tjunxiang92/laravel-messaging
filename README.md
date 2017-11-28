# Laravel Messaging Tutorial

For this tutorial, we will be building a messaging platform where users can create chatrooms to communicate with each other.

![/assets/endproduct.png](End Product)

## Initial Phase

### Planning  

We are going to break it into three components  
- Messaging  
	- Side Panel  
	- Chat Panel  

### Implementation
This assumes you know the basics of creating a laravel app  

Create a new Laravel App
```bash
laravel new laravel-messaging
cd laravel-messaging
yarn
```

### Probable Hiccups
- Understanding socket.io
- Defining tests
- Parsing JSON format
- Implementing Notifications (Emails)

## Frontend
The frontend is using Vue.js

As we described previously, we want to break it into three portions.

1. Craft the initial data structure
2. Set up templates
3. Tie up functionality
4. Replace with endpoint

#### Endpoints
- GET: Loading Conversations
- GET: Loading Specific Conversation
- POST: Create Conversation
- POST: Send Message in Conversation

## Backend

1. Define the models
2. Create the migrations
3. Create relationships
4. Create Factories
5. Create Seeders

## Tests

1. Rough outline of what tests are required
2. State out all headers of tests
3. Using Given-When-Then create the comments of tests
4. Create the tests

**Guest attempting into conversations should be redirected to login**

- Given that a user is not logged in
- When requesting for conversations
- Then redirected to login page

**User should see conversations they belong in**  

- Given that a user is logged in  
- And there are conversations that the user belongs and do not belong to  
- When requesting for conversations  
- Then a user should see only its own conversations  
- And a user should not see conversations they do not belong in

**User should see conversation messages they belong in**

* Given that a user is logged in
* And belongs to a conversation
* When requesting for the conversation
* Then the user should see it's messages

**User should not see conversation messages they do not belong in**

* Given that a user is logged in  
* And do not belong to a conversation  
* When requesting for the conversation  
* Then the user should not see it's messages  


**User can send a message in conversations they belong in**

- Given that a user is logged in
- And belongs to a conversation
- When posting a message
- Then it should be a success

**User should not be able to send a message to conversations that they do not belong in**

- Given that a user is logged in
- And does not belong to a conversation
- When posting a message
- Then it should show an error

**User is not allowed to create a conversation without a title**

- Given that a user is logged in
- When creating a new conversation
- Then it should show an error without a title

**User is not allowed to create a conversation without members**

- Given that a user is logged in
- When creating a new conversation
- And title is filled
- Then it should show an error without members

**User should be able to create a conversation**

- Given that a user is logged in
- When creating a new conversation
- And title is filled
- And member is filled
- Then conversation should be created successfully

## Integrations

1. Replace API endpoints 