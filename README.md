Hypothesis testing using PyMC3 based on the study "How Do FOSS (Free &amp; Open-Source Software) Communities Decide to Accept Pull Requests?(EASE’20)"
DOIs: https://doi.org/10.1145/3383219.3383242 

I the paper, researchers study how different Free & Open-Source Software (FOSS) communities handle
Pull Requests (PRs). The working hypothesis is that there are three dominant models
in which projects handle PRs. They name this models as protective, equitable and lenient. 
They have prepared a survey on PR handling and collected responses from members of the follow-
ing FOSS communities: FOSSASIA, Odoo, Linux Kernel, Coala, ROS, Plone, ReactJS, NodeJS,
OpenGenus, Mozilla, OpenSUSE, jQuery, and Apache.


In total, there are 380 responses. The responses are stored in the file pseudonymized-data.csv. 
It contains only answers to 7 quantitative questions relevant for this analysis:
V27. In general I say no to most pull requests (PR)/patches. The contributor has to be persistent
and prove that the PR/patch is worth evaluating.
V28. I don’t consider a pull request/patch, unless I trust the contributor.
V29. I don’t consider a pull request/patch, unless the contributor is reliable.
V30. I don’t consider a pull request/patch, unless I have a strong relationship with the contributor.
V31. I assess every pull request/patch in the same manner irrespective of the contributor.
V32. I assess pull requests/patches purely on technical grounds.
V33. I never say no to a pull request/patch. If the quality of the PR/patch is not mergeable, then
I mentor the contributor to elevate his/her PR/patch to a mergeable state.


The participants in the survey selected a mark from the Likert scale to answer each question:
1. Strongly Agree, 2. Agree, 3. Neutral, 4. Disagree, 5. Strongly Diasgree.
In the CSV file, -1 in the community file means ’other’ (so none of the listed above), and -1 in any
other column means that the respective question has not been answered.

They are interested in comparing how protective and lenient the different communities are. Below
they precisely describe the criteria to classify a community within a category.

Protective. A community is protective when the response from this community is positive to
question V29:
V29: I don't consider a pull request/patch, unless the contributor is reliable.

Equitable. A community is equitable when its response is positive to the following question:
V31: I assess every pull request/patch in the same manner irrespective of the contributor.

Lenient. A community is lenient when its response to question V33 is positive:
V33: I never say no to a pull request/patch. If the quality of the PR/patch is not mergeable



The task is to test the following hypotheses using Bayesian Data Analysis:
• H1: The Coala Community is more lenient than the Linux Kernel Community.
• H2: All communities show either a protective or equitable style of governance for pull requests
(so for each community answers to V29 and V31 are different)
