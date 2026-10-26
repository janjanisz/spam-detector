# Spam detector : decision log 

## Stage 0 : setup

- Using the SMS Spam Collection dataset from UCI because i wanted access to a dataset of both spam, and non spam messages to work with, that did not risk me leaking any of my own messages or emails. This will allow me to publish the project on GitHub without any risk. 

-  Working in a virtual environment so that I can keep this project separate from any other project I create. If I installed a library without a .venv, it could interfere with another project and possibly cause some of that project's code to break. Working in a .venv also makes the project easier to reproduce on another computer, because it's clear which libraries were installed

- Working in a Jupyter notebook because the code that i write is split into cells, which i can run one at a time. This will help me identify errors easier, as the outputs of my code will be displayed underneath each cell. 

- requirements.txt is a file which displays all of the required libraries to run the code in my spam detector project, so that anyone who wants to reproduce my project, or run the code themselves, knows what libraries and versions respectively are needed to do so. They can install the correct versions of the libraries using `pip install -r requirements.txt`. This is needed because the .venv folder will not be uploaded to GitHub.

## Stage 1 : exploring the data 

- The dataset has a total of 5574 messages of which 4827 are ham (86.6%) and 747 are spam (13.4%)

- Because 86.6% of messages are ham, even a useless model that labels every message as ham would get 86.6% accuracy, while catching no spam at all . Thus, I won't trust accuracy alone, but i will check that my model beats an accuracy of 86.6%. 
Alongside this I can measure precision and recall, which can show how well it actually can handle spam.

- The average length of a ham message was 71 characters, whilst the average length of a spam message was 139 characters. This makes spam messages roughly twice as long as ham messages, and this statistic can be used to help understand whether a message is spam or ham. However, it's also important to not forget that the mean can be deceiving, as some ham messages can be long, and some spam can be very short. Whilst that stands, it is still a useful statistic to use for classification.