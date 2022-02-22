Have you ever wondered whether you should keep developing further the code you are working on?
The questions that forms in your head of future scenarios where things might not be enough?
Welcome to overengineering. But what does it actually mean to overengineer?
```ad-note
to engineer (something, such as a product) to have more functions, capabilities, etc. than are necessary or desirable
```
[Merriam-Webster definition of 'engineer']([https://www.merriam-webster.com/dictionary/overengineer')

From the definition above, it feels like when we think of failing scenarios in the future we nudge ourselves to start overengineering. 
In the rest of the article you will find where overengineering can happen, guidelines to prevent overengineering and what you can do instead.
You might be thinking now, what's the difference between preventing and 'do this instead of' overengineering. 
There is a difference here between preventing and what we can pro-actively do.
Preventing is stopping us from overengineering in the first place, and pro-actively doing something to prepare us for future enhancements.

# Why do we overengineer?
I believe that overengineering comes from
1. lack of clearly defined requirements
2. fear of what might happen in the future
3. human factor

## Lack of clearly defined requirements
In the old days of waterfall development, we did a lot of requirements gathering and design up front, and no coding. 
This methodology has it's fair share of failed projects without even a working system to show up for it.
Fast forward a few decades we went from a waterfall model to a spiral model and landed to where we are now with agile.
We went from rigorous requirements gathering and design upfront to writing code with some requirements to writing code and user stories.
The problem with most user stories are that the requirements are not part of the story itself. A typical user story would look like
![[User-Story-and-Description-1024x679.png|400]]

What we are missing here are the requirements (functional/non-functional). 
Without requirements we are free to interpret the user story as we see fit.
Best case scenario, we have achieved what we ideally should have achieved design or code wise.
Average case scenario would be that we've overengineered, delayed the product launch, upset stakeholders, and went a bit over budget.
Most importantly, the product is working as expected.
Worst case scenario would be that we've underengineered, taken some shortcuts, and unknowingly introduced bugs or defects, but we have launched on time and have happy stakeholders.

We can do better much better by providing the requirements in the acceptance criteria of the user story.
You can even take it up a notch, you can even describe your requirements in plain spoken language on how your system should behave and translate it to something like [Gherking](https://cucumber.io/) and have semi-working tests for your requirements.
If that got you excited, you should read up on BDD (Behaviour Driven development).

The big question is of course, how do we come up with requirements?
We have to start asking questions and receive realistic answers.
E.g. 'What should happen if user A does thing Y?', or 'How should it behave if thing X happens?'
The goal here is to gather the right amount of requirements so we don't under or overengineer, and solve for the problem we currently have.
Here are some of my favorite techniques and methods
1. Impact mapping (for finding your goal)
2. MoSCoW method (for setting your requirements)
3. BDD (living documentation and acceptance tests)

## Fear of what might happen in the future
To give you an idea of what I mean, we can go overboard with defensive programming, worrying about scaling issues and known unknowns.
All of these activities can be a potential time suck. So make sure you stay in the present and solve problems you currently have.

## Human factor
```ad-todo
Should I write about the human factor? or leave it out
```

# On what levels can we overengineer?
On one axis we have
1. architecture
2. design
3. code

On another axis we have
1. functional requirements
2. non-functional requirements

![[functional-vs-nonfunctional.png|functional vs non-functional]]

## When do we overengineer?

Looking at the diagram I say that overengineering mostly occurs into the right half of the diagram.
This could mean that while thinking/working on certain feature, we haven't given it enough thought on the non-functional requirements.
Or it's also possible we might be able to lower overengineering if we have the list of non-functional requirement beforehand. 
![[functional-vs-nonfunctional-with-arrows.png]]

Now, if we want to get an idea where underengineering and overengineering occurs, I would say that underengineering mostly occurs in the left half of the diagram.
When we want to prevent underengineering, make sure your functional requirements are complete.

![[functional-vs-nonfunctional-with-arrows-2.png]]

# How to prevent overengineering
1. Figure out the 'WHY' (goal) and 'WHAT' (requirements)
2. Actively ask questions. 
3. Have your work reviewed
4. Stay in the present, don't solve problems you think you might have in the future.
5. Mind the scope creep

# How to actively prepare for overengineering
By following good software engineering practices you should have software (code or architecture wise) which is both low coupling and high cohesion. 
1. built-in fexibility and minimize impact of change (from impact change analysis)
2. keep things SOLID
3. Solve problems you have and not what you might have