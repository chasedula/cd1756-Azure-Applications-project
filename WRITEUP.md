# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

Cost:
VM's are typically more expensive than App Services. For this use case, an app service is best as a VM would be overkill in terms of compute power leading to wasted money/resources.

Scalability:
Both VM's and App Services can be scaled but to differing degrees. App Services have a maximum of 14gb of memory and 4 compute cores per instance. This pales in comparison to the specs that a single VM can be outfitted with and that's before grouping multiple VM's on the same task. For this use case, an app service is perfect as the workload is very light.

Availability:
Being in the MS cloud, both options provide excellent uptime/availability. Either option would fit this use case so it depends on the other factors to make a decision.

Workflow:
VM's allow full control over the host machine all the way down to the operating system that it's running. App Services don't have that level of customization but they do make it extremely easy to run continous deployment via GitHub, ADO, or other Git options. For this use case, the App Service makes the most sense as students are making changes to config.py, views.py, and others during development and testing.

Selection/Justification:
I chose to work with an App Service for this project as it is lightweight, cheaper, and enables continuous deployment. Being able to push changes from VSCode to GitHub and having GitHub immediately start updating my app was very helpful. It also made the most sense given the complexity of this application.


### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

The app would have to grow well beyond its original feature set to even approach VM territory. Beyond that, the only other need to go to a VM setup for this would be if it were so popular as to need load balancing.