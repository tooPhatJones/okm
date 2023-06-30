# okm
stands for the Open knowledge map
Could also be known as the open utility map, but knowledge map is more immediately descriptive to more people.
Essentially a package manager for tutorials, entirely distributed through github or other git clients. 
Eventually to include a generalized google maps style visualizer for navigating the map of tutorials.

# ephiphyte
"Epiphyte" someimtes called an "air tree" is a botany word used to mean a plant that grows on a plant. 
A phorophyte is the name for the plant the epiphyte grows on. 
Used here, an epiphyte is a relative recommended entry point into the tree of all knowledge, that does not start at the root.  
Or in other words, a contextless entry point into one of the branches of the tree of knowledge. A sub tree that grows from an existing tree without contiguous connection. 
For example, learning to drive a car. 
In a traditional tutorial, you would learn math and chemistry, engineering, and automotive science and then finally after knowing how a car works, learn to drive a car.
Learning to drive as an epiphyte would start with learning to drive and the rest could follow if desired. 

When to use an epiphyte? If building from the root of knowledge to the desired knowledge takes net more effort than starting without context in the middle of the tree of knowledge... then an epiphyte approach is the natural choice, since it would take less effor to reach your goal. 

Epiphytes have no prerequisites, instead they teach the prerequisites as they go.
Most tutorials are epiphytes, since most skills do not need explicit understanding of technical foundation in order to be learned.
Most epiphytes are built on other epiphytes. 

Its worth noting that any place in the graph could technically be used as an entry point with enough explanation. 
Here epithyte is intended to mean, a NATURAL starting point for learning a topic. 
For example you could technically start an overview of math with the first node of a calculus tutorial, and then jump back to arithmetic and then algebra and finally finish your tutorial of calculus. But since calculus requires heavy context of arithmatic and algebra to be understood, it would make more sense to start with arithmetic, then algebra, then calculus. 
Calculus is not a good candidate for an epithyte. 
However web development is a good candidate. Because while web development is built on a very long history of math, chemistry, electrical engineering, and software engineering. 
You don't really need to know any of that foundation in order to learn html, css, and JavaScript. Web dev is a good candidate for learning something without needing to cover all foundation first. 
note: Im not convinced the word epiphyte is necessary, maybe simply calling these 'entry points' would be better. Sounds cool tho.

# Trad tutorial
A tutorial that starts at the root/roots of knowledge and grows up. 
A traditional tutorial has no prerequisites because it starts all the way at the bottom.
A traditional tutorial should be used only if the difficulty in introducing a concept is higher starting with an epithet.
Traditional necessarily are less common because most skills can be taught with less effort as epithets. 
Outlining the bounds of a traditional tutorial even when it should not be used is a powerful tool for communicating a skills location in the graph of knowledge.


# Make as few assumptions about your audience as possible, 
Use the simplest language possible at all times.
define all reasonably new language as you use it 
Disambiguation, ie if any words or phrasing can be used in any other context, stop and specify the context you mean.

# Compound concepts
In learning, a compound concept is any concpet that is made of 2 or more other concepts. 
the constituent concepts can be complete, in the sense they are individually useful, or incomplete in the sense they dont make sense at all until assembled with other concepts. 
a compound concept can also be made of other compound concepts, which can be made of compound concepts and so forth. 
The concepts could be as small, or as large as you like. 
any tutorial that combines multiple tutorials is inherently a compound concept
Compound concepts are important not only to reduce confusion on behalf of the learner, but also they are the "branches" in the tree of knowledge. Wherever two or more learning paths intersect describes a branch in the tree of knowledge. 
* examples. 
a mouse trap. is a board, with a spring, a lever, a plate, and a piece of cheese. 
web development. Is the combination of html, css, and javascript


  
# Tutorial planning 
first check the graph to see if you can piggy back on anyone elses work.
Make list of all new nodes
Mark out compound concepts
start to create content keeping in mind good practice guidelines: illustrative source matter presentation, unix, low coupling high cohesion


