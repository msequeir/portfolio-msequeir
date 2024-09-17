---
title: Assignment 2
layout: doc
---
# A2

## App Name: **Wanderly**


### Intended Audience:
The intended audience is travelers and adventure seekers who want personalized travel experiences at the drop of a hat. It will hopefully expedite travel planning and remove some of the headaches involved in planning a trip that makes it daunting. 

### Value Add:
The main value that it will bring to users beyond existing apps is that they get a curated travel itinerary that considers personal preferences when deciding location, accommodation, restaurant suggestions, and more to ensure that every aspect of the trip, lines up with a user's preference. 

## Scrapbook of Comparables

#### **Kayak**
<img src="/../assets/images/Kayak.png" width="400" height="400">
  
This is a screenshot from kayak. The data collection phase could be very useful to me especially if I am doing active data collection to try and figure out how best to plan a trip for a user. This screenshot shows the different types of questions they ask. 

  
#### **Pack Up + Go**
<img src="/../assets/images/PackUp+Go.png" width="400" height="400">
  
This snippet comes from the website “Pack Up + Go” and shows the different functionality that the website provides. It’s useful for knowing what type of features I could include and maybe some of the guarantees that would be nice. Additionally, it includes at the top that Indeginous Peoples Day is coming up and would be a great getaway. 
  
  
#### **Triptile**
<img src="/../assets/images/triptile1.png" width="400" height="400">
<img src="/../assets/images/triptile2.png" width="400" height="400">
  
These two screenshots are from the website triptile.com and shows possible pre-planned trips for different locations. It’s useful because it has a nice UI format and provides examples of displays for different regions of the world and how in different countries there are different cities with pre-planned trips.  Additionally, you can see prices and dates and if it allows for private or public tour opportunities. 
  

#### **Roadtrippers**
<img src="/../assets/images/Roadtrippers1.png" width="400" height="400">
<img src="/../assets/images/Roadtrippers2.png" width="400" height="400">
  
This is from a website called Roadtrippers. It allows you to plan a trip by inputting where you are starting and where you are going. I really like the UI background and the starting and ending destinations is reminiscent of flight travel. They also have this really cool map idea where it highlights cool locations in the US that travelers might want to visit such as Mount Rushmore or national parks. 


## Features

1. **WanderMatch**
    - Description: Matches users with destinations and experiences based on their browsing history and interests. It recommends personalized travel options tailored to users’ past preferences and activities.
2. **FlightMatcher**
    - Description: Searches for flights that fit within the user’s budget and preferences, including preferred airlines, flight times, and layover conditions.
3. **DreamDestination Finder**
    - Description: Allows users to input ideal travel scenarios (e.g., adventure, relaxation) and suggests destinations that match these criteria.
4. **LocalLuxe**
    - Description: Suggests luxury travel experiences such as exclusive tours and high-end dining, tailored to users who seek premium options.
5. **TravelBuddy Chat**
    - Description: Provides an AI-powered chat feature for instant travel advice and recommendations based on the user’s itinerary and interests.
6. **TripPost**
    - Description: Users can create detailed posts about their trips, sharing experiences, itineraries, and highlights with the community.
7. **Comment**
    - Description: Users can leave comments on posts, providing feedback or engaging in discussions about shared travel experiences.
8. **Login**
    - Description: Users can securely log in to their accounts to access personalized features and travel planning tools.
9. **TripHistory**
    - Description: Users can view a comprehensive history of their past trips, including destinations, activities, and saved notes.
10. **TasteTracker**
    - Description: Users receive dining recommendations and food experiences tailored to their culinary preferences and past reviews.
11. **StaySavvy**
    - Description: Users receive curated accommodation options based on their preferences, including amenities, location, and price range.
12. **ConnectFriends**
    - Description: Users can add and connect with friends on the app to share travel plans, recommendations, and updates.
13. **TravelPoints**
    - Description: Users earn points for completing travel-related activities, which can be redeemed for rewards or special features.
14. **HighlightStories**
    - Description: Users can upload and share highlights from their trips; popular and viral stories may be featured to inspire others.
15. **TripSuggestion**
    - Description: The app randomly suggests potential travel destinations or trips based on user interests and preferences.
16. **Social Sync**
    - Description: Integrates with users' social media accounts to suggest travel destinations and activities based on their shared posts and interests.
17. **Adaptive Recommendations**
    - Description: Continuously refines recommendations based on user interactions and feedback, adapting the suggestions to better fit evolving preferences and trip details.
18. **Upvoting**
    - Description: Users can upvote posts or comments to make them more visible. 
19. **Favoriting**
    - Description: Users can favorite trip itineraries or any other items to save and look at later. 
20. **BudgetBuddy**
    - Description: Manages the travel budget by suggesting cost-effective alternatives for activities, dining, and lodging, tailored to user spending habits.
21. **EventRadar**
    - Description: Alerts users to local events and activities happening during their trip, including festivals, concerts, and cultural happenings.
22. **Interactive Map**
    - Description: Features a dynamic map highlighting personalized recommendations for attractions, dining, and lodging, with filters based on user interests.
23. **Personalized Packing List**
    - Description: Generates a packing list tailored to the user’s destination, activities, and weather conditions, with essential and optional item suggestions.
  

Note: Brainstorming for some of the features was aided by GPT. 


## VSD Design

### Stakeholders

#### Prompt 1:
**Direct Stakeholders:** Those who directly interact with your app are known as direct
stakeholders. These direct stakeholders may have unique perspectives, skills, and
concerns. In what key roles will individuals interact directly with your app? (E.g., for a
medical application, direct stakeholders would include the intake receptionist,
physician, insurance agent.)

