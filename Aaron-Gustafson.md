# Who is Aaron Gustafson?

Is a principal strategist and he will talk about progressive enhancement. His presentation was called "adaption to reality". He really likes to work for the web, but does more with web accesibility.

# The presentation

He will talk abaout adapting to reality.

## Is webdev hard?

He has found this to be very true. When he started a long time ago, the web was really small. The resolution at the time of a screen was very small (around 640 pixel). Back then things were very simple.

There are 5 things he named:

1. Screen sizes
2. Interaction
3. Network connection
4. Different needs
5. Browser support

### 1. Designing for screen sizes is hard

Over time screen size increased. They didn't have media query and all the other fancy CSS stuff. Screens kept getting bigger. At the 1024 x 768 pixels, alot of people were comfortable, however laptop sizes were all over the place. They were happy to ignore the crappy little phone screens, because most people couldn't even afford a phone with internet on it back then.

They ignored small screens until the rise of smartphones. Tablet sizes are still all over the place. To handle all the different screen sizes, they had media queries to fix this. Designers would work with standards sizes, although, there weren't really standard sizes, since the sizes were mostly all over the place. Then that's when responsiveness came in place.

"Chasing screen sizes is clearly fool's errand" is a quote he had in his presentation, just to show how much they had to keep up with all the different screen sizes.

### 2. Designing for the way the user can interact

Users will need to interact in many different ways, such as eye-tracking, braille, print, keyboard, mouse, remote, audio, gamepad, pen etc.

### 3. Varied network conditions

People will be at different places with all sorts of network connections to interact with a website or application. Latency can affect how our content is experienced. It becomes really important to consider this as we are building our application.

### 4. Our users have all different needs

We all have different needs as individual user's and there are all sorts of ways that affect the way of how we interact with the web.

### 5. Browser support

Then there's also browser support. Sometimes things can't be used. Time can have different variables that impact the way we can interact with the product.

## How do we cope with all of this?

First of all we need to acknowledge that every situation and individual is different. We don't expect that everyone will have the same experience as we do.

We usually design for people who are like us, but there are plenty of people out there who are not like us. The designer is one of a smaller group. When we design for designers, we're excluding most of the population, because most people are just simply like us. If we exclude people, we're really holding back the web.

# Smartphone penetration

In this part of the presentation he basically talked about how many people in different countries have a smartphone and made a connection with this on an economical level. He wanted to show us that half of the population for example from the US, falls into this bucket.He wanted to show us that it's easy to fall into the pit of thinking "I will design only for smartphones" but you really shouldn't, because like I said earlier, the data also shows that that would mean that you wouldn't be including a very high percentage of people.

## Smartphones are different

It's important to note that 1 in 6 UD adult is a smartphone-only internet user. It's also very important to keep in mind that phones are all very different. They all have different specs. Some people don't even make enough money who can afford a newer phone.

He found out the following: smarthphone users who fell into that lowest income bracket, experience internet errors around 52% of the time, which is just insane, because that means that we probably exclude these kind of users. Most apps were not working well on these phones.

# Creating opportunities

When we do include people, we make space for oppurtunities. Designing with constraints, is basically designing well. Originally voice controls were designed for specific people, but nowadays we can all use it to our advantage, same goes for high contrast screen modes for example.

We can build more robust experiences when we also focus around people with disabilities and design for these people.

# Approach your job with your eyes open and have empathy for your users

We need to be comfortable to make mistakes and learn from them. We need to be able to step in our user's shoes. All of this comes down to :

- Progressive enhancement

# Progressive enhancement

Approach your job with your eyes open and have empathy for your users. We need to be comfortable to make mistakes and learn from them. We need to be able to step in our user's shoes. All of this comes down to : progressive enhancement.

## What is progressive enhancement?

It's about considering a person's capability, browser's capability, a machine's capability and improving the user's experience and creating a resilience experience for your users that's not going to break.

Example: He's a music guy and mono is a great way to experience music. When you have stereo speakers, things get enhanced. But he doesn't know any album that was made for a really high end speaker and you're unable to play it on a mono speaker, because sometimes that's all people have or really what people need.

### What matters?

Progressive enhancement asks "what matters" and build that. Think about all the purposes and considering everything else as extra.

### His process of progressive enhancement - very interesting part

1. Focus on the matter: what is the purpose of this page and what matters? (img is not necessarily, author neither)
2. We want to focus on how the interface reads: write it out then read it back (the content doesn't always resonates with the user, for example: they had an option "embarassing" but they rather wrote themselves "it's embarassing". We need to speak to our users, how we talk to others)
3. Look for semantics that support 1 and 2 meaningfully (they have more meaning than a generic div element)
4. Think about how design can improve comprehension (we want to visually show what is most important and group similar elements. This is also important for people who do not interact with the design visually.)
5. Consider how your design choices impact the reading experience (If you can't read text good or see the images good it can affect the user experience negatively)
6. Think about the many differnt ways folks might interact with your application (eye-tracking/hovering and mouse, focus and target for remote or voice control or gamepad, gestures with mouse or touch or pen, text with print or braille, audio interactions with screen readers)
7. Map the potential experiences with for example: flow charts (with a start point, then a diamond shape question and write out the experience from that)
8. Iterate on this approach (valuable how the map can be evolved by different components)

## Graceful Degration

In the early days it was really hard to keep up, just like today with frameworks. People were really struggling with the basics. This is when Graceful Degration comes in play and sits in relation to progressive enhancement. It gives developers the chance to improve. It's all about blocking technical restrictions.

An example of graceful degration is that in the early days modern browsers were blocked, because if you need to update your browser, you're not delivering an error. So the solution was just to "degrade" itentionally.

Graceful Degration looks similar to progressive enhancement, because all progressive enhancement CAN degrade gracefully, but not the other way around.

# Reflection

So the most import take-away from this presentation is his process of progressive enhancement. I found it pretty interesting. He brought up a lot of, mostly shocking data that I was pretty suprised about and didn't really think about before he mentioned all of the things he did mention. It was an interesting point of view how we usually design for people who are like me: designers, but most people are indeed not designers. It was also nice to know that a lot of what he mentioned, I do usually keep in the back of mind, but I don't really think about it. His presentation has shed some light on how I can improve as a designer, but also what I'm doing good. It was also soothing to know that web development is hard, because sometimes I find it a bit over-whelming. Good to know that a professional thinks so too.
