# What are "asynchronous" functions?

Some functions require a lot of compute time and resources because they process or search the whole data set of the slip box. These functions run through a program loop that does not give "feedback" until everything is done. During the processing the program does not react. Users may interpret this as a program crash, although the program is still running correctly. Neither the user nor the operating system can estimate when the program has completed its operations due the lack of the program feedback. With the help of asynchronization, the program starts a second process that runs "on the side" and does not stop the rest of the program. Thus, the program always gives feedback and the user also knows how long he has to wait.

## null

Program: Zettelkasten - Homepage, FAQ, http://zettelkasten.danielluedecke.de/ [ID 2]

