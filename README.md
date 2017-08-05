# Custom-Newsfeed-App
The app performs the following functionalities:
1.	Create a supervised training set with the Pocket App: <br/>
a.	Install Pocket Extension on Chrome (https://chrome.google.com/webstore/search/pocket) <br/>
b.	Set up Pocket API (https://getpocket.com/developer/apps/new) <br/>
    1.	Save articles to personal repository with a tag of our choosing (‘y’ for interesting articles and ‘n’ for non-interesting) – For creating supervised (tagged) training dataset <br />
    2.	Fetch the JSON data using the API <br />
2.	Download story bodies using Embed.ly API from URLs generated in Step 1 <br />
  a.	Set up Embed.ly (https://app.embed.ly/signup) <br />
  b.	Get story bodies using Embed.ly API <br />
3.	Transform the articles to the TF-IDF matrix to apply machine learning algorithms <br />
4.	Apply linear SVM to our data <br />
  a.	SVM attempts to linearly separate data points into classes using a maximum margin hyperplane (H3 in the below figure is the maximum margin line). SVM however does not work effectively when there is an overlap of points which can be solved in two ways <br />
    1.	Soft margin SVM : This formulation also maximizes the margin but at the cost of penalty of points that falls under the wrong side of the margin <br />
    2.	Kernel trick : This method transforms the data into a higher dimensional space where the data can be linearly separated (https://www.cs.utah.edu/~piyush/teaching/15-9-print.pdf) <br />
