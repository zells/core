# Comparing *zells*

The goal of *zells* is to remove all incidental complications found in current software platforms. The [manifesto](manifesto.md) describes these complications in a rather abstract manner. The purpose of this document is to look at a selection of platforms more closely and how certain complications materialize in them.

Restricted by my own knowledge, the list of platforms is all but complete and not every complication is discussed for every platform. Please help improving this document.


## Software Platforms

The list contains a variety of software products and a set of protocols which I all consider to be *platforms*, since they allow users to create their own, new software which is can be accessed or run through the platform.

The categories are *protocols* for platforms that are defined by standards rather than an implementation. *Operating systems* is everything which is located directly between user and hardware. Things that could be considered a programming language is categorized under *virtual machines* and everything else is considered an *application*. 

The lines between the categories are somewhat fluent since it could be argued that some virtual machines behave like operating systems and some applications behave like virtual machines.


## Avoided Complications

The complications that are analysed for each platform are described in more detail in the [manifesto](manifesto.md). Each of the following paragraphs describes how a specific complication is avoided in *zells*.

**Segregation** writing and running software happens literally in the same mode and space. The only segregation could be seen between *interactions* that aim to modify a cell and such that use the cell for its primary purpose. For example moving a non-draggable cell while lay-outing.

**Set-Up** only the browser is necessary. The software can run on any other computer. Ideally, a browser-version of the the zells browser provides a web-gateway.

**Syntax** It should be possible to use any syntax to write a program for the zells VM. Although I can't prove that. Also, translating between syntax might be possible.

**Discoverability** OK this still is tricky. Any library is browsable since it's all just cells. So looking for a specific cell can be done with the browser. All documentation and examples can be integrated into the cell since it's alive. So if I have a string and I want to know what I can do with this string, I have autocomplete, can browse the cells and try out what they do. People can create their own String cells if they want to that have more or different capabilities.

**Interactivity** This I haven't thought through completely yet. Definitely wanna achieve something similar to Smalltalk. Programming should be completely interactive. But what that means I don't know yet. Shuckles.

**Dependencies** Well there are none. You just use whatever cell exists in the universe. But there still might be different versions. But you can always just use a specific version. Although if you want to change that you may have to change every single usage. Better to keep that in one point. I think that's possible since all paths are resolved upwards. So versioning is still tricky but at least using any number of different versions in a project in no problem anymore.

**Serialization** Completely gone. Talking to external services still require it but because of the completely homogeneous structure everything can be serialized automatically. Except when you talk to stupid services. Then you still need to serialize but it's easier.

**Data Safety** concerns are also gone. Since everything, every single change is saved. Not every message that is sent to a cell but every modification of it.

**Sharing** is super easy because of the low set-up costs and because it's just protocols.

**Autonomy** might be the hardest to argue. The main thing is that authentication and identification is distributed so you don't need a central database for that anymore. Content discovery might still need central gateways but the content itself can be completely distributed as well. And the most important point is that it's easy to create and modify software so no need to wait or depend on somebody else.

**Security** is improved because of the use of cryptography instead of passwords. Cracking and theft is still possible but much harder and because of the identities, scamming is also a lot harder. The trustworthiness of zells users can be estimated by their reputation.


## Protocols

### WorldWideWeb

**Segregation** is very high since development happens in a completely different environment
**Set-Up** Is low, only a browser is needed which is pretty much already installed everywhere
**Syntax** can be any
**Discoverability** quite good for humans, not so good for machines because of little structure
**Interactivity** gets better in some browsers, still very bad though
**Dependencies** depends on the language, web services can be very tricky, mostly because of authentication
**Serialization** always and everywhere and very annoying
**Data Safety** better back-up your database
**Sharing** very easy, all you need is a URL
**Autonomy** so and so. While it's completely open, it's architecture is rather centralized so infrastructure is needed
**Security** very low, based on passwords, gets a little better with multi-factor authentication

## Operating Systems

### Linux

**Segregation** are written in an editor and run either in the terminal or with a GUI.
**Set-Up** Installation is quite easy now, can be run from a USB stick
**Syntax** Multiple languages possible, strong lock-in though, unfamiliar to most people, CLI is terrible
**Discoverability** man pages and built-in help. 
**Interactivity**
**Dependencies**
**Serialization** piping is almost nice but the pipes are so tiny
**Data Safety** don't shoot yourself in the foot
**Sharing** package managers, distributions, compile your own
**Autonomy** it's free and most things are free
**Security** good user-based security, lots of things need system-wide access though

### Windows

**Segregation** programs usually have GUIs
**Set-Up** pre-installed on most costumer PCs, easy to install
**Syntax** languages, GUIs
**Discoverability** Pretty bad since everything in menus
**Interactivity**
**Dependencies**
**Serialization**
**Data Safety** Better make those back-ups
**Sharing** Easier because of market domination
**Autonomy** Pretty bad because controlled by Microsoft
**Security** Slowly improving but still pretty terrible

