---
title: Assignment 6
layout: doc
---
# A6


## Tasks Lists


| **Task Title**         | **Instruction**                                                                                          | **Rationale**                                                                                                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Register a User        | Create a new user account on the app.                                                                    | Testing user registration helps identify any friction points in the onboarding process, ensuring users can start engaging with the app. Verifies ease of access to all subsequent features requiring login.                   |
| Upvote a Post          | Find a post and upvote it.                                                                               | Tests engagement mechanisms, checking if users can intuitively interact with posts and assess their impact. Gauges the clarity and accessibility of the upvote feature and provides feedback on user motivation to engage.    |
| Favorite a Post        | Favorite a post and then check that it appears in your favorites.                                        | Confirms that users can personalize their experience through favoriting, assessing if users can both favorite content and locate their favorites easily, which aids in evaluating content discoverability and retention.       |
| Create an Itinerary    | Go to the itinerary section and create a new itinerary.                                                  | Tests users’ ability to access and navigate the itinerary feature, a unique aspect of the app. Verifies the clarity of itinerary creation flow and gathers insight on the usability of planning-related functionality.         |
| Create a Post Using an Itinerary | Use the itinerary you just created to make a post that references it.                        | Tests the integration between itinerary and post creation, confirming that users can understand and complete a more complex, multi-step process. Provides insight into the intuitiveness of linking related content.          |


## Participant Analysis Report 1
My first usability session with participant X yielded valuable insights into both effective elements and areas needing improvement in the app’s design. The first task—logging in—was seamless, as expected. Given the prevalence of login screens in most applications, it was unsurprising that X completed this task without hesitation, bridging the gulf of execution effectively.  

Following login, X instinctively moved to the title area to navigate back to the home screen, demonstrating that the clickable title was intuitive. This familiar design pattern helped reinforce that this navigation method aligns with user expectations. He then scrolled through the home page, examining photos and reading comments, remarking that these elements gave him a clear sense of the app’s purpose due to the sample data. This was a positive sign that the app’s content structure communicated its core function effectively.  

The next task was to upvote a post. X identified the thumbs-up button immediately and successfully noted the increasing upvote count. This quick recognition suggested that the visual feedback—a visible change in the upvote count—effectively bridged the gulf of evaluation. When asked to favorite a post, he inferred that the heart icon represented this function, and the change in color upon clicking confirmed the action. This visual confirmation played a significant role in guiding X’s actions and avoided the need for repeated clicking to verify the task's completion.
However, X’s experience shifted during the subsequent task of locating favorited posts. He expressed that the navbar text was difficult to distinguish due to the words being closely spaced. His comment brought attention to a need for clearer separation or padding in the top-right navigation bar to prevent user frustration.  

The final two tasks—creating an itinerary and then a post using the itinerary—revealed a couple usability issues. X expressed uncertainty about what “creating an itinerary” or “creating a post” entailed, indicating that the purpose of these features may not be clear from the terminology alone. After some trial and error, he located the itinerary section and created one, but faced challenges in navigating back to create a post with that itinerary. X noted that the “Create Post” button’s placement in the upper-left corner was unconventional, as he initially looked elsewhere on the screen. His struggle suggests that users might benefit from clearer visual guidance or labeling for creating posts.  

In his final feedback, X mentioned he did not anticipate needing an “itinerary ID” to make a post, which was an unexpected source of confusion. This feedback highlights a gap in intuitiveness and suggests that adding a brief prompt or auto-populated selection for itineraries might bridge the gulf of execution for first-time users. This session clarified that while certain elements are well-aligned with user expectations, other unique aspects of the app may need further clarification or restructuring to create a smoother user journey.


## Participant Analysis Report 2
The second interview, conducted with participant Y, revealed additional insights for refining the app’s usability. As with the first interview, the login process was straightforward, confirming that this basic functionality is well-executed. After logging in, Y navigated to the posts page by clicking on the title, showing that the clickable title function is fairly intuitive for navigation. Y spent a few moments exploring the search and filtering options and mentioned that the upvoting and favoriting elements, along with the overall design, created an inviting, appealing aesthetic. These comments indicated that the interface was visually engaging and that core interactions aligned with her expectations.  

