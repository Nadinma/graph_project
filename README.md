# Graph for Interaction Flow

#### High level description of project: this project is a demonstration of how Data Scientists identify problematic areas within an organization. In this case a Data Science specialist doesn’t particularly solve the problem for you, but a DS specialist can direct to the right solution. 

[More detailed scrypt](https://github.com/Nadinma/graph_project/blob/main/graph_serach_project.ipynb)

### Intro / EDA

The goal of this project is to explore the interaction flow of an organization and build a framework that will help the HR department to narrow down problematic areas in a big organization with hundreds or thousands employees.

My dataset consisted of “calendar meetings over a 3 month period from an anonymous business". Most departments and titles have been renamed (changed) due to data sensitivity.  

During my exploratory data analysis I’ve managed to form 3 different sub-graphs, which were not connected to each other. Two sub-graphs were very small and I decided to remove them and keep them as a topic for separate investigation. From here on I will be only focusing on the largest of these 3 networks, which I believe is the main structure of the organization.

I was ably to identify 738 individuals who formed 19935 connections, which are either one-on-one meetings or group meetings with three or more people. Also I was able to split this main network  into 11 smaller communities, which could be considered as departments or product groups. 

### TechStack 
For my work I used such tools as Pandas, Numpy, Matplotlib, Gephi, Python, Networkx

### Centrality
The main concept I applied in my research is centrality, which helps to understand  importance of people in the network in a given perspective and can be expressed in different ways; there are multiple types of centrality measures. 
Degree centrality - the most connected people within a network - most popular, 
Betweenness centrality -  People or who connect network together the most - gatekeepers, and 
Closeness centrality - People spread information very efficiently through the network - influencers. 

### Degree Centrality - Most Connected, who can be called local opinion leaders
I highlighted top 4 most connected - CEO; VP of Product #1, VP of Product #2; VP of Product #3. Which sounds kind of normal based on their positions. When I explored communities separately they still appeared as most connected. Which tells us that they are not only formal leaders by holding their status, they actually leading the communities. 

Pict###

But for deeper investigation I would ask the next questions: 

