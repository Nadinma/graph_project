# Graph for Interaction Flow

#### High level description of project: this project is a demonstration of how Data Scientists identify problematic areas within an organization. In this case a Data Science specialist doesn’t particularly solve the problem for you, but a DS specialist can direct to the right solution. 

[More detailed scrypt](https://github.com/Nadinma/graph_project/blob/main/graph_serach_project.ipynb)

### Intro

The goal of this project is to explore the interaction flow of an organization and build a framework that will help the HR department to narrow down problematic areas in a big organization with hundreds or thousands employees.

My dataset consisted of “calendar meetings over a 3 month period from an anonymous business". Most departments and titles have been renamed (changed) due to data sensitivity.  

During my exploratory data analysis I’ve managed to form 3 different sub-graphs, which were not connected to each other. Two sub-graphs were very small and I decided to remove them and keep them as a topic for separate investigation. From here on I will be only focusing on the largest of these 3 networks, which I believe is the main structure of the organization.

I was ably to identify 738 individuals who formed 19935 connections, which are either one-on-one meetings or group meetings with three or more people. Also I was able to split this main network  into 11 smaller communities, which could be considered as departments or product groups. 