- **Observation**: The direct stakeholders are travelers who seek to plan trips using personalized itineraries and content creators who would like to share their travels using the Post and Story features. These groups could have different expectations from the app: travelers may prioritize convenience and customizability while content creators may value visibility. 

- **Design Response**: 
Introducing separate modes for users with one being travelers and one being for content creators. A creator mode could prioritize activities that would garner clicks and curate trips based off of content creation. A traveler mode would priortize WanderMatch and other features such as TasteTracker. 
  

#### Prompt 2:

**Indirect Stakeholders:** Some people may be affected by a system without directly using
it. These people are known as indirect stakeholders. In what key roles will individuals be
affected by your app but will not directly interact with it? (E.g., for a law enforcement
database, indirect stakeholders would include citizens, bystanders, lawyers.) Generate a
list of 3-5 indirect stakeholders. For each indirect stakeholder role, note at least one
concern specific to that role.


**Local Businesses** (e.g., hotels, restaurants, tour operators)  
- **Concern**: They rely on user-generated recommendations through features like StaySavvy and TasteTracker. However, smaller or less tech-savvy businesses may struggle to gain visibility compared to larger, more established businesses.  
- **Design Response**: Offer a feature where smaller businesses can be promoted based on location proximity and user preferences, balancing exposure for both popular and lesser-known establishments. 

**Tourism Boards**  
- **Concern**: Tourism boards may be indirectly impacted if the app promotes certain locations over others, potentially leading to overcrowding in popular spots while under-promoting lesser-known destinations.  
- **Design Response** : Implement a feature that promotes lesser-known destinations and encourages sustainable tourism. This would include partnering with tourism boards to highlight under-visited areas and spread tourism benefits across regions.  

**Local Communities**  
- **Concern**: Local residents may experience increased tourist traffic, which can affect their daily lives through overcrowding or rising costs of living in popular areas promoted by the app.  
- **Design Response**: Incorporate a Sustainable Travel Alert that informs users about the capacity of certain destinations and offers alternative options during peak times, thereby mitigating the negative impact on local communities.
  
  

### Time  
#### Prompt 3:
**Adaptation:** People are inherently adaptive, changing themselves or their behaviors in
order to fit current conditions. Technologies can facilitate adaptation (e.g., a device that
displays home energy use may encourage a homeowner to turn out the lights) or hinder
adaptation (e.g., a person may be prevented from adopting a useful new technology if it
is incompatible with other currently used technology). What is a lifestyle change that you
app might support? Does it inhibit any positive lifestyle changes, or encourage negative
ones?

- **Observation**: The app encourages users to explore new places and experiences by offering personalized recommendations through features like DreamDestination Finder and WanderMatch. This can promote a more adventurous lifestyle, allowing users to broaden their horizons and discover hidden gems they might not have considered.  
- **Concern**: The app might inadvertently encourage over-reliance on digital tools for travel planning, potentially inhibiting spontaneity or discouraging personal exploration. Users may miss out on the joy of serendipitous discovery by overly relying on curated content and recommendations.  
- **Design Response**: Introduce a feature called Off-the-Grid Mode, which encourages users to explore destinations with minimal guidance, allowing more room for spontaneity. This mode would provide only essential information (like safety tips) and encourage users to explore without detailed itineraries or recommendations, fostering a sense of adventure and discovery.

### Pervasiveness  
#### Prompt 4:  
**Crossing National Boundaries:** Nations have different rules, customs, and
infrastructure that affect use of a technology. What challenges might your app encounter
if it were used in other countries?  
- **Observation** : The app’s features like FlightMatcher and StaySavvy might face challenges in different countries due to varying regulations, language barriers, and differences in how travel services are booked and accessed. Certain countries may have stricter data privacy laws that affect the app’s ability to collect and store user preferences or provide personalized recommendations.  
- **Concern**: In countries with stricter regulations or less developed infrastructure, the app may struggle to function as smoothly, leading to reduced usability. Additionally, cultural differences could affect how travel suggestions are received or how users engage with the app.  
- **Design Response**: Implement localized versions of the app tailored to the legal and cultural context of different regions. Regional Customization Settings could allow the app to adapt its recommendations, data collection policies, and interface based on the local regulations, language, and customs. Collaborating with local travel agencies could also improve the app’s functionality in diverse locations.

### Values  
##### Prompt 5:  
**Environmental Sustainability:** Many systems can be applied or extended to support a
desirable environmental outcome (e.g., a system designed to support efficient printing
from web browsers may lead to less use of paper and ink). At the same time, systems may
have unintended negative effects on the environment (e.g., pollution and waste created
in the production of electronics). How might your app and its design support a position
environmental outcome? How might it or its use lead to negative effects (intended or
unintended)?


- **Observation**: Including a features that encourages eco-friendly travel by recommending green accommodations and low-impact activities would be a great boost to this app. This can reduce the user’s carbon footprint while traveling and promote sustainable tourism practices. However, unintended negative effects could arise from excessive travel planning or recommendations that increase frequent short-term trips, contributing to higher emissions from transportation.    
- **Concern**: While the app promotes sustainable choices, the convenience it provides may unintentionally encourage users to travel more frequently, increasing their overall environmental impact through air travel and other emissions-heavy transportation.  
- **Design Response**: Add a Carbon Footprint Tracker that shows users the environmental impact of their travel plans. Encourage eco-friendly alternatives by rewarding users with points or badges for choosing sustainable options, such as train travel over flights or carbon-offsetting activities. This would incentivize responsible travel while mitigating the risk of excessive travel contributing to environmental harm.

Note: Some responses were aided by GPT. 


## Sketches
<img src="/../assets/images/6.1040_Sketch1.jpeg" width="700" height="400">
<img src="/../assets/images/6.1040_Sketch2.jpeg" width="700" height="400">
<img src="/../assets/images/6.1040_Sketch3.jpeg" width="700" height="400">