# Illustrative design: 
Simply put, don't explain where you can illustrate. However usually for any broad context switch, an explanation will be necessary to bridge the gap between contexts.
Explanations can be built into the material. Or if they are needed to transition context for the sake of a specific tutorial, then they can be separate nodes in the graph.
The rule is to use explanation as sparingly as possible and allow your illustrations to do the majority of communication.
Illustrate with illustrations that demonstrate with source matter representation
# Source matter presentation
This means that your tutorial should be created in the medium you are trying to teach as much as possible.
If teaching js, don't make a website with snippets of js, or use a codepen, or a video. 
Put your tutorial direly in the environment the learner will be using. 
Put it in a JavaScript file, in an executable environment. 
They should be able to learn without the environment through illustration, but if they are in the environment, they should be able to demonstrate easier with dramatically less need to translate mediums. 
Every illustration should have the potential to be executed or immediately immitated by the learner as much as possible, but the user should not need to execute unless they want to for their own purposes. 
example, css tutorial in a css file https://learnxinyminutes.com/docs/css/


# Low coupling high cohesion and Unix philosophy
the following terms are used to describe best practices for creating modules (swappable pieces of something) 
Low coupling means don't create unnecessary dependencies for your modules.
High cohesion means group modules together that go together
Unix philosophy states that your modules should do one thing and do it well. 

These three design practices foster creations that are easier to update, add onto, and refactor when necessary.

Make your illustrations demonstrations that can be individually executed separately before being combined. 





# The pub system 
overview of git goes here...
Basically, the tutorials will be published after the fashion of a package manager to a centralized public index. 
the index should be simple. Only checking to make sure the published content is following the prescribed rules... ie, pointing to resources that exist. Having correct metadata fields. 
if resources pointed to don't exist, then there should be an error message
whenever a new version of a tutorial is ready, it can be re published and the version number incremented

# overview of git
link to git tutorial here later. But for now brief explanation
Git is many things at once. 
Its the ability to collaborate between very very large numbers of people at once on the same project in a way that does not require a constant connection to the internet. 
It preserves a history of changes, and allows collaborators to 'try' different versions of a project without needing to make lots of expensive copies
It has the ability to share changes with collaborators built in
and finally it comes with security and verifiability in mind, so that any change can be identified via hash. 
For these reasons git is the tool we recommend to develop and collaborate and share tutorials. 


# tree.json metadata rules, 
The tree.json file should contain an:
an object called definitions, that defines the names of the nodes, and the urls where they are located as strings. 
if these nodes are parts or pieces of other tutorials then they should be descriptively named, and have an array specifying staring and ending indexes of the tutorial they are taken from, as well as the url of that tutorial
Array called tree, holding the names of the definitions object in the order of intended traversal, complete with compound concepts outlined in sub arrays.
Finally metadata like the version number of publishing
Any lists of white or black or trusted lists as well as any other filtering metadata the authors would like to include for the graph visualizer. 
# how to reference other tutorials to specific depth
Your tutorial that references other tutorials will be an array, and any time you need to reference another tutorial, you can make a sub array with starting an ending points of another tutorial, or even parts of a node of another tutorial



# the reputation system and best practices for use
Anyone can publish their opinion about another project or set of projects with metadata in their tree.json
tentative fields are white list, blacklist, and trusted blacklist. 
whitelist: a list of projects the current project owners think are good/trustworthy. can also be used to over rule or create exceptions for any individual projects you disagree with your trusted blacklister about. 
blacklist: a list of projects the current project owners think are not good/trustworthy. 
trusted blacklist: a list of projects the current project owners implicitly trust to blacklist other projects. 

I think we can also allow any metadata to be trusted and therefore amalgamated by anyone who wants to trust anyone else's data
However we can also gather and show git metadata, activity pull requests, how fast they are responded too, how often they are merged or not. The general activity around a project to give users a confidence rating that the project is not abandoned and that its being maintained and cared for.




