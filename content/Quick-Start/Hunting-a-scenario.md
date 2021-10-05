> Hunting a simple scenario

After the [installation](content/Quick-Start/Installation.md), open the board that the addon is installed on it, and click the Scenario Hunting icon. 

![Open the addon](images/open-addon.png)
Notice that the name of the messages (like `Remove items from basket`) is separated from the fields of the message (like `customer id, product id, amount`), and the fields are separated by `line` or by comma (`,`).

As you see it's going to lead us to reverse narrate the test scenario we want to hunt without losing our focus on the model. 

![The addon is opened](images/addon-opened.png)

It asks us to select the "Then" step of the test. Let's select it. 


![the "Then" step was selected](images/then-step-selected.png)

Then select the "When" step

![The "When" step was selected](images/when-step-selected.png)

And the system under test, or in short the "Subject"

![The "Subject" was selected](images/subject-selected.png)

And let's select or type the "Context" (the context in which the test scenario is meaningful)

![The "Context" was selected](images/context-selected.png)

And now we have enough data to be able to name the scenario. Let's type a name for it. 

![The "Scenario" was selected](images/scenario-title-selected.png)

Now let's select a template that generates `C#` aggregate test code. (More on templates later)

![Select a template](images/select-template.png)

Now we can check if the "When" step provides enough data to the subject to enable it to calculate the expected "Then" step, or some preconditions should be added to the scneario, but let's skip it for now, and save the scenario.

![Save the scenario](images/save-the-scenario.png)

By clicking the save button the code is downloaded to the default download folder of my browser. And since I've deliberately set the download folder of this browser to my project's folder, the test code is downloaded right to the root of my project folder. So I can access the code from my IDE of choice. 
Programming language and design style are variables, and we will discuss them later.

![The test was downloaded](images/test-downloaded.png)

We derived the test code from the design so far. 
Now we can start to solve this exciting puzzle.
First, the build should be passed.
The compiler turns the test into a todo list for us.

![The test won't build](images/test-won't-build.png)

 Refactoring tools can be used to add the missing classes, methods, and functions as fast as possible.

![The missing classes, methods and functions are added, and test is built](images/test-built.png)

The build is passed successfully. Let's run the test, and let the failures tell us what to implement next.

![Test failed after passing the build](images/test-failed-1.png)

Before starting to implement, it turns out that passing `customerId` to `RemoveItemsFromBasket` is redundant, because each basket belongs only to a single customer. So let's remove this parameter.

![CustomerId removed](images/customerId-removed.png)

But should it be removed from the board too? 
No! Because the command handler needs it to fetch basket aggregates from repository before removing items from them.

![Command](images/command.png)

That a field is removed from code, but not from the board, is another indicator that a precondition is missing. But let's ignore it for now, and implement the test.


