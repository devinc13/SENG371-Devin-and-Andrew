# SENG371-Devin-and-Andrew

##Our Project Question: 
How does the number of progressive (new feature) and anti-regressive (maintenance) changes over time affect the number of bugs discovered?

##Methodology: 
We will gather data to create graphs of progressive changes, anti-regressive changes and the number of reported bugs. The data on bugs will be taken from issue trackers in open source repositories (eg. JIRA, TestRail, Trac), or from performing searches in the GitHub issue tracker, which can be searched using "bug created:2012-11-01..2012-12-01" to specify the dates of tickets created with the word bug in them, or "label:bug created:2012-11-01..2012-12-01" if that project uses a label to represent bugs. The data on progressive and anti-regressive changes will be collected from change-logs, from searching the issue tracker (similar to the bug search) and gource (to find large re-factorings).

##Codebases/Systems: 
Ruby on Rails (6674 issues - GitHub issue tracker): https://github.com/rails/rails, node.js (5608 issues - GitHub issue tracker): https://github.com/joyent/node and Bootstrap (10,820 issues - GitHub issue tracker): https://github.com/twbs/bootstrap

##Milestones: 
1. Done by Feb 4th - Gather data on number of reported bugs per month for each codebase.
2. Done by Feb 11th - Gather data on number of progressive and anti-regressive changes each month.
3. Done by Feb 18th - Use data to create graphs or similar visual ways to represent the data.
4. Done by Feb 18th - Review STAT 260 and decide on cool statistics stuff we can do with the data!
5. Done by Feb 23rd - Draw conclusions.

##Python Script Usage:
bugCounter.py -u (githubUsername) -p (githubPassword) -a (startYear) -b (startMonth) -c (endYear) -d (endMonth) -o (owner) -r (repository) -q (query)

** Username and password are used to improve the GitHub API's rate limit from 5 requests per minute to 20 requests per minute. USE AT YOUR OWN RISK!