# Nodes being defined by line numbers unless they are in binaries
Git lets you reference not only branches, but also commits, files, line numbers, and ranges or lines numbers in files in a single url.
The nodes of the tutorial for non binary files will be ranges of line numbers in files. 
If binary files, see creating tutorials in binaries. 
# Creating tutorials in binaries, video, blender files ect..
Using git with binaries wont be possible at first, so any tutorials created in binary files ie, pdf, blender file, video ect....
We can simply write out the topics by order, and either make files no larger than their relative entry points. 


# how to coordinate edits to collaborative graph projects
discourse graphs protocol
this potentially could be used across repositories. 

# tentative requirements/additions
1. Perhaps a sorting field in the visualizer for white list, used to filter for communities that are invite only.
2. Not having a trusted white list, because it can expedite group think. To be clear a trusted blacklist is a form of group think, but it has more utility because its disproportionately useful to the learner to be able to not waste time with low quality content. 

# common objections
Q. What prevents unnecessary forking of projects and therefore more and not less noise to filter out. 
A. The reputation system can accomplish this on a resource level if content creators wish to be accepted by each other. If not then the only recourse will be community reputation. 

Q. What about 'siloed communities' where different communities create their own versions of the same Resources?
A. This method is not intended to be a solution for this problem, only a more efficient way of using existing tools to communicate. However this problem could be addressed down the road with better tools/technique potentially. The best way to avoid this problem is by starting with and maintaining high standards for the content created. 

Q. Is there any way for creators to earn reputation or monetize their content?
A. Of course! There are myriad ways to accomplish both of these goals. More to come later. 

# how this system is not better than llms for learning, does helps with human coordination in ways llms cannot currently
rn. llms are great, but they dont give the learning any sense of concreteness in the same way a fixed resource like a curriculum does. 
That sense of concreteness can be a vital part of the learning and review process, since the ease of review directly afffects the way a learner approaches learning. 
if you cant review the same resource in future you might focus far more on the concepts and not memorization. If you can review the same resource you might spend far more effort actually trying to internalize the information. 
This does not even speak to the need for adequate cheat sheet resources that help someone quickly review the salient points after learning something in the first place which llms may or may not be able to produce at a moments notice. 
The need for curated resources is still there.

# The inefficiency in trad school   
1. They ask you to decide what you want to do in ignorance, and then there are massive penalties for changing your mind at any point for obvious financial reasons. Knowledge graph solves this. They don't use bfs learning technique, which i am lumping in with this point because its a different way of saying the same thing.
2. Cant b too efficient cause they loose profits, and cant be too inefficient or competitors will take their profits, they have to walk that line of barely usable, almost non functional. By padding the curriculum as much as they can without seeming greedy, but also by enforcing as few quality standards as possible without seeming incompetent. 
3. Centralized, distributed, obfuscated. vs decentalized monolithic, transparent. curriculum is centralized and obfuscated through constant unnecessary change and meaningless iteration instead of distributed and transparent with only necessary changes, another massive massive money making inefficiency.

# the basic plane of communication is "how"
given common objectives the best way to coordinate
this is because why is a question of the different ways how you can do something. 

Or you could say, if "why" is the common object. 
Then still how is still the common ground to communicate how to do that. 
If you have a map of how then you can communicate everything else using that map as the common denominator.
In my mind this is the primary reason this is useful. 
If we have a map of "how" we can use it as common ground to communicate about what next and coordinate as humans toward common goals. 


# This potentially could be used as a way to train llms in a way that can help with logical reasoning

# tutorial + cheatsheet sans reference
The best learning resource is a tutorial, and has a cheatsheet. 
A "reference" or "documentation" that is separate from the tutorial is extremely common, but its not actually required and often is simply a sign of bad tutorial design. 
If your tutorial is designed well you should not need "documentation" because everything should be explained in your tutorial. 
That Isn't to say that you cant outline parts of your tutorial for different needs, or different skill levels. 
But splitting your learning resource into a tutorial, and a reference is mostly just a time honored obfuscation and waste of time. 
However, what you do want is a tutorial, and a cheat sheet. 
There is no reason the cheat sheet cant be used extensively in the tutorial, but a cheat sheet is an essential part of any good learning resource. 







