# Comparing *zells*

The goal of *zells* is to enable Software Literacy by providing a software platform without the incidental complications found in current platforms. The [manifesto] describes these complications in details, although in a rather abstract manner. The purpose of this document is to look at a selection of current platforms more closely and how certain complications materialize in them.

Restricted by my own knowledge, the list of platforms is all but complete and not every complication is discussed for every platform. If you find something missing, wrong or imprecise, please [help improving][edit] this document. Any form of contribution or feedback will be appreciated.

For an up-to-date list and descriptions of identified complications and how they are avoided in *zells*, please refer to the [manifesto].

[manifesto]: https://github.com/zells/core/blob/master/manifesto.md
[edit]: https://github.com/zells/core/edit/master/comparison.md


## Platforms

This list contains a variety of software products and protocols which I all consider to be *platforms*, since they allow users to create, run and share their own software.

The categories are *protocols* for platforms that are defined by standards rather than an implementation, *operating systems* for everything which is located directly between user and hardware, *virtual machines* for things that could be called programming languages and everything else is considered an *application*. 

The lines between these categories are fluent since it could be argued that some virtual machines behave like operating systems or have well defined protocols and some applications behave like virtual machines.


## Protocols

While for many of the discussed platforms protocol-like specification are available, the WorldWideWeb is unique in it's wide-spreadedness and multitude of implementations. *zells* aims to belong to this category.

### WorldWideWeb

For the purpose of this comparison, the WorldWideWeb is considered to consist of the specifications of HTTP, HTML and CSS and to a certain extend JavaScript. These are implemented by servers such as Apache and browsers such as Firefox.

**Syntax**: The web server can be implemented using any language as long as it adheres to the HTTP specification. Code for structure (HTML) and presentation (CSS) is interpreted by the browser and therefore is very limited in terms of syntax and extensibility and in practise only JavaScript can be used to encode behaviour. For that reason a number of compilers and pre-processors is available which further complicates the development process.

**Interactivity**: Server-side the level of interactivity depends on the chosen language but it's generally low due to the limited interface of the web browser. To my knowledge, Seaside offers the most interactive experience. Client-side interactivity depends mostly on the browser and is continuously improving but still very low.

**Segregation**: The level of segregation between writing and using web software depends very much on the type of software. Very simple systems can almost entirely be written in the browser - although it's not originally designed to serve this purpose. 

**Set-Up**: Sophisticated systems require a complex set-up, a dozen specialized tools and a complicated building and deployment process.

**Sharing**: The omnipresence of web clients make sharing a web application very simple once an adequate web server is set-up. This is very easy for simple applications and extremely complicated for complex applications. Since most code is executed on the server side, complexity rises with the number of users.

**Dependencies**: There are two kinds of dependencies of web applications: libraries and web-services. The management of the former is all but trivial as the large number of package managers illustrates. The complication of the latter depends on the service, but are usually subject to authentication and usage limitations.

**Serialization**: Again depends on the server technology used. Most require a data serialization for persistence and HTTP forces all input and output to always be serialized including communication with web services. With good tools, most of this can be automated but usually not all.

**Autonomy**: While envisioned as a distributed system that allows its users to collaborate and share their own software easily, the client-server model favours a high degree of centralization because of the high cost of running a server. For this reason, most web users do not create their own applications and even static content is distributed using centralized services like provided by Facebook, Twitter or Google.

**Security**: Web browsers restrict web application from accessing most of the hosting system which increases security but also limits their capabilities. Yet web applications are prone to many attacks such as session hijacking, cross-site scripting, phishing and many more.

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
