---
title: Assignment 3
layout: doc
---
# A3

## Wanderly Product Pitch

**Wanderly** is your ultimate passport to adventure, designed for explorers, dreamers, and globetrotters eager to share their journeys and plan their next big trip. Whether you’re backpacking through Europe, road-tripping across the U.S., or discovering hidden gems in your own backyard, Wanderly transforms your travel stories into immersive experiences.

***Share*** your adventures with rich, interactive posts that showcase stunning photos, day-by-day itineraries, and unforgettable moments. ***Collaborate*** with friends to plan group trips, combining ideas and creating the perfect getaway together with real-time collaborative itinerary planning. ***Discover*** inspiration by browsing trips from travelers worldwide, using powerful search and filter tools to find exactly what you’re looking for—whether it’s epic hikes, culinary hotspots, or must-see landmarks.

Want to know which trips stand out? The upvoting system lets you elevate the most helpful and inspiring posts, and personal ratings give travelers a way to reflect on their own experiences. Plus, you can save your ***favorite*** trips for easy access when you’re ready to book your next adventure.

**Wanderly isn’t just an app—it’s your adventure hub, where every journey begins and new destinations await. Get ready to explore the world like never before!**
  
Note: Completed with the help of ChatGPT



## Concepts

### Concept 1: Posting 
  - **concept** Posting[ItineraryType, PhotoType]
  - **purpose**: Enable users to share their travel experiences by creating detailed posts that document their trips.
  - **principle**: Users can create a post about their trip, which includes an itinerary object, photos, and options for upvoting.
  - **state**:
    - posts: set Post — Represents all posts made by users in the application.
    - upvotes: Post -> set User — Maps each post to the set of users who have upvoted it.
    - itineraries: Post -> ItineraryType — Links each post to its corresponding itinerary.  
  - **actions**:
    - createPost(u: User, itinerary: ItineraryType, photos: set PhotoType) -> Post
    - editPost(u: User, p: Post, itinerary: ItineraryType, photos: set PhotoType)
    - deletePost(u: User, p: Post)

### Concept 2: Itinerary Creation 
  - **concept** ItineraryCreation[ActivityType, LodgingType]
  - **purpose**: Allow users to create and save detailed itineraries for their trips.
  - **principle**: Users input day-by-day details of their trip plans which can be saved and later shared or modified.
  - **state**:
    - itineraries: set Itinerary — Represents all itineraries created by users.
    - days: Itinerary -> set Day — Maps each itinerary to a set of days.
    - activities: Day -> set ActivityType — Maps each day to a set of activities.
    - lodging: Itinerary -> LodgingType — Links each itinerary to its lodging details.  
  - **actions**:
    - createItinerary(u: User, out i: Itinerary)
    - addActivity(i: Itinerary, d: Day, a: ActivityType)
    - addLodging(i: Itinerary, l: LodgingType)
    - modifyItinerary(i: Itinerary, d: Day, a: ActivityType)


### Concept 3: Upvoting System 
  - **concept** Upvoting[PostType]
  - **purpose**: Encourage users to highlight the most helpful or interesting trips by upvoting posts.
  - **principle**: Users can upvote a post they like, which boosts its ranking in the discovery feed.
  - **state**
    - upvotes: PostType -> Int — Tracks the number of upvotes for each post.
    - voters: PostType -> set User — Maps each post to the set of users who have voted on it.  
  - **actions**:
    - upvotePost(p: PostType, u: User)
    - removeUpvote(p: PostType, u: User)


### Concept 4: Authenticating 
  - **concept** Authenticating
  - **purpose**: Authenticate users so that app users correspond to real people.
  - **principle**: After a user registers with a username and password pair, they can authenticate as that user by providing matching credentials.
  - **state**:
    - registered: set User — Represents users who have registered.
    - username, password: User -> one String — Maps each user to their username and password.  
  - **actions**:
    - register(username: String, password: String, out u: User)
    - authenticate(username: String, password: String, out u: User)


### Concept 5: Favoriting 
  - **concept** Favoriting[PostType]
  - **purpose**: Allow users to save posts they find interesting, creating a personalized collection of content.
  - **principle**: Users can favorite any post, which will be saved to their favorites list.
  - **state**:
    - favorited: set (User, PostType) — Tracks which posts each user has favorited.  
  - **actions**:
    - favoritePost(u: User, p: PostType)
    - unfavoritePost(u: User, p: PostType)
    - viewFavoritedPosts(u: User)  


