## Recommendations_Engine_with_IBM
Udacity Data Science Nanodegree - Recommendation Engines project

### Overview
This project works with the articles hosted with IBM and analyzes user interactions to create 
recommendations to users for content to view. This is performed via Rank and Collaborative-based
recommendations and evaluated via SVD. Code has been leveraged from the class instructor / lessons, 
and from the Peer/Mentor discussion boards.

### ToC
1. [Libraries](#libraries)
2. [File Descriptions](#files)
3. [Recommendations_with_IBM](#project)
4. [Results](#results)

### Libraries <a name="libraries"></a>
The following libraries were utilized:
* Pandas
* Numpy
* Matplotlib
* Pickle
* Progressbar (required "pip install" in the Udacity workspace)

### File Descriptions <a name="files"></a>
* Recommendations_with_IBM.ipynb: Primary Jupyter Notebook project file containing all code. Can be run as-is.
* Recommendations_with_IBM.html: HTLM version of the Jupyter Notebook project file.
* Data:
  - user-item-interactions.csv: CSV file containing user interactions with the articles (user email, article id) hosted by IBM.
  - articles_community.csv: CSV file containing article information (title, summary, etc.)

### Recommendations_with_IBM Summary <a name="project"></a>
The project file is based on the following structure:
    I. Exploratory Data Analysis
    II. Rank Based Recommendations
    III. User-User Based Collaborative Filtering
    IV. Content Based Recommendations (EXTRA - NOT REQUIRED)
    V. Matrix Factorization
Section IV was not performed (Extra).

### Results <a name="results"></a> 
The overall effort was based on a very small subset of data due to the sparse nature of the original dataset. As seen in the 
initial exploration, most users only interact with 3 or fewer articles. This leads to problems during SVD where our train / test
data sets are heavily restricted. The resulting accuracy is "high" at 96% when using several hundred latent features, but this
is not to be taken as representative of all the data since much of that data says there was no interaction. To improve, we would
suggest merging in additional recommendations: continue with trying collaborative first, but combine rank and content based 
recommendations using keywords from the title and summaries and showing the top articles from that subset of content.
