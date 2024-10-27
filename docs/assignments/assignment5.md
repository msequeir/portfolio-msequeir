---
title: Assignment 5
layout: doc
---
# A5


## Heuristics for Evaluation: 

### Observations
**Usability criteria**: capture the broad overall goals that your visual and interactive designs might be trying to satisfy.  


- *Efficiency*: once you know how to use an interface, can you use it to quickly and efficiently accomplish your goals?  

    - Once you know how to use the interface you can use it pretty quickly and efficiently to accomplish your goals. For example, once you understand that you can navigate to any of the pages using the icons that are present at the top of every page, it becomes pretty easy to maneuver through the website and get to the page you want.   

- *Error tolerance*: how easily can a user recover from making mistakes?  

    - The interface allows for easy recovery against making a mistake, for example say somebody clicked the wrong icon on the top so they are taken to the wrong page, they can easily navigate back to the page they were on using said icon. One thing I might consider is giving users a warning before they upload a post or something along this idea, or if somebody is editing a post and accidentally leaves the page, they may want a warning or they might lose their data. 

**Physical heuristics**: describe characteristics about the user interface that affect how users might operate it  

- *Fitt’s Law*: how quickly and easily can users reach for (or point to with their cursor) interface elements?  

    - I think in respect to Fitt’s law my icons especially in the top bar are pretty close to each other, which is pretty good. Users can slightly move their cursor and access different pages especially as seen in the top right bar of the page. Additionally, I will probably have a logo or a search bar in the top center to allow this to conenct the icons on either side of it in respect to Fitt's Law.    

- *Mapping*: does the layout of the interface elements match their function?  

    - In terms of the layout, I have the home button in the top left of every screen which I think makes sense. Maybe some of the other icons could be reorganized to make sense, but I might get a better feel of this as I start designing.   


**Linguistic level**: describe cultural conventions and norms about the interface
- *Speak a user’s language*: does the interface use simple, helpful informative messages? are there instances where messages might only be understandable by developers?  

    - In my wireframing, I did not consider how my app would handle error messages. For example making a post without an itinerary error should lead to an error message so that’s something I can consider adding to my interface. However, as I am coding I am discovering that error messages I included in my backend nicely propagate to the front end so I'm glad I did it this way. 

- *Consistency*: does the interface reuse the same names, symbols, and icons for the same concepts or actions? how consistent is the interface with others across the same application domain or platform?  

    - The interface reuses the same icons at the top of every page. This takes the user to the home page, itinerary, favorites and so on. This is consistent with every page and then on the page where you are editing an itinerary the itinerary icon is replaced by a single person or two people to represent collaborating on an itinerary.   


Reflections after writing the code:

As I designed my app, I wanted to keep the user in mind. I orignially wanted emojis to be my links but decided this might not be super intuitive as to what they mean so I kept the words. Additionally, I found that keeping my emojis different enough when I did include them was key. I kept hearts as favoriting a post, a thumbs up as upvoting and the pencil and trash icons as editing and deleting respectively. It was a little tough figuring out how to make sure favoriting and liking and rating could all be different but I think the way my app does it with hearts, thumbs and stars makes intuitive sense. Additionally, I keep my links at the top close to eahc other and allow the user to click either on the logo or the icon to get to the home screen. Overall, I really tried to keep these heursitics in mind when designing my website, all so that the user has a good experience with my page. 

## Design Study

<img src="/../assets/images/image_design.png" width="400" height="400">
<img src="/../assets/images/font_design.png" width="400" height="400">

### Image
For my design study the first thing I looked at were the images. I first looked at the rainbow image and really liked the light blue teal color that I saw. Being that it stood out to me I wanted to pursue a wide variety of images that accentuated these different shades of blue. I loooked through many different sources and since this is a travel app I decided that looking at travel images were a great way to inspire me. As you look through my app, the inspiration from these images is evident, with my app featuring a light teal color as the background. 

## Font
Looking at fonts was a fun process and I looked at a whole lot of fonts. I decided that I really liked the serif fonts after looking at a few and gathered some of those fonts for inspiration and included them on my slide. Additionally, I wanted my logo to in cursive after looking at some these different fonts and it felt applicable for the travel vibe I was going for. Finally, the two fonts Lobster and Poppins stuck out to me so I included them in my design slides and they made their way into my app!



## Link to Frontend Code Repository
https://github.com/msequeir/frontend-starter

## Link to Vercel Deployment
https://frontend-starter-gb69ifsvg-matts-projects-15c29c0a.vercel.app/