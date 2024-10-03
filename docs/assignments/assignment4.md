---
title: Assignment 4
layout: doc
---
# A4


## Abstract Data Model of Wanderly Concepts
Below is the abstract data model for each concept, listing the state variables and their relations. These are defined in a generic manner, with type parameters that allow flexibility in the specific implementation.

### Concept 1: Posting[ItineraryType, PhotoType]
- State Variables:
    - posts: set Post — Represents all posts made by users.
    - itineraries: Post -> ItineraryType — Links each post to its corresponding itinerary.
    - photos: Post -> set PhotoType — Links each post to a set of photos.
### Concept 2: ItineraryCreation
- State Variables:
    - itineraries: set Itinerary — Represents all itineraries created by users.
### Concept 3: Upvoting[PostType]
- State Variables:
    - upvotes: PostType -> Int — Tracks the number of upvotes for each post.
    - voters: PostType -> set User — Maps each post to the set of users who have voted on it.
### Concept 4: Authenticating
- State Variables:
    - registered: set User — Represents users who have registered.
    - username, password: User -> one String — Maps each user to their username and password.
### Concept 5: Favoriting[PostType]
- State Variables:
    - favorited: set (User, PostType) — Tracks which posts each user has favorited.
### Concept 6: SearchAndFilter[PostType]
- State Variables:
    - posts: set PostType — Represents all posts in the application.
    - filteredPosts: set PostType — Represents posts that match the search criteria.
### Concept 7: TripRating[PostType]
- State Variables:
- ratings: PostType -> set (User, Int) — Maps each post to a user's own rating (1 to 5 stars).
- averageRating: PostType -> Real — Represents the average rating for each post.
### Concept 8: CollaborativeTripPlanning[PostType]
- State Variables:
    - collaborativeItineraries: set Itinerary — Represents all itineraries being co-created.
    - collaborators: Itinerary -> set User — Maps each itinerary to its set of collaborators.
    - edits: Itinerary -> set Edit — Tracks modifications made to the collaborative itinerary.


## Wanderly App Definition
Here’s how the concepts are instantiated for Wanderly:

- Posting[Itinerary, Photo]
- ItineraryCreation
- Upvoting[Post]
- Authenticating
- Favoriting[Post]
- SearchAndFilter[Post]
- TripRating[Post]
- CollaborativeTripPlanning[Post]


  
## Data Diagram
  <img src="/../assets/images/Data_Diagram.jpeg" width="400" height="400">

## Deliverables

### Functioning Backend Concepts:
- Upvoting
- Favoriting
- Posting
- Filtering Posts by Author / Title or both

## Concept Outlines

    {  
    - name: "Create Itinerary",  
    - endpoint: "/api/itinerary/:id/",  
    - method: "POST",  
    - fields: {id},
  },  

    {
    name: "Update Itinerary",
    endpoint: "/api/itinerary/:id",
    method: "PATCH",
    fields: { ... },
  },

    {  
    - name: "Send Collab Itinerary",  
    - endpoint: "/api/itinerary/colab/:id/",  
    - method: "POST",  
    - fields: {id},
  },  

  {  
    - name: "Create Trip Rating",  
    - endpoint: "/api/post/:id/rating",  
    - method: "POST",  
    - fields: {id},
  },  

  {  
    - name: "Update Trip Rating",  
    - endpoint: "/api/post/:id/rating",  
    - method: "PATCH",  
    - fields: {id},
  },  

  
  
