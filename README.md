# ProfFeeds
A website that records student feedbacks on a course and professor and uses sentiment analysis to rate the professor. Also, it eliminates and replaces any profane words from the comments. 

The website is created using Flask and displays information that can be used by new students about the course and the professor. This includes the professor's name, comments by students, and their ratings.

The LSTM model was trained on past comments(provided through a csv file) and appropriate labels and attained an accuracy of around 70%. The LSTM model uses NLTK for text preprocessing, LSTM for training ML model, providing 5-level label(Excellent, Good, Neutral, Bad, Very Bad) for each comment and calculates an average label for each professor.

The comments/feedbacks provided by students are then filtered for any profane words using better_profanity library and these are replaced with less harmful words using HuggingFace BERT AI transformer with GPT2Tokenizer which operates on GPT2(free).

Finally, the UI displays the filtered comments along with an average label. This would help students gauge the course before applying to a course.
