# NLP-Capstone
## Coursera - Johns Hopkins University Data Science Specialization Capstone
* Author:  James Francisco PhD
* Date: April 14, 2019  
* [Email to james.r.francisco@outlook.com](mailto:james.r.francisco@outlook.com)  
* [GitHub Code Repository](https://github.com/JamesFrancisco/JHU-Capstone)
* [Presentation RPubs url](http://rpubs.com/JFrancisco1958/NextWordPredictionApp)
* [Shiny App URL](https://jrfanalytics.shinyapps.io/DataScience_Capstone_App/)

## Coursera Data Science Capstone Project
The Coursera Data Science Specialization Capstone project from Johns Hopkins University (JHU) allows 
students to create a usable public data product that can show their skills to potential 
employers. Projects are drawn from real-world problems and are conducted with industry, government, 
and academic partners. In this part of the course JHU partnered with SwiftKey 
(https://swiftkey.com/) to apply data science in the area of natural language processing.

## Next word prediction app (using N-gram models)
- based on N-gram model with "Stupid Backoff" ([Brants et al 2007](http://www.cs.columbia.edu/~smaskey/CS6998-0412/supportmaterial/langmodel_mapreduce.pdf))
- checks if highest-order (in this case, n=4) n-gram has been seen. If not "degrades" to a lower-order model (n=3, 2)
- built on the `cracklib-small` dictionary, Cracklib is a library tool finds potential words quickly, by using an index file to access dictionary words, and by keeping a table to assist binary searching.

For additional prediction accuracy were also used:
- Good-Turing Smoothing
- MLE
- linear-regression
- linguistic tweaks

## Dataset
The underlying dataset for this word prediction app was gathered from three English language sources provided by Swiftkey:

* Blogs
* News
* Twitter

The original english corpus combined over 580 MB of language information. Which summed up to over half a billion characters. After processing the data our model consists out of **millions of ngram tokens**.

### The project consisted on several parts:
  1. Getting the data
  2. Data splitting
  3. Data cleaning and tokenization
  4. Building an n-gram model
  5. Building a predictive model
  6. Building the final shiny app
  
### How to run the code:
- Simply run the shipy app server from the  `shiny` dir.

- Or build your own prediction model first. In order to do this just go to the "scripts" folder, configure "config.r" and run "run.r". Because of the volume of data, this will take a while.

### Additional information
All R scripts, files, presentations etc. in this repository are materials prepared for the capstone project course of the Coursera Data Science specialization developed by professors of Johns Hopkins University Bloomberg School of Public Health in cooperation with SwiftKey.

- Learn more about the Coursera Data Science Specialization: [https://www.coursera.org/specialization/jhudatascience](https://www.coursera.org/specialization/jhudatascience)