The upvoting and favoriting tasks were also successful; Y immediately identified the thumbs-up and heart icons and completed these actions effortlessly. Similar to participant X, Y remarked that the text in the navigation bar felt cramped, which suggests that additional spacing would improve readability across different user preferences. After completing these initial tasks, she navigated to the Favorites page smoothly, again indicating that the layout and icons communicated their purposes effectively.  

Creating an itinerary presented unexpected challenges for Y. She navigated to the Itinerary page and initially tried to use the search function, assuming that her own name would bring up content. When no results appeared—understandably, since she hadn’t created an itinerary yet—she expressed confusion and spent some time looking for other options. Eventually, she discovered the “Create Itinerary” button, though the delay suggests that this call-to-action could be more prominent to reduce struggles. Initially, I had assumed the button placement would be visually prominent, but Y’s hesitation indicated otherwise, highlighting a potential design revision.  

Once she created an itinerary, she proceeded to create a post. In contrast to participant X, Y located the “Create Post” link quickly. However, she encountered a challenge when prompted for the “itinerary ID.” She retraced her steps, explored the Itinerary section, and eventually located the ID. Her feedback indicated that this process was unintuitive, reinforcing the need to make itinerary selection smoother within the post creation flow. Additionally, Y struggled to add an image, as she added the image link but missed the “Add Image” button. This gap points to a need for clearer instructions or visual cues within the image upload process, especially for users less familiar with the linking approach for images.  

In her final feedback, Y mentioned that the overall functionality was engaging but that the itinerary ID and image addition could be streamlined for greater usability. This feedback supports incorporating a more guided approach for unique tasks within the app, potentially improving the user journey in future iterations.


## Flaws and Opportunities for Improvement
- Navigation Bar Text Spacing
    - Level: Physical
    - Severity: Minor
    - Issue: Both participants noted that the words in the navigation bar were too close together, making the navigation elements harder to read and creating visual clutter. This spacing issue likely stems from minimal padding between the elements.
    - Solution: Increase the padding between navigation elements to improve readability and reduce visual clutter, enhancing the user experience without any substantial redesign.
      
        

- Create Itinerary Button Visibility
    - Level: Conceptual
    - Severity: Moderate
    - Issue: Both users struggled a little with creating an itinerary, with one participant expressing that it didn’t stand out immediately. This indicates that users may not recognize the button quickly in its current location or visual style.
    - Solution: Enhance the button’s visual prominence by placing it at eye level when the page loads, possibly making it a larger or more distinct color. Adding introductory text or a tooltip explaining its function could also help guide users toward it more intuitively.  

      
- Itinerary ID Requirement for Post Creation
    - Level: Linguistic
    - Severity: Major
    - Issue: The term "itinerary ID" was confusing for both users, who were uncertain where to find the ID or what it referred to, resulting in delays and some frustration. This terminology created a linguistic gap that complicated the task unnecessarily.
    - Solution: Consider removing the need for users to locate the itinerary ID themselves and instead implement an itinerary selection dropdown during post creation. Alternatively, a more descriptive term could be used, such as "Select Your Itinerary," to clarify the relationship between itineraries and posts.  
      

- Image Addition Confusion
    - Level: Physical
    - Severity: Moderate
    - Issue: One user had difficulty adding an image because they inputted the URL but missed the separate “Add Image” button, which prevented the image from being uploaded. This extra step was not immediately intuitive and caused some friction.
    - Solution: Simplify the image addition process by combining the URL entry and confirmation into a single action. For instance, hitting “Enter” or clicking outside the URL field could automatically upload the image without requiring a secondary click. Alternatively, provide a more prominent visual cue on the “Add Image” button.  
      

- Intuitive Design for Favoriting and Upvoting Confirmation
    - Level: Conceptual
    - Severity: Minor
    - Issue: While both users completed the favoriting and upvoting tasks, one participant commented that the visual confirmation (e.g., color changes in the thumbs-up and heart icons) helped reassure them they had completed the actions successfully. Without it, they may have tried clicking multiple times to confirm their actions.
    - Solution: Ensure that all interactive elements provide a clear, immediate visual response upon interaction, reinforcing the action’s success. This feature was effective in its current form but could be further emphasized by adding an optional tooltip with confirmation text.