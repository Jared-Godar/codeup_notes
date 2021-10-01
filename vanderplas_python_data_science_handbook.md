# Python Data Science Handbook
## Essential Tools for Working With Data
### Jake VanderPlas 2017

--- 

Author: user and deleloper of Python scientific stack. Astronomer and interdisciplinary research director at University of Washington
---

Python is a first-class data science tool:
- Libraries for storing, manipulation, and gaining insight for data
    - **IPython**: computational environment
    - **Jupyter**: computational environment
    - **NUmPy**: including *ndarray* for storage and manipulation of dense data arrays
    - **Pandas**: *DatFrame* for storage and manipulation of labeled/columnar data
    - **Matplotlib** Flexible range of data visualizations
    - **Sckkit-Learn** machine learning
---

## Preface

### What is Data Science?

![DSVenn][\reading\images\dsven]

Surprisingly hard to nail down a data science definition. Ubiquitous term. Perhaps best lable for criss-disciplinary set of skills that are becoming increasingly important in many aplications across industry and academia.

Interdisciplinary with three distinct skills:
1. *Statisticial* who knows hoe to model and summarize data sets
2. *Computer scientist* who can design and use aldorithms to efficiently store, process, and visualize the data
3. *Domain expertise* necessary to formulate the right questions and put the answers in context.

### Target audience

Commonly asked "How should I learn Python?" From technically-minded students, developers, and researchers w

### Why python?

Emerged as first-class tool for scientific computing tasks, including the analysis and visualization of large datasets.

The usefulness of Python for data science stems primarily from the large and active ecosystem of third-party packages: NumPy for manipulation of homogeneous arraybased data, Pandas for manipulation of heterogeneous and labeled data, SciPy for common scientific computing tasks, Matplotlib for publication-quality visualizations, IPython for interactive execution and sharing of code, Scikit-Learn for machine
learning, and many more tools that will be mentioned in the following pages.

### Phtyon 2 v 3

Book uses python 3, not compatible with 2.x. Data scientists have had a slower transition to 3 because most of the toolkits needed time to catch up

### Supplementary material 

[GitHub](https://github.com/jakevdp/PythonDataScienceHandbook) 

Cloned into codeup-data-science

An attribution usually includes the title, author, publisher, and ISBN. For example, 

“Python Data Science Handbook by Jake VanderPlas (O’Reilly). Copyright 2017 Jake VanderPlas, 978-1-491-91205-8.”

### Installation Considerations

Anaconda includes both Python and conda, and additionally bundles a suite of other preinstalled packages geared toward scientific computing. Because of the size of this bundle, expect the installation to consume several gigabytes of disk space.

Throughout the text, we will also make use of other, more specialized tools in Python’s scientific ecosystem; installation is usually as easy as typing 

**`conda install *packagename*`**. 

For more information on conda, including information about creating
and using conda environments (which I would highly recommend), refer to conda’s [online documentation](http://conda.pydata.org/docs/).

### Conventions Used in This Book

The following typographical conventions are used in this book:

*Italic*
Indicates new terms, URLs, email addresses, filenames, and file extensions.

`Constant width`
Used for program listings, as well as within paragraphs to refer to program elements such as variable or function names, databases, data types, environment variables, statements, and keywords.

**`Constant width bold`**
Shows commands or other text that should be typed literally by the user.

*`Constant width italic`*
Shows text that should be replaced with user-supplied values or by values determined
by context.

### Safari (formerly Safari Books Online) 

Membership-based training and reference platform for enterprise, government, educators, and individuals.

Members have access to thousands of books, training videos, Learning Paths, interactive tutorials, and curated playlists from over 250 publishers, including O’Reilly Media, Harvard Business Review, Prentice Hall Professional, Addison-Wesley Professional, Microsoft Press, Sams, Que, Peachpit Press, Adobe, Focal Press, Cisco Press, John Wiley & Sons, Syngress, Morgan Kaufmann, IBM Redbooks, Packt, Adobe
Press, FT Press, Apress, Manning, New Riders, McGraw-Hill, Jones & Bartlett, and Course Technology, among others.

[For more information, please visit](http://oreilly.com/safari)

We have a [web page for this book](http://bit.ly/python-data-sci-handbook), where we list errata, examples, and any additional information. 

To comment or ask technical questions about this book, send email to bookquestions@oreilly.com.

For more information about our books, courses, conferences, and news, see our website
at http://www.oreilly.com.

Find us on [Facebook](http://facebook.com/oreilly)
Follow us on [Twitter](http://twitter.com/oreillymedia)
Watch us on [YouTube](http://www.youtube.com/oreillymedia)

