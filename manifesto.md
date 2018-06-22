# zells - Enabling Software Literacy

Computers are amazing. They let us connect with friends on the other side of the globe, access endless streams of entertainment, be super heroes, discover new truths about our universe, and bring a million other wonders that would have been considered pure magic a couple of generations ago. And yet, in spite of these achievements, we still live in the Dark Ages of computing.

To unleash the full power of computers, we need to increase the number of software literate people - people who can write and read software, not just use it. And just like most people aren't professional authors, the goal is not for everybody to be professional software developers, but to enable every person with access to a computer to express their own ideas, as well as understand and build upon powerful ideas of others through the medium of software.

**The mission of *zells* is to work towards Universal Software Literacy by drastically decreasing the cost of writing, reading, changing, and sharing dynamic models.**


## Software as a Medium

Hundreds of years ago, before the Age of Enlightenment, producing texts was incredibly expensive. They had to be written on rare paper and bundled up into bulky and fragile books. They could only be written by well trained professionals, were usually big and complicated, and therefore took a long time to write. Only the largest and wealthiest institutions could afford to create them, and controlled which texts were written and which were not. With a tiny number of books around and reading being considered difficult to learn, people instead listened to their interpretations at weekly gatherings. It was free, easy and convenient.

Few people could imagine a world of universal literacy where text is virtually everywhere and almost everybody can access and contribute to an ever growing corpus of collective human knowledge. It wasn't until the invention of the printing press that text production became cheap enough to start an upward spiral of printed books and literate citizens, which ultimately lead to the Scientific Revolution.

Four millennia after the first written word marked the beginning of history, the invention of the computer gave us a new medium, one of executable dynamic models - called software. It lets us express ideas not only statically - being identical for every reader - but also dynamically - reacting to a changing world and interacting with its users. The potential of this new medium to augment the human intellect was already described 50 years ago, yet almost nobody is literate, let alone fluent in it.

Instead of learning to express our own ideas, and understand those of others enough to change and reproduce them, we are content with the limited interpretations and options that user interfaces give us, making their designers our priests, their companies our churches, and their developers our monks. To enable Software Literacy, we need a printing press for software. A way to make software cheap enough to start a spiral of accessible dynamic models and software literate citizens, which could lead to the next cognitive revolution.


## The Cost of Software

To make software cheaper, we need to understand what it is that makes it expensive. The hardware necessary to run it is definitely a factor, but a rapidly decreasing one. Also, a single computer is enough to access the entire library of all existing software, so the contribution of hardware cost to each individual piece is tiny.

Software is expensive because software developers are expensive. And developers are expensive, because it requires years of training to become a good one. The reason that you can get many programs for the equivalent of a cup of coffee or even for free, is that it's almost free to copy software. So every user only has to contribute a tiny fraction to its total cost. But the cost is always enormous, even if only consisting of volunteered evenings.

Why is this extensive training necessary? Because many software projects are big and complex. It's all but simple to build something that works, is fast, reliable, and solves an actual problem for thousands if not millions of people. Complex problems require complex solutions, which causes the majority of complications that make these projects expensive. These are essential complications.

But what about simple problems? Maybe you just want to write a little app that helps you with organizing your household chores. It only has to work somewhat, doesn't has to be very fast or reliable and only has to solve your own problem. Why is that still difficult to write? This is because of accidental complications.

Writing a novel or reading a scientific paper is hard, because of essential complications inherent in the task itself. It takes years of practice to become a good novelist or scientist. But writing a letter to your mother is easy. All you need is a pen and paper. If you would have to make your own paper from trees and your own pen from goose feathers, that would be accidental complications, because if would only keep you from writing that letter.


## Accidental Complications

To find out what the accidental complications of software are, let's follow a hypothetical coffee shop owner Mary, who recently noticed that the queues in her shop are getting longer and longer. She wants to find out what would be the best way to increase the shop's throughput - the number of coffees sold per hour. The options are to either hire more staff or buy more machines. She thinks software can help her with this problem and indeed finds a coffee shop simulation which seems to fit her needs. But after a first glance Mary realizes that it only simulates Cappuccinos, not the other five variants of coffee that she serves. Luckily, Mary is software literate and the simulation is open-source which means she can adapt it to her needs. Theoretically.

Mary's first challenge is to overcome the **segregation** of the execution and authoring environments of the simulation. To run it, all she had to do was download and open it. But to modify it, she has to find its source code, download it, and "build" it - turning the code into its executable form.

To do so, she needs to first **set up** the programming platform that the simulation was written for. This includes downloading and installing another program, which takes her only half an hour but she remembers another time when a whole day was gone before she had a platform installed and working.

The next step is to download and install all the **dependencies** of the simulation - pieces of software, so-called libraries, which the simulation depends on, but are distributed separately. Since many libraries in turn depend on other libraries, most platforms have programs for downloading and installing them. But even with such a dependency manager, this step still feels like a lottery to Mary, since it either works or it doesn't, and there is usually little she can do in the latter case. This time all libraries are successfully installed and it only took her two hours to build the coffee shop simulation from source. That's over a hundred times slower than just running it but she is still happy since it usually takes longer.

In order to add the other kinds of coffee to the simulation, Mary has to learn the **syntax** of the programming language - the meaning and rules of its words and punctuation. Every language has a different syntax of which some are quite cryptic. Since Mary is not familiar with the one she is facing, she makes many mistakes - mostly forgotten colons, parentheses or accidentally using spaces instead of tabs. These mistakes are even harder to find by the unhelpful error messages that she is presented with. Instead of a simple "you forgot a colon here", the only clue she gets is the number of the line where the code stopped making sense to the computer, which is sometimes miles aways from the actual mistake.

