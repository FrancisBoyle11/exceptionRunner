Tasks to answer in your own README.md that you submit on Canvas:

1.  See logger.log, why is it different from the log to console?
    With the log we have warnings that specify a level. We use the log to log messages to help us analyze problems. The console displays exceptions. In this example, we see that       in the console exceptions and stack traces are displayed. While in the log we get a message with a FINER logging level for the same operations.
3.  Where does this line come from? FINER org.junit.jupiter.engine.execution.ConditionEvaluator logResult Evaluation of condition [org.junit.jupiter.engine.extension.DisabledCondition] resulted in: ConditionEvaluationResult [enabled = true, reason = '@Disabled is not present']
4.  What does Assertions.assertThrows do?
5.  See TimerException and there are 3 questions
    1.  What is serialVersionUID and why do we need it? (please read on Internet)
    2.  Why do we need to override constructors?
    3.  Why we did not override other Exception methods?	
6.  The Timer.java has a static block static {}, what does it do? (determine when called by debugger)
7.  What is README.md file format how is it related to bitbucket? (https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html)
8.  Why is the test failing? what do we need to change in Timer? (fix that all tests pass and describe the issue)
9.  What is the actual issue here, what is the sequence of Exceptions and handlers (debug)
10.  Make a printScreen of your eclipse JUnit5 plugin run (JUnit window at the bottom panel) 
11.  Make a printScreen of your eclipse Maven test run, with console
12.  What category of Exceptions is TimerException and what is NullPointerException
13.  Push the updated/fixed source code to your own repository.
