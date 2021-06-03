# Graph for Interaction Flow

#### High level description of project: this project is a demonstration of how Data Scientists identify problematic areas within an organization. In this case a Data Science specialist doesn’t particularly solve the problem for you, but a DS specialist can direct to the right solution. 

[More detailed here](https://github.com/Nadinma/graph_project/blob/main/graph_serach_project.ipynb)

### Intro / EDA

The goal of this project is to explore the interaction flow of an organization and build a framework that will help the HR department to narrow down problematic areas in a big organization with hundreds or thousands employees.

My dataset consisted of “calendar meetings over a 3 month period from an anonymous business". Most departments and titles have been renamed (changed) due to data sensitivity.  

During my exploratory data analysis I’ve managed to form 3 different sub-graphs, which were not connected to each other. Two sub-graphs were very small and I decided to remove them and keep them as a topic for separate investigation. From here on I will be only focusing on the largest of these 3 networks, which I believe is the main structure of the organization.

I was ably to identify 738 individuals who formed 19935 connections, which are either one-on-one meetings or group meetings with three or more people. Also I was able to split this main network  into 11 smaller communities, which could be considered as departments or product groups. 


![] (https://github.com/Nadinma/graph_project/blob/main/images/Communities.png)

### TechStack 
For my work I used such tools as Pandas, Numpy, Matplotlib, Gephi, Python, Networkx

### Centrality
The main concept I applied in my research is centrality, which helps to understand  importance of people in the network in a given perspective and can be expressed in different ways; there are multiple types of centrality measures. 
Degree centrality - the most connected people within a network - most popular, 
Betweenness centrality -  People or who connect network together the most - gatekeepers, and 
Closeness centrality - People spread information very efficiently through the network - influencers. 

### Degree Centrality - Most Connected, who can be called local opinion leaders
I highlighted top 4 most connected - CEO; VP of Product #1, VP of Product #2; VP of Product #3. Which sounds kind of normal based on their positions. When I explored communities separately they still appeared as most connected. Which tells us that they are not only formal leaders by holding their status, they actually leading the communities. 


![] (https://github.com/Nadinma/graph_project/blob/main/images/DegreeCentrality.png)

But for deeper investigation I would ask the next questions: 
- Why are they involved in local meetings?
- Do they delegate enough?
- What happens if we remove a node? 

### Degree Centrality - Two other layers 
I decided to check and see who are the next most popular or connected people, after removing previously mentioned positions, I’ve got another layer of VPs, then I removed them too. Now we can see most employees are having similar level of popularity which tells us that the structure of this particular organization is more flat. Some departments are flatter than the others like number 6 and 3. 


![] (https://github.com/Nadinma/graph_project/blob/main/images/DegreeCentrality_2layers.png)

### Degree Centrality - Least Connected / Popular
Let’s look at the situation from the opposite side and think about least connected people - they are the brightest dots on the picture. 
It may be ok for them to be kind of isolated because of the nature of their work. 
But what if: 
- there is a problem with communication tools and channels?
- inclusivity issues?
- reasons why these people may not be included in planning process?

![] (https://github.com/Nadinma/graph_project/blob/main/images/Least%20Connected.png)

### Betweenness Centrality
To assess global opinion leadership, the closeness and betweenness centrality measures are better suited.
Let’s continue with our gatekeepers. Here we can see top four people with high traffic. 
We’ve got two new players - Lead and VP of product #4. 
If three individuals are around the same level, but the forth one (Lead) needs a deeper look.  


![] (https://github.com/Nadinma/graph_project/blob/main/images/BetweennessCentrality.png)

Questions for deeper exploration: 
- Is Lead an outlier?
- Is there a problem of duplicated functionality? 
- Are they effective or just bottleneck?

### Closeness centrality
And here our influencers or people that are able to spread information very efficiently through the network. We can see top four and they are the same people. We can conclude that they are empowered by the organization - they are formal and informal leaders. They are working inward and outward by connecting their teams inside and with teams outside together. 


![] (https://github.com/Nadinma/graph_project/blob/main/images/ClosennessCentrality.png)

But still some questions here:
- Are they the only people that effectively spread the information?
- Do others have enough resources and channels to spread the information?
- Do we want to involve more people in planning process? 

### Next Steps 
There is more work to do here and I would look at:
From Business Perspective:
- Teams survey 
- 360° review for highlighted people
- Work with HR and Department Leads to get more targeted problems and solutions

Friom Data Perspective: 
- Layers 
- Communities 
- Shapley Betweenness Centrality, which calculates the value of a node by examing repercussions of the node failing (being removed from the network) on different subsections of the network. Essentially, if the removal of a node were to be detrimental to any group of nodes, the node will have high Shapley betweenness centrality.

