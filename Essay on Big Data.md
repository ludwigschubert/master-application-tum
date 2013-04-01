% From ubiquitous sensors to insights
% Ludwig Schubert
% March 24, 2013

Application to TUM's Master Program in Computer Science, Essay subject 2: *What is the impact of ubiquitous sensors and how does Informatics help to analyze the collected data?*
This essay is written in Markdown. The body-only word count is 1002. References are given in [square brackets] and are listed at the end of the document.

# From ubiquitous sensors to insights

## Towards the "Internet of Things"

Cheaper sensor prices, large-scale adoption of portable computing devices and a growing degree of interconnection between electronic devices cause a massive increase of produced data.[McKinsey] Today's vision of how this trend will culminate, the "Internet of Things", would mean a global network with vastly more participants than humans on earth. 

My scale uploading my weight to an online portal where my smartphone can use it during my runs[Withings] to calculate burned calories gives merely a humble preview of the interconnectedness we're facing.

This unprecedented growth in required storage and processing capabilities poses a set of challenges for Informatics to overcome. Pure volume is the first unsolved problem.

In fact, data volume is growing faster than storage volume; and since 2009 has surpassed available storage volume. [IDC, pp. 9–10] It's hard to overstate the paradigm shift this induces: we are literally running out of memory and processing power to cope with the onslaught of data.

Additionally, organization, meaningful statistics, visualization, long-term storage, secure access and lack of structure & comparability are equally problematic.

## Informatics - Enabler & Innovator

Informatics acts both as an enabler—by providing efficient algorithms and new data structures to deal with this increased amount of data—and as an innovator—by finding new use cases and computing meaningful results which extract value from those large amounts of data.

### Informatics as an Enabler

Informatics can help programmers in dealing with those large amounts of data. 

Currently the only practical way of handling this data is parallel computing. Since parallel programming is inherently hard[McKenney], Informatics can assist developers by creating new programming languages, frameworks or models which abstract the parallelization layer away from them. Popular examples are the MapReduce programming model [MapReduce], Bigtable as an alternative to traditional relational database systems [Bigtable], and the key-value store Dynamo [Dynamo].

But one can even observe new programming languages being created with built-in support for concurrency, enabling easy parallelization of code, like Google's Go. Since those new languages often build on older, pre-established concepts (in the case of go's concurrency support: Hoare's Communicating Sequential Processes) older languages that suit the concurrent programming styles are resurgent, such as Erlang. It originated in the late eighties, but today by web companies like Facebook and Wooga use it to support their massive user bases. Erlang offers language-level support for concurrency similar to the aforementioned Go.

However, even the biggest data processing capability is by itself a means, not an end. To extract meaningful information even from condensed data it is often needed to visualize the results in a way that is approachable to humans. The last years saw an increase in the usage of data rich "info-graphics" in journalistic publications that is unlikely to wear off soon. The general increase in data driven decision-making in the industry will need even more visualization techniques and talent. This in turn will likely lead to a closer collaboration between designers and coders, or even new kinds of jobs with overlapping responsibilities. Rune Madsen, for example, already holds a graduate course called "printing code" for which he argues "during the last decade [the line between graphic design and programming] has obviously blurred, but not to the degree one would expect"[…]. I'm expecting this development to continue, especially outside the field of scientific visualization and towards more general data visualization for businesses. 

### Informatics as an Innovator

While a historic example, Google's Page Rank algorithm can in hindsight serve as an excellent example of a data-driven innovation. [Rajaraman] argues that the simple use of *more data*—as in "including anchor text of links linking to", in addition to "the content of" a website—was the pivotal improvement in search engine utility.

Future startups and scientific applications can possibly make similar advancements by including data that hadn't been included previously into their datasets, or by not having to restrict big datasets at all. [Halevy] retells how an in-painting algorithm that performed poorly with a few thousand images in its training data set suddenly became very useful when researchers expanded said dataset by several orders of magnitude.

In general it is much harder to predict Informatics' role as an innovator than as an enabler – after all, enough real world challenges already exists in which a better information distribution can improve performance. It is inherent to innovations to not be  predictable beforehand. However, one can extrapolate from current trends which areas computer scientist are currently studying intensively.