### Concept 6: Search and Filter
  - **concept** SearchAndFilter[PostType]
  - **purpose**: Allow users to search for posts based on specific criteria, enhancing content discoverability.
  - **principle**: Users can enter search queries to find posts and apply filters to narrow down results.
  - **state**:
    - posts: set PostType — Represents all posts in the application.
    - filteredPosts: set PostType — Represents posts that match the search criteria.  
  - **actions**:
    - searchPosts(query: String) -> set PostType
    - filterPosts(location: String, activity: String) -> set PostType
    - clearFilters() -> set PostType

### Concept 7: Trip Rating
  - **concept** TripRating[PostType]  
  - **purpose**: Allow users to rate their own trips on a 5-star scale, providing a self-evaluation feature.  
  - **principle**: Users can assign a rating between 1 and 5 stars to their own post (representing a trip), and the average rating is calculated based on the user's own rating.  
  - **state**:  
    - ratings: PostType -> set (User, Int) — Maps each post to a user's own rating (an integer from 1 to 5).  
    - averageRating: PostType -> Real — Represents the average rating for each post (since users can only rate their own posts, this value reflects their personal rating).    
  - **actions**:  
    - rateOwnPost(u: User, p: PostType, rating: Int) — Allows a user to rate a post they created with a value between 1 and 5.  
    - updateAverageRating(p: PostType) — Recalculates the average rating for a post (in this case, only the user's own rating is included).  
    - removeRating(u: User, p: PostType) — Removes a user's rating for their own post.

### Concept 8: Collaborative Trip Planning
  - **concept** CollaborativeTripPlanning[PostType]  
  - **purpose**: Enable users to co-create and manage itineraries for group trips, making the planning process collaborative and interactive.
  - **principle**: Users can invite others to collaborate on a shared itinerary, allowing all invited users to contribute, edit, and refine the trip details. Changes made by any collaborator are visible to the entire group in real-time.  
    
  - **state**:  
      collaborativeItineraries: set Itinerary — Represents all itineraries that are being collaboratively created by multiple users.
      collaborators: Itinerary -> set User — Maps each collaborative itinerary to the set of users who can edit and contribute to it.
      edits: Itinerary -> set Edit — Tracks modifications made to the collaborative itinerary.  
        
  - **actions**:   
      - createCollaborativeItinerary(u: User, out i: Itinerary) — Allows a user to start a new collaborative itinerary and invite others to participate.
      - inviteCollaborator(i: Itinerary, u: User) — Adds a specified user as a collaborator on the itinerary.
      - editCollaborativeItinerary(i: Itinerary, d: Day, a: Activity, u: User) — Allows a collaborator to add or modify activities, lodging, or other itinerary details.
      - viewEdits(i: Itinerary) — Displays a log of all changes made to the itinerary, including the user responsible for each change.


Note: Completed with the help of ChatGPT

### Dependency Diagram
<img src="/../assets/images/Dependency_Diagram.jpeg" width="550" height="550">


## Wireframes
[Figma Designs] (https://www.figma.com/proto/jKjXKkqoIhKNDqcmwgmE68/Wanderly?node-id=10-105&t=qJkXb2dfdpm9FdVm-1)

## Design Tradeoffs

1. Search and Filter vs. Commenting System
- Options: Implement either a powerful search and filter system to find posts by location/activity or allow users to comment directly on posts to foster discussion.
- Rationale: I chose Search and Filter because it enhances discoverability and user personalization. Comments could clutter the travel feed and distract from the core experience of finding valuable travel insights. Search capabilities make it easier for users to efficiently navigate the app and find content relevant to their specific needs.
2. Upvote Button vs. Favorite Button
- Options: Implement either an upvote button, a favorite button, or both. They have overlapping visual functions, but serve different purposes.
- Rationale: Initially, I considered only including one button, as the two seemed visually redundant. However, I ultimately chose to include both because their functionalities are distinct enough. The Upvote button highlights helpful and popular content for the community, while the Favorite button allows users to save posts for personal use. Including both ensures that users can engage with content publicly while also curating their own collections privately.

3. Self-Rating System vs. Public Rating System
- Options: Let users rate their own trips (self-evaluation) or allow others to rate trips publicly.
- Rationale: I chose Self-Rating to ensure ratings are personal and authentic to the user's experience. Public ratings could bias results and create unnecessary competition. Self-rating emphasizes reflection rather than popularity, keeping the app more focused on personal growth and meaningful travel experiences rather than external validation.

Note: Responses were polished by GPT.