### Macintosh

**Segregation** always GUIs
**Set-Up** pre-installed on Apple computers
**Syntax** Consistent GUIs
**Discoverability** Menus
**Interactivity**
**Dependencies**
**Serialization**
**Data Safety** At least time machine is built-in
**Sharing** Good among fellow mac users, gotta make sure it runs in the new version
**Autonomy** Not too bad but Apple is trying to make it worse
**Security** Linux-based

### iOS

**Segregation** Development happens on a different plattform
**Set-Up** Zero for running, by now pretty easy for creation
**Syntax** Limited languages available
**Discoverability**
**Interactivity** Terrible, simulator
**Dependencies**
**Serialization**
**Data Safety** It's all in the cloud
**Sharing** Easy through market
**Autonomy** Terrible, high fees and tightly controlled market
**Security** dunno

### Android

**Segregation** Cross-platform
**Set-Up** Pretty straight forward by now
**Syntax** Still only Java?
**Discoverability**
**Interactivity** Terrible, simluator
**Dependencies**
**Serialization**
**Data Safety** To the clouds, but harder since less integrated/mandatory than iOS
**Sharing** Easy through market
**Autonomy** Better than iOS but still pretty bad
**Security** Permission-based, better since more fine-grained


## Virtual Machines

### JVM

**Segregation**
**Set-Up** Not too bad
**Syntax** Mostly Java, some others
**Discoverability** Depends on the IDE
**Interactivity** Debugger
**Dependencies** Complicated build systems
**Serialization** The worst
**Data Safety** VCS kinda mandatory
**Sharing** Easy because very wide-spread
**Autonomy** Owned by Oracle
**Security** Dunno

### CLI

**Segregation**
**Set-Up**
**Syntax** Different languages available
**Discoverability**
**Interactivity**
**Dependencies**
**Serialization**
**Data Safety**
**Sharing**
**Autonomy** Owned by Microsoft
**Security**

### Smalltalk

**Segregation** Way less, both happens in the same environment
**Set-Up** Download and install
**Syntax** Single language
**Discoverability** Quite good with search and examples
**Interactivity** Very good with awesome debugging
**Dependencies** dunno
**Serialization** Probably not needed withing one image
**Data Safety** The image must live
**Sharing** Tricky with out-filing and VCS
**Autonomy** open-source all the things
**Security** dunno

### unison

**Segregation**
**Set-Up**
**Syntax** Only functional
**Discoverability**
**Interactivity** High because direct manipulation I think
**Dependencies**
**Serialization** Not necessary within platform
**Data Safety**
**Sharing** Should be easy because programs can be run remotely
**Autonomy** Also good because easy distribution
**Security**

### JavaScript

**Segregation** REPL
**Set-Up** Runs in the browser
**Syntax**
**Discoverability**
**Interactivity** Depends on browser
**Dependencies** so many package managers
**Serialization** JSON
**Data Safety**
**Sharing** Easy through web
**Autonomy**
**Security** Totally sand-boxed inside browser

### LiveCode

**Segregation**
**Set-Up**
**Syntax** Very intersting
**Discoverability**
**Interactivity** Higher than alternatives
**Dependencies**
**Serialization**
**Data Safety**
**Sharing**
**Autonomy**
**Security**


## Applications

### Flash

**Segregation**
**Set-Up** Used to be everywhere, now getting worse
**Syntax**
**Discoverability**
**Interactivity** Quite good
**Dependencies**
**Serialization** For getting anything in or out
**Data Safety**
**Sharing** Used to be very easy through web
**Autonomy** Owned by Adobe
**Security**

### Scratch

**Segregation** Very little
**Set-Up** None
**Syntax** Graphical
**Discoverability** Not so good I think
**Interactivity** Very good but could be better
**Dependencies** Even possible?
**Serialization** Necessary
**Data Safety** It's on the cloud
**Sharing** Very easy
**Autonomy** Complete dependency
**Security** Completely sand-boxed

### Etoys

**Segregation**
**Set-Up**
**Syntax**
**Discoverability**
**Interactivity**
**Dependencies**
**Serialization**
**Data Safety**
**Sharing**
**Autonomy**
**Security**

### Excel

**Segregation**
**Set-Up**
**Syntax**
**Discoverability**
**Interactivity**
**Dependencies**
**Serialization**
**Data Safety**
**Sharing**
**Autonomy**
**Security**

### Matlab

**Segregation**
**Set-Up**
**Syntax**
**Discoverability**
**Interactivity**
**Dependencies**
**Serialization**
**Data Safety**
**Sharing**
**Autonomy**
**Security**

### Eve

**Segregation**
**Set-Up**
**Syntax**
**Discoverability**
**Interactivity**
**Dependencies**
**Serialization**
**Data Safety**
**Sharing**
**Autonomy**
**Security**

