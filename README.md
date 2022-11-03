Tasks to answer in your own README.md that you submit on Canvas:

1. See logger.log, why is it different from the log to console?
It provides additional information about the code, and in a defined format  
It includes information from security levels above the INFO level

2. Where does this line come from? FINER org.junit.jupiter.engine.execution.ConditionEvaluator logResult Evaluation of condition [org.junit.jupiter.engine.extension.DisabledCondition] resulted in: ConditionEvaluationResult [enabled = true, reason = '@Disabled is not present']
It comes from the logger.log file

3. What does Assertions.assertThrows do?
it checks if the test throws a given exception

4. See TimerException and there are 3 questions
    1. What is serialVersionUID and why do we need it? (please read on Internet)
         It is a member of a serializable class that uniquely identifies each instance of a class. 
         It's needed to check for compatibility of different class versions

    2. Why do we need to override constructors?
         so that we can extend the functionality of the constructor w/o losing the functionality of the superclass
         because we want to keep superclass functionality.
   
    3. Why we did not override other Exception methods?
       Exception constructors cannot be overridden. 
       We have to make separate constructors so that we can call the superclass's constructor and maintain functionality

5. The Timer.java has a static block static {}, what does it do? (determine when called by debugger)
It sets the properties of Timer's loggers to match what is specified in the logger.properties file, and doesn't allow 
Timer.java to be used until a logger.properties file exists in the correct location

6. What is README.md file format how is it related to bitbucket? (https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html)
The file is formatted in markdown language, which is used by bitbucket for pull request's descriptions or comments, and in
README files to provide information when viewing the repository from the browser  

7. Why is the test failing? what do we need to change in Timer? (fix that all tests pass and describe the issue)
The test fails because we aren't throwing what it expects us to throw. It is fixed when timeNow is initialized at the 
start of the function.

8. What is the actual issue here, what is the sequence of Exceptions and handlers (debug)
In the finally block, timeNow is being called on for arithmetic when it holds a null value. This causes the system to
throw a NullPointerException that is to be caught by a handler.
The exception happens first, and then the handler catches it.

9. Make a printScreen of your eclipse JUnit5 plugin run (JUnit window at the bottom panel)
10. Make a printScreen of your eclipse Maven test run, with console
11. What category of Exceptions is TimerException and what is NullPointerException
TimerException is a checked exception, and NullPointerException is an unchecked exception.

12. Push the updated/fixed source code to your own repository.
    https://bitbucket.org/jjw73012/exceptionrunner/src/master/