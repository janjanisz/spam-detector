# Spam detector : decision log 

## Stage 0 : setup

- Using the SMS Spam Collection dataset from UCI because i wanted access to a dataset of both spam, and non spam messages to work with, that did not risk me leaking any of my own messages or emails. This will allow me to publish the project on GitHub without any risk. 

-  Working in a virtual environment so that I can keep this project separate from any other project I create. If I installed a library without a .venv, it could interfere with another project and possibly cause some of that project's code to break. Working in a .venv also makes the project easier to reproduce on another computer, because it's clear which libraries were installed

- Working in a Jupyter notebook because the code that i write is split into cells, which i can run one at a time. This will help me identify errors easier, as the outputs of my code will be displayed underneath each cell. 

- requirements.txt is a file which displays all of the required libraries to run the code in my spam detector project, so that anyone who wants to reproduce my project, or run the code themselves, knows what libraries and versions respectively are needed to do so. They can install the correct versions of the libraries using `pip install -r requirements.txt`. This is needed because the .venv folder will not be uploaded to GitHub.