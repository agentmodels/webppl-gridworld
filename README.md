# webppl-agents
Webppl library with agents for solving MDPs and POMDPs. JS library for displaying Gridworld. 

##Insallation
```
sh install.sh
```
If `npm link` doesn't work due to permissions, you can use sudo or [follow this](http://justjs.com/posts/npm-link-developing-your-own-npm-modules-without-tears). 

Note that this links several repositories of webppl packages to your global npm package list. 

##Running from the command line 
To run purely on the command line we need to have the [webppl-dp](https://github.com/stuhlmueller/webppl-dp) package in a local repository. Then we can run with:
```
webppl --require webppl-dp --require . examples/hyperbolic/generative_examples.wppl
```

##Running in the browser

Running a webppl script in the browser allows use of `GridWorld.draw` for easier debugging of agents. To do so, do we first have to install webppl from source and link it to node. 

Then we can compile webppl and webppl-gridworld together and run your script.

```
sh compile.sh examples/hyperbolic/generative_examples.wppl
```

To just run your script without compiling (for example if there have been not changes in `/src` we can do:

```
sh run.sh myscript.webppl
```
