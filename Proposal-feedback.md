Empirical-ApiUsage
==================

### Some general feedback:

* The proposal is vague about what exactly will be analyzed.  If API usage is studied, then, what parts of the API will you focus on?  Classes?  Methods?
* Which apis/communities will you focus on?  Having a good criteria for selecting different types of Apis/Communities will make the analysis more compelling.  For example, small communities, versus big communities.  New technologies (such as Swift) vs old technologies.    Competing technologies (iPhone vs Android), ruby on rails vs django.
* I would suggest increasing your targetted number of communities to something more like 5-6 communities.  This will help you get a wider coverage of topics to work with.
* "finding various statistics about these" is too vague of a goal.  If any thing the main goal here seems to do a "replication study" on a different set of data.  Just state that.  Then, extract out the high level goals as originally stated in the previous work.
* How will you represent the API?  In my previous work, I parsed the javadoc or used xml representations to extract the classes and packages automatically.  I would suggest finding something like this first.
* Some more thinking on the final metrics used.  Will you just use coverage?  Code samples?

### Writing feedback

* First sentenance is a run-on.
* "a lot of codes" should use more formal language.
* "difficulties surrounding software community"
* First sentenance of Motivation section can be written more simply: "Some libraries/APIs are used more frequently than others".  Then, there is an opportunity to follow up with motivation: Our goal is to explore the factors that explain why certain libraries and particular subsets of libraries become more popular than others.


### Some useful related work:

* [Making Sense of Online Code Snippets](https://cs.uwaterloo.ca/~rtholmes/papers/msr_2013_subramanian.pdf)

### Code resources

The code used in my previous work is listed here:

https://github.com/chrisparnin/anacrowd

This would probably be very useful for importing and parsing out content from the dataset; however, I would caution against directly using my code as you might find it easier to create your own infrastructure, especially if you want to use something like Hadoop, and then incorporate a little bit at a time.
