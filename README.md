Overview:

This is a project that has the purpose of helping educators create responsive quizzes for their students so that students can learn from their mistakes instantly, rather than waiting a couple weeks before recieving results
for their answers to a quiz. This allows students to instantly see where they lack knowledege in a subject, and the quiz also gives feedback as to why a student's answer to a quiz maybe correct or incorrect.
The project does this by creating a wrapper between the front end of the application and Google Gemini, through VertaxAI, and Google Cloud. The program generates questions based on uploaded pdfs data that is stored in a local
ChromaDb, where each of the pieces of text data from the pdfs are set as a unique set of vector embeddings. The teacher chooses a topic that they want the quiz to be on, and the number of questions that they want the quiz to
have for the students to answer and recieve feedback on. 

The program allows ChromaDb to communicate with Google Gemini and the Google Cloud, in order to instantly generate unique quizzes for course content that a teacher is teching. This will both allow the teacher to spend more time
teaching content to students, and also gives students insights on their strengths and weaknesses for the course content.

The program is seperated into 10 tasks:

Task 1 and 2: Setup Google Cloud, and personal environment. This can be done by cloning and forking the radicalai repository for quizify.

Task 3: In this task we setup a DocumentProcessor for the teacher, Streamlit for the frontend, and the Python library langchain for the backend to use the PyPDFLoader. The program allows for multiple pages of data to be uploaded
to the uploader, to allow for multiple pdfs to be processed at the same time.

Task 4: In this task, the program uses langchain to create an EmbeddingClient, that will take chunks of text data and convert them into vector embeddings.

Task 5: In this task, the program uses the EmbeddingClient created in Task 4, and the DocumentProcessor in Task 3 to create a Chroma database of the uploaded pdfs, and the related vector embeddings for the texts in the pdfs

Task 6: In this task, the program uses the EmbeddingClient, DocumentProcessor, and the ChromaCollection, along with a Streamlit front end to ask the user for a topic of the quiz, and the number of questions they want for the quiz,
and then displays the results of a query for data that matches the topics inputted by the teacher, using the nearest neighbors algorithm.

Task 7: In this task, the program expands on task 6, and adds to the funtionality by generating one quesiton related to the topic inputted by the teacher, and generating the associated correct answer to the question, and an
explanation as to why the answer is correct

Task 8: In this task, the program expands upon task 7, and adds the functionality of generating n questions related to the topic inputted by the teacher, where n is a number between 1 and 10, that is the number of questions
that the teacher wishes to have on the quiz

Task 9: In this task, the program expands upon task 8, and uses Streamlit to fix the UI of the quiz for one question, where the user is able to interact with a Streamlit form that displays the AI generated question, and gives
a multiple choice based options of possibly correct answers

Task 10: In this task, the program expands upon task 9, and uses Streamlit to fix all remaining UI issues in Task 9. This means that the program will show the user that their answer is correct or wrong, and give an explanation as to why,
the program will also allow the user to flip through all questions.

How to run the program:

First, ensure that you have all libraries installed using the following command:

pip install requirements.txt

Once all libraries are installed or up to date, cd tasks/task_10 and run the following command in terminal:

streamlit run task10.py

Things that I want to add to this project:

Right now the project generate n questions for one inputted topics, however, I want to add the functionality of allowing the teacher to
input x files, and input multiple topics, and for each topics the program will generate n questions using anyone of the x files of data
that the program has available to it.

Thank you for your time, and I hope you have a great rest of your day.
Puneetpal Powar




