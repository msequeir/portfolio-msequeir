---
title: Assignment 4
layout: doc
---
# A4


## Wanderly App Definition
Below is the abstract data model for each concept, listing the state variables and their relations. These are defined in a generic manner, with type parameters that allow flexibility in the specific implementation.

### Concept 1: Posting[Itinerary]
- State Variables:
    - posts: Post —> One User
    - title: Post -> One String 
    - rating: Post -> number;
    - itineraries: Post -> ItineraryType — Links each post to its corresponding itinerary.
    - photos: Post -> set urllinks — Links each post to a url of photos.
### Concept 2: Itinerary
- State Variables:
    - author: Itinerary -> One author
    - collaborators: Itinerary -> set of editors
    - content: Itinerary -> One string
### Concept 3: Upvoting
- State Variables:
    - postId: upvote -> One postID
    - userId: upvote -> One userId
### Concept 4: Authenticating
- State Variables:
    - registered: set User — Represents users who have registered.
    - username, password: User -> one String — Maps each user to their username and password.
### Concept 5: Favoriting
- State Variables:
    - favorited: User -> set of Favorited Posts
### Concept 6: Friending
- State Variables:
    - friends: User -> set User

After reviewing the feedback I got from A3, I decided to refine my concepts in my app definition. I had Trip Rating as It's own concept earlier but  now I just decided to keep it as a variable in my Posting concept because of the feedback I recieved and it made more sense. Additionally, I had CollabItinerary as a sepearate concept but after reviewing my feedback I decided to make collaborators as a variable that was part of my itinerary concept. I made these design decision primarily to reflect the feedback I recieved to address some of the concerns the TAs had. 


## Data Representation

### Authenticating

export interface UserDoc extends BaseDoc {
  username: string;
  password: string;
}

### Favoriting

export interface FavoriteDoc extends BaseDoc {
  postId: ObjectId;
  userId: ObjectId;
}

### Itinerary

export interface ItineraryDoc extends BaseDoc {
  author: ObjectId; // Original creator
  collaborators: ObjectId[]; // Other editors
  content: string;
}

### Posting


export interface PostDoc extends BaseDoc {
  author: ObjectId;
  title: string;
  tags: string;
  rating: number;
  itineraryId: ObjectId;
  favoriteUsers: ObjectId[];
  imageUrls: string[];
}

### Upvoting

export interface UpvoteDoc extends BaseDoc {
  postId: ObjectId;
  userId: ObjectId;
}

### Friending
export interface FriendshipDoc extends BaseDoc {
  user1: ObjectId;
  user2: ObjectId;
}

  
## Data Diagram
  <img src="/../assets/images/Data_Diagram.jpeg" width="400" height="400">

  Note: Consulted with a TA :)

### Robustness:

Throughout my routes.ts I make sure that I am validating the input and making sure that only actions that are allowed to happen are happening. For example, in my updateItinerary route,  I await Itinerary.assertAuthorIsAllowedToEdit(itineraryOid, user); // Ensure the user is the owner. I do a similar thing with deleting an itinerary and the same concept applies for my posting as well. Additionally, when posts add an itinerary id to a post, I validate that the itinerary is valid and I check if that user is allowed to post that itinerary. Furthermore, in specific concepts themselves I handle cases that might break my app such as referrring to a delete post or showing posts with itineraries that may or may not be there. 



## Link to Backend Code Repository
https://github.com/msequeir/backend-starter

## Link to Vercel Deployment
https://backend-starter-g8erxzpn8-matts-projects-15c29c0a.vercel.app

<h2> Design Reflections </h2>

As I was working through my backend, I made a lot of choices along the way that affected how my design ended up looking. To begin with, one thing I didn't consider when I was making my original design was how uploading images were going to work. I knew I wanted posting to include images but it turns out that this would be a complicated thing to include. After consulting the Discourse Forum, it suggested keeping track of images as urls that were uploaded to Google drive. I then decided to add a variable to my posting.ts that is a list of strings keeping track of all of the image urls associated with a certain image.


Additionally, another major design decision I made was how favoriting was going to work. This idea of favoriting is that a user is able to favorite a post and then look at their favorite posts whenever they want to. I was considering defining a variable in post that maps to a set of users but I decided to let my favoriting.ts handle these complications. Also, I initially did not consider how deleting the original post would affect favoriting. I ran into some trouble at the beginning when deleted posts would show up in a user's favorites and I decided that this was not the behavior I wanted. I then decided that when displaying a user's favorite posts, it made sure to check that the posts are still active and valid, and if not, that post does not show up in favorites. 


Furthermore, another design decision I made was how to include itineraries as a part of my posting. I knew I wanted to make itineraries a separate concept because I knew I wanted users to be able to create an itinerary without creating a post. Then combining the two, I decided to have a user link an itinerary id to the post and then when the user calls getPost it can display the whole itinerary, as opposed to just id. I did consider just displaying the itinerary id and allowing the user to see the itinerary with the id if they wanted to, but I decided to show the itinerary with a post as well. It felt like this made more sense from the users point of view and removes an unnecessary step. 