Three subfields that readily come to (my) mind are Natural Language Processing, Artificial Intelligence and Cluster Computing. Both NLP and AI will profit greatly from the possible increase in data size and less selective data samples. Cluster Computing on the other hand is already rapidly advancing, as de-facto standards have emerged in the industry (e.g. Hadoop) that have already been surpassed hundredfold in speed by newer research projects. (e.g. UCB's Spark)

Summing up, Informatics is at an exiting point in time now – for the first time, data management problems have grown so big that we literally can't fix them by increasing resources. We will have to find more advanced processes.

## Conclusion

Like any new technological development in the past, Big Data starts out as an inherently value-neutral concept. Nuclear power comes to mind, mechanical printing, BitTorrent or even the Internet itself. But in the same way that BitTorrent leaves the decision to download widely available illegal content to its users, Big Data puts computer scientists in a position of social responsibility that most of us don't seem to realize. Constant surveillance by myriads of sensors and data collectors can just as easily restrict human freedom as it can enable it. But unlike programming models or tools for enabling large-scale data processing, I'm not aware of any kind of reusable concepts which informatics could offer to avoid such harmful usage. The moral judgement remains—as it has always been—in the hands of the individual developer.

# References

*References which have not been used in the text to back up statements have been used for general research and are still listed here.*

[IDC] IDC, “A Digital Universe Decade – Are You Ready?,” vol. 2009, no. Figure 1, 2010.
[Bigtable] F. Chang, J. Dean, and S. Ghemawat, “Bigtable: A distributed storage system for structured data,” ACM Transactions on …, 2008.
[McKenney] P. McKenney, M. Gupta, and M. Michael, “Is parallel programming hard, and if so, why?,” 2009.
[Rajaraman] A. Rajaraman, “More data usually beats better algorithms,” 2008. [Online]. Available: http://anand.typepad.com/datawocky/2008/03/more-data-usual.html. [Accessed: 18-Mar-2013].
[Boyd] D. Boyd and K. Crawford, “Six provocations for big data,” pp. 1–17, 2011.
[McKinsey] J. Manyika, M. Chui, B. Brown, and J. Bughin, “Big data: The next frontier for innovation, competition, and productivity,” McKinsey Global Institute, no. June, 2011.
[Withings] “Withings Smart Body Analyzer + Runkeeper + Weightbot.” [Online]. Available: http://www.withings.com/en/bodyanalyzer. [Accessed: 31-Mar-2013].
[Dynamo] G. Decandia, D. Hastorun, M. Jampani, G. Kakulapati, A. Lakshman, A. Pilchin, S. Sivasubramanian, P. Vosshall, and W. Vogels, “Dynamo: amazon’s highly available key-value store,” ACM SIGOPS …, pp. 205–220, 2007.
[MapReduce] J. Dean and S. Ghemawat, “MapReduce: simplified data processing on large clusters,” Communications of the ACM, pp. 1–13, 2008.
[Ghemawat] S. Ghemawat, H. Gobioff, and S. Leung, “The Google file system,” ACM SIGOPS Operating Systems …, vol. 37, no. 5, p. 29, Dec. 2003.
[Ma] Y. Ma, M. Richards, M. Ghanem, Y. Guo, and J. Hassard, “Air Pollution Monitoring and Mining Based on Sensor Grid in London,” Sensors, vol. 8, no. 6, pp. 3601–3623, Jun. 2008.
[Halevy] A. Halevy, P. Norvig, and F. Pereira, “The Unreasonable Effectiveness of Data,” IEEE Intelligent Systems, vol. 24, no. 2, pp. 8–12, Mar. 2009.
[Madsen] “Rune Madsen – Printing Code course description” [Online]. Available: http://runemadsen.com/printing-code. [Accessed: 01-Apr-2013].
[Li] I. Li, “Personal informatics & context: Using context to reveal factors that affect behavior,” Journal of Ambient Intelligence and Smart …, no. August, 2012.