# Creation of The Cartographer
The Cartographer is a "pleasure project" of mine simply way to bring some thoughts to the world.
The main idea was to create a very simple web service on which i can put some documents and present them like a blog or simply as a document in itself.
I know there are plenty of web services like Nginx and apache which can do most of this stuff already and surely better - but where is the fun in that? I find kind of a pleasure in creating my own stuff and it helps me grasp new concepts much quicker. So i used it to tinker around with yet another programming language, which is always fun and best to do on a "real-life" project.

So here i am.

Now i will guide you though the inner workings of The Cartographer (which is honestly very simply).

## Source Code
You can find the complete source code of the The Cartographer on github.com.
The project consists of two repository, from which one is the backend and the otis simply the web content for it:

+ [backend](https://github.com/ngrande/cartographer)
+ [web content](https://github.com/ngrande/cartographer-web)

## Concept
Simply serve my documents to the end user.
I like to write notes and documentation in markdown, it's simple and can be done in any editor, so my programming should be able to serve markdown documents as a web view to the end user. But i also did not want to be limited to this functionality, so i wanted to keep it as dumb as possible and just serve whatever is lying around in a given directory. But surely a markdown document can not be displayed properly in a browser - so i had to implement a conversion for such documents.
This means: html and txt files can simply be displayed as-is and all other documents have to get a conversion.
So i remembered a nice tool for this job: [pandoc](https://pandoc.org/) (side note: this tool is mainly written in an even more interesting language: Haskell - if you want to learn something real new and not just hop form C-like language to another C-like language with different kinds of OOP features: try this functional programming language; it's like starting from zero...).

So i figured i could use this handy tool to do the conversion for me.

## Keep it simple

