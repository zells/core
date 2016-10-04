# Enabling Software Literacy

Software nowadays is fundamentally broken. It's limited, never quite works the way we want it to, but it can't be changed, can't be combined and can't be trusted.

More and more, users are put into - sometimes golden - cages, and forced to hand over their ideas, personal information, and even identities to international quasi-monopolies that put everything into walled gardens which the creator can only access through tiny keyholes.

To fix this, we need to increase the currently tiny number of people who are able to write, modify, combine and share software. We need a tool that makes writing software easy and fun. One that enables software literacy.


## What's this about?

This document focuses on the problems that *zells* means to solve. The following sections describe why these problems need to be solved, what the problems are, the solution, and finally how it solves each previously described problem. If you've never written a piece of software, most of the described problems will be unknown to you, but some are universal and affect everybody.

The purpose of this document is to provide a basis for discussion about the justification of the project as well as validity and effectiveness of its approach.


## Why is Software Literacy important?

In a world more and more controlled by software, **understanding** how the systems work that we interact with every day can eliminate a lot of frustration and superstition. Just as knowing why apples fall down and aeroplanes fly up, the citizens of the 21st century need to know that computers are not magical boxes but composed of dynamic models.

Such models are ideal for **learning** about the inner workings of this universe that we live in, because the best way to understand something is to try to replicate it. And in the virtual world of computers, everything can be replicated, from complex physical phenomena to abstract ideas, and even your own mind.

To do so requires **thinking** about your own thinking and describing your own, oftentimes unconscious, mental models. This enhances your analytical and logical skills as well as your ability of self-reflection which benefits any part of life.

Once a mental model is externalized as software, it can be shared and improved in **collaboration**, across time and space. This allows to discuss ideas at a drastically different level. Ideas are no longer static descriptions that need to be read and understood. Encoded in software, they are living, responsive systems that can be tested and interacted with directly, independently from their creator.

But maybe most important is the **empowerment** that software literacy brings to its holder. Being able to solve your own problems means you no longer depend on somebody else to care, understand and solve them for you. And you can build exactly what you need or adapt something that is close. And by leveraging the power of automation, you can solve your problems faster, and more reliably than by hand.

The benefits of *understanding*, *learning*, *thinking*, *collaboration* and *empowerment* that a wide-spread software literacy could provide for humanity would eclipse even the impact of the printing press and the steam engine. It would be a true computer revolution.


## What prevents Software Literacy?

Despite the many advantages of software literacy, learning how to write software is not an easy task nor is practising it a very pleasant one. One reason is certainly the current society and culture of programmers which is evidently uninviting for newcomers. But with a larger and more diverse community of software literates, this problem solves itself. Another, more fundamental reason is that solving complex problems is inherently complicated. But the fact that even the simplest problem is unproportionally difficult so solve with software nowadays, indicates that there must be unnecessary, incidental complications that make it harder than it needs to be.

A tool that is to enable software literacy must eliminate most if not all incidental complications. So what are they?

The most important one might be the **segregation** of authoring and using software. This prohibits the user from inspecting the software they are using in order to understand it on a deeper level and manipulate its data in ways unanticipated by its developers. It also makes modifying it very difficult. Even if it's legally possible, you not only need to access the source code and understand it, you also need to be able to rebuild the program from that source.

To do so, requires to **set-up** the software platform but also all the software needed to transform the source code into a running program. This usually requires some expertise in the operating system and more often than not the permission to make system-wide changes which is not always given.

Another reason that prevents a user from modifying a software is that it might be written in a **syntax** that is unknown to them, since every software platform dictates its own which must be learned and memorized.

But even more idiosyncratic are the libraries of a specific platform. There is usually no **discoverability** for which libraries exist and how they are used. Instead, external documentation and help from peers is required for even the simplest tasks that are not memorized.

And even after all platform-specific hurdles are taken, there is no obvious link between the change of a code segment and the effect it has on the program execution. Few development environments provide true **interactivity** when analysing the running program so modifications have an immediate effect. Instead, the program must be rebuilt and much of the previous state recreated.

An additional complication when writing software and also building from source are external **dependencies**. Almost every software depends on other software which needs to be acquired and installed in its entirety, even if only a small part is used. This software might itself depend on further software and so on. In the worst case, two dependencies depend on the same software but in different, conflicting versions.

Managing these dependencies can be avoided by using remote services. But amongst other complications they introduce like authentication, they require **serialization** of all data that is sent or received. This process is oftentimes very cumbersome since a lot of information is lost during serialization which then needs to be restored, usually by hand. Also, any data that needs to be stored, for example in a file or database, must be serialized.

Storing to disk is necessary for **data safety**, since any data that is not saved is lost as soon as the program is terminated. This is almost always the case for the program's state (which is sometimes desired) and especially for the undo buffer. Many times important data has been lost by either not saving or accidentally overwriting it.

But perhaps most frustrating (and not only for software writers) is the fact that even decades after the creation of the internet, **sharing** a piece of software is still an unsolved problem. This is especially true for programs but also for videos, pictures and formatted text. You either need to send it to a - hopefully trusted and secure - third party or to each recipient individually. In any case, you have to make sure that the computer of the recipient is able to interpret the content. This requires to export it to several formats which then need to be kept in sync with the source. But even then the sent version is quickly out of date.

