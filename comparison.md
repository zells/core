# Comparing *zells*

The goal of *zells* is to remove all incidental complications found in current software platforms. The [manifesto] describes these complications in a rather abstract manner. The purpose of this document is to look at a selection of current platforms more closely and how certain complications materialize in them.

Restricted by my own knowledge, the list of platforms is all but complete and not every complication is discussed for every platform. If you find something missing, wrong or imprecise, please [help improving][pulls] this document.

For an up-to-date list and description of identified complications and how they are avoided in *zells*, please refer to the [manifesto].

[manifesto]: https://github.com/zells/core/blob/master/manifesto.md
[pulls]: https://github.com/zells/core/pulls

## Platforms

This list contains a variety of software products and a set of protocols which I all consider to be *platforms*, since they allow users to create their own, new software.

The categories are *protocols* for platforms that are defined by standards rather than an implementation, *operating systems* for everything which is located directly between user and hardware, *virtual machines* are things that could be considered programming languages and everything else is considered an *application*. 

The lines between the categories are somewhat fluent since it could be argued that some virtual machines behave like operating systems and some applications behave like virtual machines.


## Protocols

### WorldWideWeb

For the purpose of this comparison, the WorldWideWeb consists of the specifications of HTTP, HTML and CSS and to a certain extend JavaScript. These are implemented by servers such as Apache and browsers such as Firefox. While HTML offers a straight-forward **syntax**, it is very limited and cannot be extended. And while any language can be used for server-side code, only JavaScript is practical on client side. But at least the **interactivity** when modifying client-side code is improving.

The web browser is only designed for accessing software, not manipulating then, which leads to a very high**segregation** between writing and using web application. While the latter only requires a web browser which is pre-installed on most systems and makes **sharing** applications very easy, the former requires a complicated **set-up** including web server, pre-processors, build tools, a server-side language and usually package managers to download third-party **dependencies**. 

Instead of downloading them, third-party software can also be provided as web services. Besides complicated authentication, and very low **discoverability** because little semantic information, these services require the **serialization** of every single sent and received message.

While invisioned as a distributed system that fosters **autonomy**, the WorldWideWeb turned out to favour centralization. **Security** is maintained by sandboxing web application as much as possible but web application are prone to many attacks such as session hijacking, cross-site scripting, phishing and many more.

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
