## [COMP 523 J - Venture Capital Online Judging](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/index.md#comp-523-j---venture-capital-online-judging)
- [Project](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/project.md#comp-523-j---venture-capital-online-judging)
- [Team](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/team.md#comp-523-j---venture-capital-online-judging)
- [Journal](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/journal.md#comp-523-j---venture-capital-online-judging)
- [Deliverables](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/deliverables.md#comp-523-j---venture-capital-online-judging)

### Deliverables
* Assignment 1 - [Project Management Board](https://trello.com/b/TRUO0EXx/comp-523-j-wvcc-ojs) (Board is private)
* Assignment 2 - [Web Site](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/index.md#comp-523-j---venture-capital-online-judging)
* Assignment 3 - [User Stories](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/deliverables.md#user-stories)
* Assignment 4 - [Clickable Prototype](https://www.figma.com/proto/UUul35Gly4q1VOsE5kkV7T/VCIC-Clickable-Prototype?node-id=4%3A0&scaling=scale-down)
* Assignment 5 - [Apples Reflection 1](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/deliverables.md#apples-reflection-1)
* Assignment 6 - [Application Architecture](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/deliverables.md#application-architecture)
* Assignment 7 - [Architecture Diagram](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/deliverables.md#application-diagram)
* Assignment 9 - [Midterm Presentation](https://docs.google.com/presentation/d/1yTJ45F_x-e_LXWPIcksyG-ltLQu3-1x2ww8HwgD0F10/edit?usp=sharing)
* [Tech Talk Presentation](https://docs.google.com/presentation/d/1LQhzsYi8q72A2QyU-L2Jw75hTM9pAL6IbQE7e7RIQ4U/edit?usp=sharing)
* [Codepen Demo](https://codepen.io/lukecw98/pen/ZEORqEX)

### User Stories

Need to have:
* As an Administrator, in order to create events, I can create a Google Sheet with the Judge / Participant data.
* As a Judge, in order to know which event I'm in, I can click an event and see my name listed.
* As a Judge, in order to vote in an event, I can click on the event, then my name, then fill out the form.

Nice to have:
* As an Organizer, in order to give the students the results, I can view the real-time results page.
* As a Viewer, in order to view the final results, I can navigate to the results page if given permission by the organizer.
* As a Judge, in order to correct the spelling of my name, I can type in the new spelling of my name.

### Apples Reflection 1

In working with the UNC Kenan-Flager Business School on the Venture Capital Investment Competition (VCIC), we are able to support entrepreneurial education across the country. VCIC is a national series of competitions that has real entrepreneurs pitching ideas to students as though they were investors. This flipped competition provides experience for both the entrepreneurs and students, giving them new and valuable perspectives in the world of business. In seeing how entrepreneurs pitch their ideas, students will be able to better express their own if they are ever looking for investments. Because VCIC is a competition strictly created for educational purposes, it is an effective way to teach students about financing new ventures.<br/>
Our contribution to VCIC creates a simpler interface for judges to submit their votes for winning participants. This increase in usability makes it easier to find and retain judges for every year the event continues. Because the interface is easy to use, judges will see it as less of a chore and more of an opportunity to give their time and energy to contribute in this educational venture. As judges are hard to find and keep, VCIC will have a chance to grow – including more competitions and students to participate in them. By giving more people the opportunity to participate in this competition, we assist them in learning the principles of business and finance.

### Application Architecture

#### Decision 1
Summary: In order to provide an interface for our application, we decided to only use a Front-End to make all API calls and display information.

Problem: In order for our app to provide functionality, it needs routing capabilities.

Constraints: Our page needs to be embedded onto the client's website, which runs on a Wordpress PHP backend.

Options: Create a dedicated backend server or Create only the front-end application.

Client-Server Architecture

Pros: 
- More modular
- Easy to add functionality
- Easy to implement routes
- More resources readily available
- Less complex

Cons:
- Needs to host backend separately
- More moving parts
- Has more dependencies
- Would probably cost money to host

Front-End only Archictecture

Pros:
- Does not need a server
- Less dependencies
- Less moving parts
- Would not cost extra to host

Cons:
- Less modular
- Harder to add functionality
- Harder to implement routes 
- Less resources readily available
- More complex

Rationale: In order to make it easier for the client, we decided to use the Front-End only Architecture.

#### Decision 2
Summary: In order to store and fetch information for each event, we decided to utilize the Google Sheets API and use Google Sheets as our database.

Problem: How do we store and fetch information for each event?

Constraints: The application must be able to dynamically access a database based on the parameters given to it.

Options: Google Sheets or Database as a Service

Google Sheets

Pros:
- Utilizing existing infrastructure
- Client has more experience using it
- Free
- Simple

Cons:
- Need to figure out how to use it
- Could be less efficient

Database as a Service

Pros:
- Could be more efficient
- Plenty of online documentation exists

Cons:
- Not Free
- Not Simple
- Client has less experience using it

Rationale: Because the client knows how to use Google Sheets, the application will access needed information from the Sheets he provides.

#### Decision 3
Summary: In order to create an interactive webpage, we decided to use Javascript.

Problem: In order to write code, we need to write it in a coding language.

Constraints: This language needs to work with wordpress.

Options: Javascript or PHP

Javascript

Pros:
- Build for writing interactive webpages
- Less complex for Front-End use

Cons:
- More complex for logic

PHP

Pros:
- Less complex for logic

Cons:
- Built for front-end and back-end logic
- More complex for Front-End use

Rationale: Because it was designed for interactive websites, we will be using Javascript.

#### Decision 4
Problem: We do not have the time or ability to create most of the javascript functions ourselves.

Constraints: It must provide functionality to javascript.

Options: React or Vue or our-own-thing

React:

Pros:
- Taught in the UNC curriculum
- A main javascript front-end
- Plenty or tutorials and resources for it
- Comes with plenty of UI functionality
	
Cons:
- Complicated
- Very large
- Learning curve

Vue:

Pros:
- Lightweight
- Easy to use
- Faster
	
Cons:
- Comes with less UI functionality
- Indepently developed
- Not taught in the UNC curriculum
	
Our-own-thing:

Pros:
- We would know how it works
	
Cons:
- Would be clunky, inefficient, poorly designed
- Cannot be finished within one semester
- Would need to provide continual support
- Would come with no UI funcionality
	
Decision: Because it fulfills all of our needs and was recommended by the mentor, we will be using the React framework.

### Architecture Diagram
![image](https://github.com/Deeakron/COMP-523-J/blob/gh-pages/comp523_architecture_diagram.png)
