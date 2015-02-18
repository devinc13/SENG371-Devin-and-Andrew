# SENG371-Devin-and-Andrew

##Our Project Question: 
How does the number of progressive (new feature) and anti-regressive (maintenance) changes over time affect the number of bugs discovered?

##Methodology: 
We will gather data to create graphs of progressive changes, anti-regressive changes and the number of reported bugs. The data on bugs, anti-regressive and progressive changes will be taken by performing searches in the GitHub issue tracker, which can be searched using "bug created:2012-11-01..2012-12-01" to specify the dates of tickets created with the word bug in them, or "label:bug created:2012-11-01..2012-12-01" if that project uses a label to represent bugs. We have created a python script that hits GitHub's API in monthly increments to search the number of issues or pull requests with certain queries and/or labels.

##Codebases/Systems: 
Ruby on Rails (6674 issues - GitHub issue tracker): https://github.com/rails/rails, node.js (5608 issues - GitHub issue tracker): https://github.com/joyent/node and Bootstrap (10,820 issues - GitHub issue tracker): https://github.com/twbs/bootstrap

##Milestones: 
1. Done by Feb 4th - Gather data on number of reported bugs per month for each codebase.
2. Done by Feb 11th - Gather data on number of progressive and anti-regressive changes each month.
3. Done by Feb 18th - Use data to create graphs or similar visual ways to represent the data.
4. Done by Feb 18th - Review STAT 260 and decide on cool statistics stuff we can do with the data!
5. Done by Feb 23rd - Draw conclusions.

##Notes:
For Ruby on Rails, they don't use labels to differentiate pull requests or issues, so we needed to do keyword searches. For bugs, we searched for the word "bug", for anti-regressive changes we searched for "refactor OR rewrite" and for progressive changes we searched for "feature".

##Python Script Usage:
bugCounter.py -u (githubUsername) -p (githubPassword) -a (startYear) -b (startMonth) -c (endYear) -d (endMonth) -o (owner) -r (repository) -q (query) -l (label)

* The -l and -q arguments for adding a label and a query is optional

** Username and password are used to improve the GitHub API's rate limit from 5 requests per minute to 20 requests per minute. USE AT YOUR OWN RISK!
![Bootstrap](/Bootstrap.jpg "Bootstrap")