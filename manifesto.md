# Enabling Software Literacy

The Computer has changed the way we live, work and play dramatically and is certainly one of the most important inventions in the history of humanity. But compared to books and the printing press, we're still in the dark ages. The real computer revolution has yet to happen.

For millenia, text was authored and understood by only a tiny fraction of society, the scholars. The general public was not interested nor encouraged to read and write. Literacy was deemed too advanced a skill for most people and their only access to the written word remained through the weekly interpretation of the local scholar. This power over text let a handful of institutions control the thoughts and lives of the illiterate.

Besides social norms, the most important reason for a limited access to books was that they were expensive to produce, mostly because of the cost of making copies. The small therefore number of books and even smaller numbers of producers meant there was no reason to learn to read yourself. Hearing the reading and interpretation every Sunday seemed good enough. And you wouldn't even think about writing a book unless you had a very good reason, enough funds and of course the permission of the ones in charge.

The printing press reduced the production cost of texts enough so that people with unconstitutional ideas could afford to write and publish them. Soon there were so many books, that in order access them, you simply had to learn to read yourself. Eventually, the ideas you found would inspire your own ideas worth writing about. The result of this upword spiral of literacy was that in a 100 years we learned far more about our universe and ourselves than in the 1000 years before.

The scholars of our times, the ones who have full access to the medium computer, are called programmers. Instead of static text or graphics, they produce, analyse and manipulate dynamic models which can interact with their environment. The users only get access to a small portion of the models, interpreted through a user interface. The institutions in control of these models and interpretations, and therefore making the rules we live by, are international coporations. The general public is not interested nor encouraged to become software literate, unless to join one of the institutions.

Although software is as good as free to copy, producing it is still very costly since it requires a vast amount of specialized knowledge and training. There is no printing press for software yet. Something that reduces production costs enough to enable an upward spiral of software literacy. If we achieve this, the result could be even more transformative than the scientific revolution.


## What is Software Literacy?

Software literacy is the ability to not just *use* software, but create, understand, change and share dynamic models through software. Like text literacy, being software literate comes with many personal advantages. Here's one example.

Mary owns a small restaurant. She is software literate but not a professional programmer. She uses an extensive suite of software to run her business, which she could probably not create herself but she is able to **understand** what these systems do and how they do it. Instead of seeing magical black boxes, she feels in control of her devices. Today she looked at the data that her new smart fridge sends to its manufacturer and is relieved to see that it only includes total operation time and malfunctions.

For today she planned to work on her new customer prediction software. In the past she regularly misjudged how busy the place would be the next evening so she was either understaffed or had to send waiters home. Trying to express her intuitions in software forced her to **think** about her own mental models regarding how people behave. She had to find a way to explicitly express something that so far was always just a gut feeling.

To make a good prediction, she **learned** about many aspects of human behaviour, specifically about group dynamics. She noticed for example, that the time of when the first customer arrives heavily influences the total number of customers for any given evening. She tested this theory by asking friends to come at specific times and integrated the results into the model.

Last week she sent the model to a fellow software literate restaurant owner, to find out how well it worked in his case. Immediately he found an assumption that didn't hold in his case but still it worked surprisingly well. Mary is already looking forward to improve the model even more through this **collaboration**.

During her lunch break, her friend asks her why she learned about software in the first place. Mary tells her that it was the fact that her ordering system did not allow customers to change their mind after the order has been sent to the kitchen. Mary suspected that she lost a couple of regulars because of that, but she could not convince the developers to change it. So she learned to do it herself. Mary realizes that it's this feeling of **empowerment**, to be able to solve her own problems, that she treasures the most about being software literate.


## What makes Software difficult?

Like writing a good novel, creating a complex software system is inherently difficult. But even doing something equivalent to a shopping list in software requires a substantial investment. For most small problems you can find specialized tools, but they have their own drawbacks. These tools are by definition limited and therefore also 
limit the kind of ideas you can express with them. The same pen and paper can be used to write a shopping list or an award-winning novel. Having to learn a new tool impedes the transition from one to the other unneccessarly.

Software authoring tools without this limitation are called general-purpose programming languages. But while these give you a greater freedom of expression, most of them also put a series of hurdles in your way before you can successfully create, manipulate and share you first piece of software.

Imagine you are using some software that doesn't match your needs exactly, so you want to adapt it. The first thing you need to do is to **set-up** the supporting platform on your own system. If you're unlucky, this might require administration rights that you don't have or something else goes wrong and it ends up taking hours.

After that, you need to be able to *build* the system you want to change. This means you have to download all of its **dependencies**. If you're lucky, it's a single command. But you probably have to install additional tools to run it or external dependencies like databases. All of these come with their own potentially cumbersome setup requirements. And it might be that if you want to change just the version of a single dependency, the whole build fails.

All of this is necessary to turn a bunch of code into a running, working application. To change something, you have to manipulate that code. For that, you have to familiarize yourself with its **syntax** and obey it precisely. A single misplaced character will make the whole system impossible to run.

Besides spelling everything correctly, you also have to use thee right words, since every element of the system only understands a very limited vocabulary defined by its **programming interface**. If you're lucky, somebody wrote down somewhere what these words are, how they should be used and what they do. Otherwise you have to find out yourself by trial-and-error or reading the code which hopefully is accessible and uses the same syntax.

Once you know the right words and syntax, you can make changes to the code. But in order to see their effects, you have to build the system and run it from zero, for every tiny change. And everytime you **lose your context** and have to recreate all state that you need to observe the changed behaviour.

And even if you find a way to keep your context, you still need to continously switch between the environment in which the software runs and the one where you can edit its code. This **segregation** means that you cannot "look under the hood" of the running system. For each of its pieces you have to somehow find the corresponding code yourself.

And that's only the code. Usually apart from it you also have the data that your software either uses as input or generates as output. The thing with data is that in order to save it to your harddrive or send it over a network, it has to be **seriaalized** - transformed from reacting, rich, connected elements to a dead, flat and isolated string of ones and zeros. And everytime you want to use that data again, you have to interpret that string of ones and zeros and reconstitute all its context and meaning.

That only works of course if the data has not been accidentally overwritten or deleted. For every bit of information you have to deal with **data safety** by making backups or prohibiting accidental actions. The same goes for the code.

But you've taken all these hurdles and successfully created or manipulated your software and now you want to **share** it with the world because you're sure that others can profit from it as well. But how do you make sure it works on their computers?

So you decide it might be easier to just run it on your own computer and serialize everything back and forth. But now you need a big powerful machine which is costly to maintain or a lot of work or both. You also need to rent an address or add your software to a central repository. Seems like you can't share your creation without losing **autonomy**.

Another problem with running your software on someonen else's computer is that you have to convince them that your software does not do anything bad to their machine, since every software they run can do everything they do, including reading and deleting personal files. And if instead you decide to only run it on your own computer, you're now responsible for the **security** of everybody's data. Good luck with that.


## How can we make it easier?

None of these hurdles are essential to programming, but they all contribute to making software harder and more expensive than it has to be. Yet for every complication there is at least one software plattform that successfully avoids it. In order to make software cheaper and reduce training time to almost zero, we need a tool that avoids all of these incidental complications without decreasing power and limiting expressive freedom.

The result would be a new, a better web of dynamic models. A more open, more democratic, more flexible, more empowering and more secure platform to communicate through and with computers. A platform that allows everyone to participate and contribute freely and safely. A platform that makes writing software easy and fun - and accessible to everyone. A platform that enables software literacy. This is the goal of [zells](http://zells.org).
