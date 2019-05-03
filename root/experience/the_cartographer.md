# Creation of The Cartographer
The Cartographer is a "pleasure project" of mine simply way to bring some thoughts to the world.
The main idea was to create a very simple web service on which i can put some documents and present them like a blog or simply as a document in itself.
I know there are plenty of web services like Nginx and apache which can do most of this stuff already and surely better - but where is the fun in that? I find kind of a pleasure in creating my own stuff and it helps me grasp new concepts much quicker. So i used it to tinker around with yet another programming language, which is always fun and best to do on a "real-life" project.

So here i am.

Now let me guide you through the inner workings of The Cartographer (which is honestly very simply).

## Source Code
You can find the complete source code of the The Cartographer on github.com.
The project consists of two repository, from which one is the back end and the other is simply the web content for it:

+ [back end](https://github.com/ngrande/cartographer)
+ [web content](https://github.com/ngrande/cartographer-web)

## Concept
Simply serve every document from a directory hierarchy to the web.
Keep it as simple as possible but also let us have some flexibility.

For a website HTML is the first thing let's add some more to it:<br/>
Since i like to write notes and documentation in markdown, so we will create a process that is able to serve markdown documents to a web browser in a readable form.

Now we have the first requirements:

+ Read a directory hierarchy
+ Serve every file within these directories
+ Support native HTML
+ Support markdown

## Implementation


### Conversion
This means: html and txt files can simply be displayed as-is and all other documents have to get a conversion.
So i remembered a nice tool for this job: [pandoc](https://pandoc.org/) (side note: this tool is mainly written in an even more interesting language: Haskell - if you want to learn something real new and not just hop form C-like language to another C-like language with different kinds of OOP features: try this functional programming language; it's like starting from zero...).

So i figured i could use this handy tool to do the conversion for me.

## Keep it simple

