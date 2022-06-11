# Problem Statement 3

The problem statement for this project is provided.



# Data Collection 3

Was enough data gathered to generate a significant result? 3
- Yes. 12,277 unique titles were scraped.
Was data collected that was useful and relevant to the project? 3
- Yes
Was data collection and storage optimized through custom functions, pipelines, and/or automation? 3
- Good work using the built in libraries to open and write to the end of a file.
Was thought given to the server receiving the requests such as considering number of requests per second? 3
- Yes. Praw handles this.



# Data Cleaning and EDA 2

Are missing values imputed/handled appropriately? 3
- No missing values were present in the data.
Are distributions examined and described? 3
- Great work creating a custom function to help with examining distributions. The one thing I would recommend is when you interpret these distributions try to include how what you're seeing relates back to your overall project. How is what you are seeing informing your understanding of the data?
Are outliers identified and addressed? 2
- You did identify and address outliers by removing posts with more than 1000 comments and a score of over 5000 which was great. As a reader I was unsure why you choose these values to be the definitions of your outliers. Try to explain the logic behind your decision to use these values.
Are appropriate summary statistics provided? 3
- Yes. I liked that you provided statistics along with your histogram and boxplot interpretations. This helped to provide relevant information and drive home your interpretations.
Are steps taken during data cleaning and EDA framed appropriately? 3
- Yes
Does the student address whether or not they are likely to be able to answer their problem statement with the provided data given what they've discovered during EDA? 1
- You did great EDA however I was unsure if you felt you were likely to be able to answer your problem statement with the provided data.



# Preprocessing and Modeling 2

Is text data successfully converted to a matrix representation? 3
- Yes
Are methods such as stop words, stemming, and lemmatization explored? 3
- Stop words are removed and stemming is implemented.
Does the student properly split and/or sample the data for validation/training purposes? 2
- The one note I have here is to make sure you fit your tfidf vectorizer after you split your data and only fit it on your training set.
Does the student test and evaluate a variety of models to identify a production algorithm (AT MINIMUM: two models)? 3
- 3 models are tested and evaluated.
Does the student defend their choice of production model relevant to the data at hand and the problem? 2
- You choose your random forest model and you talked about it's feature importances. One thing you could do to help defend your choice relative to the data at hand is to talk about it's metrics in the context of your data. For instance you mentioned that that the random forest had the best sensitivity while the logistic regression had better specificity. Why might you care more about sensitivity vs specificity for this specific data and problem?
Does the student explain how the model works and evaluate its performance successes/downfalls? 2
- Great work looking at a lot of different metrics for your models. Similarly to the above feedback when you are looking at your models performance try to evaluate it within the context of your project. How might having a better or worse score in a particular area be a positive or negative for your project?



# Evaluation and Conceptual Understanding 2

Does the student accurately identify and explain the baseline score? 2
- You identified the baseline as being 49% however in a binary classification problem the baseline is the majority class which in your case would be 51%. This a small difference and should be a pretty quick fix for you.
Does the student select and use metrics relevant to the problem objective? 3
- Good work using a wide range of the classification metrics available to you.
Does the student interpret the results of their model for purposes of inference? 2
- Great work interpreting your models for inference and bringing those interpretations into your conclusions. Be careful when interpreting your logistic regression coefficients. When you pull them out of your model they speak to the change in log odds rather than the change in odds. If you want to interpret them as the change in odds make sure to use np.exp().
Is domain knowledge demonstrated when interpreting results? 2
- You demonstrated domain knowledge in your conclusions and recommendations. One area that could use a little more domain knowledge is your modeling section. I mentioned this above but when you are interpreting the metrics for a particular model try to tie what you are showing back to the problem at hand. Why might you care more about one metric vs the other and what impact would do they have on your project?
Does the student provide appropriate interpretation with regards to descriptive and inferential statistics? 3
- Yes



# Conclusion and Recommendations 3

Does the student provide appropriate context to connect individual steps back to the overall project? 3
- Good work explaining what parts of your project you were pulling your conclusions from to give context.
Is it clear how the final recommendations were reached? 3
- Yes
Are the conclusions/recommendations clearly stated? 3
- Yes
Does the conclusion answer the original problem statement? 3
- Yes
Does the student address how findings of this research can be applied for the benefit of stakeholders? 3
- Yes
Are future steps to move the project forward identified? 3
- Yes



# Project Organization 3

Are modules imported correctly (using appropriate aliases)? 3
- Yes
Are data imported/saved using relative paths? 3
- Yes
Does the README provide a good executive summary of the project? 3
- Great work here. After reading your executive summary I knew where you got your data from, what you were trying to accomplish, and what techniques/models you were going to use to accomplish it.
Is markdown formatting used appropriately to structure notebooks? 3
- Great work using a lot of markdown to help guide your reader through your thought process.
Are there an appropriate amount of comments to support the code? 3
- Great work again including comments to make your code more readable.
Are files & directories organized correctly? 3
- Yes
Are there unnecessary files included? 3
- No
Do files and directories have well-structured, appropriate, consistent names? 3
- Yes



# Visualizations 2

Are sufficient visualizations provided? 3
- Great work including a lot of visualizations in your EDA and model evaluation.
Do plots accurately demonstrate valid relationships? 3
- Yes
Are plots labeled properly? 3
- Yes
Are plots interpreted appropriately? 3
- Great work including markdown below your graphs so that your reader knows right away what the takeaways are.
Are plots formatted and scaled appropriately for inclusion in a notebook-based technical report? 2
- Your graphs for the most part are formatted and scaled appropriately for a notebook based technical report. The one thing you might consider for the future is making your titles and labels larger or making them bold. This will help draw your readers eye to the relevant information and make your graphs look a bit better.


# Python Syntax and Control Flow 2

Is care taken to write human readable code? 3
- Good work using explicit variable names for your functions.
Is the code syntactically correct (no runtime errors)? 3
- Yes
Does the code generate desired results (logically correct)? 3
- I could not find any inconsistencies in your code.
Does the code follows general best practices and style guidelines? 1
- For the most part your code follow the general best practices and style guidelines however you have some long lines that get cut off when rendered on a vertical screen. Additionally some of your functions break the recommended indentation rules. Check out https://peps.python.org/pep-0008/#introduction for a detailed style guide.
Are Pandas functions used appropriately? 3
- Yes
Are sklearn and NLTK methods used appropriately? 3
- Yes
