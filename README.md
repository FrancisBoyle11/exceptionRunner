Tasks to answer in your own README.md that you submit on Canvas:

1.  See logger.log, why is it different from the log to console?
    With the log we have warnings that specify a level. We use the log to log messages to help us analyze problems. The console displays exceptions. In this example, we see     that   
2.	Where does this line come from? FINER org.junit.jupiter.engine.execution.ConditionEvaluator logResult Evaluation of condition [org.junit.jupiter.engine.extension.DisabledCondition] resulted in: ConditionEvaluationResult [enabled = true, reason = '@Disabled is not present']
It comes from logger.info("Calling took: "+ (System.currentTimeMillis() - timeNow)). Once it starts evaluating an unexpected exception is encountered.
3.	What does Assertions.assertThrows do?
    Assertions.assertThrows asserts that a specific exception is thrown. In other words, it makes sure that the program encounters an exception. In this scenario, it asserts     that a TimerException is thrown. However, a NullPointerException is thrown, hence there is an exception.
4.  See TimerException and there are 3 questions.
5.  What is serialVersionUID why do we need it? (please read on Internet)
    The serialVersionUID is an id system that helps understand the specific version of class that we are using for serialization and deserialization. Exceptions happen to be     serializable classes, so we include this in the Exception class because we want in to work as intended, just like we do any other serializable class.
    Why do we need to override constructors?
    We override constructors to we get the desired functionality of the current class instead of that of the normal Exception class. 
    Why did we not override other Exception methods?
    We did not override the other Exception methods because we like the information that it offers. If we did this, we complicate our code for no reason. We like the product     of the other methods because it considers general exceptions and has the desired output. We only want to override the methods that do not help us in our task.
5.	The Timer.java has a static block static {}, what does it do? (determine when called by debugger) 
The static block begins execution when the Timer class gets initialized. The static block serves as a good way to initialize static variables. In this instance, upon the class’s initialization it opens the logger.properties file and sets the properties.

6.	What is README.md file format how is it related to bitbucket? (https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html)
The md format means MarkDown. According to the website, Bitbucket uses it for formatting texts. Second, Markdown can be used for README files and serve as descriptions for pull requests.
7.	Why is the test failing? What do we need to change in Timer? (fix that all tests pass and describe the issue)
The test checks for assertThrow of a TimerException while a NullPointerException is thrown. Thus, it cannot handle it and causes a problem. We need to ensure that a null value cannot be given to the statement in the finally branch.
8.	What is the actual issue here, what is the sequence of Exceptions and handlers (debug)?
The actual issue is that there is a NullPointerException. Sequence: It runs the assertThrows segment which tests for a TimerException.The timeToWait < 0 thus it throws a TimerException and goes to the finally branch. In the finally branch there is a NullPointerException that is not handled thus we have the issue.
11.	What category of Exceptions is TimerException and what is NullPointerException
-	A NullPointerException is considered a RuntimeException and a TimerException is implemented by extending the Exception class.
12.	Push the updated/fixed source code to your own repository.
https://github.com/FrancisBoyle11/exceptionRunner
