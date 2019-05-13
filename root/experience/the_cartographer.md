# Creation of The Cartographer
From time to time i stumble upon a very well written post about an interesting topic and then i think: i also know something, why not share it with others? Maybe the 'well-written' part will be well-lacking but why not. Also i like to learn more about programming and try out new features and languages.
So one day i became bored enough to start this little side project which might end up in the ether like it happens so often when i start such a project.
Nevertheless i might gain some experience with Go - which i will use in this project quite a lot - and how to write thoughts down for a wider audience than one.
The main idea was to create a very minimalistic web service on which i can put my documents and present them like in a blog or just as a document / html page  in itself.
Surely there are plenty of other web services for this job but it's fun to create your own. It also helps me grasp new concepts much quicker and getting your fingers dirty with a new language is best done with a 'real-life project'.

So here i am.

Now let me guide you through the inner workings of The Cartographer (which is honestly very simple).

## Source Code
You can find the complete source code of the The Cartographer on github.com.
The project consists of two repository, from which one is the back end and the other is the web content for it:

+ [back end](https://github.com/ngrande/cartographer)
+ [web content](https://github.com/ngrande/cartographer-web)

## Concept
Serve every document from a specified root directory as web pages.
Keep it simple but also let us have some flexibility.

At the beginning mainly concentrate on HTML and markdown documents, the former is just what you have to do for a web server and the letter is nice to have.
For the purpose of flexibility a way to have a template for our html files would be a nice start, so we do not need to copy & paste our html layout.

So we have the requirements:

+ Read a directory hierarchy
+ Serve every file within these directories
+ Support native HTML
+ Support markdown
+ templates

## Implementation

### Read everything into memory


### Conversion
First we have to do a markdown to html conversion.
So i remembered a nice tool for this job: [pandoc](https://pandoc.org/) (side note: this tool is mainly written in an even more interesting language: Haskell - if you want to learn something real new and not just hop form C-like language to another C-like language with different kinds of OOP features: try this functional programming language; it's like starting from zero again...).

So i figured i could use this handy tool to do the conversion for me.

A simple call to the system shall do the trick:

    
    import "os/exec"
    
    ...
    
    // assuming you run this on a unix system
    cmd := exec.Command("sh", "-c", "/usr/bin/pandoc -f markdown -t html5 -s path_to_file")
    res, err := cmd.Output() // res stores our HTML now
    

### Templates