As a result, the most popular way of creating and sharing content is through a service provider, oftentimes a for-profit company whose bottom line might not be aligned with the interests of its users. This loss of **autonomy** usually goes hand in hand with loss of control over one's creations and virtual identity, along with earned reputation. Neither can be transferred to another provider in case the current one can no longer be trusted or goes out of business.

And last but not least, **security** is a major and oftentimes overlooked challenge. This includes creating secure programs but also protecting your own system, data and personal information form malicious software and people. Passwords provide pseudo-security at best. Too much trust is required to be given to some software, and not enough can be given to other.


## So what's the Solution?

The tool that eliminates all these incidental complications, is a global software platform, based on a unified programming model consisting of *composable*, *distributed*, *secure*, *persistent*, *dynamic* and *abstractable* objects, called *cells*.

**Composable** - Each cell has a name and can contain any number of other cells. This forms a hierarchy where every cell is uniquely identified by its canonical path. 

**Distributed** - All cells exist in a single, globally shared hierarchy. It does not matter where a cell is physically located. It can be on your own computer or on any other in the network. It can seamlessly move between them and even be on multiple devices at once. 

**Secure** - Every user can access any cell in this hierarchy, but only with a digitally signed permission by its owner. Therefore all user identities and permissions are secured by cryptographic algorithms and asymmetric keys.

**Persistent** - Any change to a cell is automatically saved, along with the entire history of all changes, including possibly alternative timelines.

**Dynamic** - Cells have behaviour by reacting to messages consisting of another cell. This way, a cell can control how it looks and reacts to input.

**Abstractable** - Each cell is deduced from another cell. The new cell inherits the reaction and children of this stem cell which it can then overwrite. This way, properties shared by several cells can be combined in a single cell and do not need to be duplicated unnecessarily.


## How does this solve anything?

The platform can be accessed through multiple interfaces, including command line. But the most useful one is a virtual canvas that cells can draw themselves on, and through which the user can interact with them. The program needs no installation which minimizes the **set-up** costs. These can be further lowered by providing an implementation that runs inside a web-browser. Any cell can then be accessed and manipulated by simply opening a web site.

The canvas is used for displaying but also for modifying a cell, either directly through a context menu or by opening an *inspector* for it. The inspector shows the cell's hierarchy and provides a means for standard operations such as renaming, creating, deleting, setting the type and changing the behaviour of a cell. Having a single mode for editing and interaction removes the **segregation** of the two activities. The user can easily and at any time inspect and modify what they see.

All this happens live while the cell is active and present on the canvas. In this **interactive** environment, the effect of any modification can be immediately seen. This way, Spreadsheet-like applications can be very easily built but also way more powerful programs.

**Data safety** is always provided since every change to a cell is automatically saved and also synchronized to all devices on which the cell exists. Having its history accessible means that changes can be easily analysed and old states restored. A global, infinite undo button.

Using other cells as **dependencies** means simply executing them. Since this can be done as part of a cell's behaviour, there is not difference between internal libraries, external dependencies and applications. The uniformity of the structure allows everything to be accessed in the same way. Any version of a cell can be used by accessing its history, regardless of which version other cells might be depending on. Applications don't have to provide a specific application programming interface to be used by another program. The underlying structure of every cell can be accessed and used directly, enabling arbitrary combinations of capabilities.

Since all cells use a uniform, generic structure that any data type can be mapped to, they never need to be **serialized** manually for communication with external services, nor for storage since they are automatically persisted.

Because there is no serialization, there is no **syntax**. Instructions of a cell's behaviour are stored in a structured way instead of plain text. Although a higher-level language is necessary to describe behaviours efficiently, any syntax can be used to do so since every syntax can be translated to executing behaviours of composed and abstracted cells. It is even possible to translate between different high-level languages.

Cells are always alive, so they can be directly queried to **discover** their capabilities. The platform can also be used to search cells with a certain capability for example with keywords or by providing an exemplary input and output. And if the cell's behaviour isn't exactly as needed, it can easily be adjusted.

Since every cell is accessible to every user, **sharing** a piece of software is done by simply sending its path to the other user. Cells render themselves, so the receiver is guaranteed that they're displayed to them in exactly the same way as to the creator. All changes are synchronized so both users can edit the cell collaboratively in real-time. The network load can be decreased by automatically replicating the cell on both devices.

This way no third party is needed to create and share content. **Autonomy** is further increased by using asymmetric cryptographic keys as identification for users. This allows many operations to be done without a central authority. By using digital signatures, data can stay where it belongs - with its owner. This enables a truly open and democratic internet without the artificial switching costs caused by closed data.

Cryptography also enables a high level of **security**. By default, a cell is only accessible to its owner, who has to digitally sign an explicit permission for anyone else to access it. Permissions can be very fine-grained, specifying the kind of access, its scope and expiration. Permissions are only asked for when needed so that the user can understand the reasons behind granting it, and the immediate effects of refusing it. All communication through untrusted channels is encrypted and a user can limit the devices that his cells are replicated to, to avoid them ending up somewhere in the clouds. Digital signatures make impersonations impossible and give each user a virtual identity with its own, valuable and verifiable reputation. And if we're lucky, this could make the internet a much friendlier place.


## What's next?

The described software platform eliminates all incidental complications found in current platforms. The result is a new, a better web. A more open, more democratic, more flexible, more empowering and more secure platform to communicate through and with computers. A platform that allows everyone to participate and contribute freely and safely. A platform that makes writing software easy and fun - and accessible to everyone. A platform that enables software literacy. This is the goal of [zells](http://zells.org).