Even once Mary has learned the syntax, in order to modify the simulation, she has to understand its structure and behavior. But all she has to go by is static text in files, with very little hints on what a certain part is actually doing or how it is connected with other parts. It seems to her like the program was never intended to be **read and understood** by another person - and she is probably right. She knows there is a well thought-out mental model hidden in these files, but it takes her hours to put the pieces together.

She does this mostly by using a scientific approach: study the code, guess what a piece does, change it a little bit, run the program and see if she guessed right. While she likes being able to experiment with the model this way, she is annoyed that every time she wants to change a piece of code, she needs to restart the program, **losing its state**. With every restart, she has to configure the simulation again - define how many machines and staff members there should be and how long it takes to grind the beans, brew the coffee and foam the milk.

And even after she figured out what a certain piece of the program does, she still has to **discover the protocol**, the very limited vocabulary and sentence structures that she can use to make the piece do what she wants it to do. There is some documentation explaining the protocols, but more often than not it's outdated, so she has to infer them from the code.

Eventually she figured it out and even found an open-source project that models how a Frappuccino is made which would save her quite some time if she could use it in her simulation. But unfortunately, it was written in another programming language. And even though the two languages are very similar, she can't **access other languages** from within her simulation. There is no other way - she had to write the Frapuccino model herself.

Now that the simulation fits her situation, Mary can finally find out what the total coffee throughput looks like for different numbers of staff and machines. She wants to save the result for each scenario on the hard drive disk in order to compare them, so she has to serialize them. **Serialization** is the act of transforming a multi-dimensional, interconnected data structure, into a one-dimensional string of bits, which has to be done every time before saving data to disk or sending it over a wire. During this transformation, a lot of contextual information gets lost which has to recreated when reading the results back into memory.

But even if the structure can be re-created, the lost context means that a correct **interpretation** is needed to make sense of the simulation results. So Mary has to make sure that she serializes them in exactly the format that her analytics program understands. It takes Mary several dozen tries to get this fragile process right since even the slightest deviation means she can't use the result at all. Luckily, she only uses very simple data and finally manages to save it in the correct format. More complex information, e.g. web pages, are almost impossible to interpret correctly or even to decide what "correct" means.

After Mary simulated many different scenarios and is looking forward to the insights she might get from the collected data, she realizes that she accidentally used the same file name for saving the results of each run. That means that all results except the last one were overridden. Because of this lack of **data safety**, she lost the results of several hours of work.

Too frustrated to repeat the whole procedure, Mary decides to push it to another day and instead wants to **share** her version of the simulation with her friend Joe from across town who also owns a coffee shop and might benefit from it. This means though that he too has to set-up the platform, install all dependencies and build the program before he can run it. It takes him several hours but in the end he gets the simulation running.

The next day Joe calls Mary and asks why her program accesses his address book file where he keeps the personal information of his customers. After hours of digging, Mary discovers that some library that was downloaded as a dependency of a dependency contained malicious code that searches for address book files and uploads them to a private forum on the Web. Because of the weak **security** of her operating system and a lack of control over what program may and may not do, the customers personal information got stolen.

Even worse, the next day a customer tells her that he thought her shop was closed since its Facebook page has disappeared. Puzzled, Mary checks her emails and indeed finds one from Facebook saying that her page was suspended because it "violated the terms and conditions" - without any further details. After several weeks of emails and calls, Mary still doesn't know why her page was suspended. She realizes that she gave Facebook too much control over her digital existence, sacrificing her **autonomy** for convenience. But at least she doesn't have to worry about increasing the shop's throughput anymore since without the page the number of her customers has halved.


## Advantages of Software Literacy

But even though devastated by her struggles with the numerous accidental complications of software development, Mary kept at her simulation project and eventually got it working securely and robustly.

In the end she is glad to be software literate, since it helps her with **understanding** all the physical and virtual things around her. Before, things like her cash register, ATMs or most apps on her phone were black boxes to her. Now she understands how they work, why if not, and what risks are involved when using them. The world seems a little less magical, but she enjoys the feeling that, if she wanted to, she could probably learn to build and control any of these things.

When putting an idea of herself into software, Mary also notices that she spends a lot of time thinking about her own thoughts and often times she only really understood a concept after expressing it on software. This **thinking about thinking** eventually became second nature and not only helped her with her business, but also with personal problems.

She also enjoys using software like the simulation for **learning** new things about her business by experimenting with different scenarios and seeing how things change.

Software literacy lets her use a more **scientific** approach to running her shop. Instead of gut feelings and anecdotes, she is able to support her decisions with data collected from simulations. Instinctively, she wouldn't have taken the risk of hiring a new staff member, but the data show that this will increase throughput more economically than a new machine.

And once she had expressed an idea in software, she enjoys how easy it is to improve it by **collaborating** with her peers. After she made the simulation safe to run, Joe added some of his knowledge about coffee brewing so now it's even more accurate.

But the one thing she likes the best about being software literate is how **empowering** it is. She can create her own simulations, set-up her own website and booking system and solve her own problems. She would never want to give that up.


## Software without Complications

The vision of *zells* is a world in which people like Mary are able to take advantage of the full power of software, without having to struggle through accidental complications. A world where you can easily write, read, share and collaborate on ideas using dynamic models instead of static artifacts, without constantly having to solve problems that are not essential to your goal.

Although for every mentioned complication there exists already at least one software platform that successfully avoids it, in order to make software sufficiently inexpensive to enable Software Literacy, we need a platform that avoids all accidental complications without decreasing its usefulness or usability.

Writing software should be as easy as picking up a pen and paper. Reading it should be as easy as opening a book. Sharing dynamic models should be as easy as showing a drawing to a friend. And shaping an idea together should be as easy as molding clay. This is the goal of [zells](http://zells.org).