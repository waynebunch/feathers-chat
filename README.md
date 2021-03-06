#FeathersJS Chat Application Breakdown

## Breakdown of the files will be in `breakdown` directory

## I will start with the package.json file and work my way down as I see it

A MEAN (Mongo, Express, Angular, Node and JS by proxy) tutorial for novices, by a novice.  I've
spent so much time trying to figure out what my next move is to get into the dev world.  I figure
I'm at an intermediate level where I could do the job, but getting the job would be much harder.
Enter Git, where I'm going to start contributing like mad.

**The best way for me to learn is through teaching to myself, and hopefully it helps others.**

The idea:  Go through developed code that has a little bit of everything, and when I don't know 
something, figure it out and write about it.  Reverse engineer the hell out of it.

This is my attempt.

Every note on here implies I didn't know much about it, so I did a little research
on it.  These explanations are from a learning dev, so they might not even be 100% correct, it's 
just how I see it.  Hopefully it opens a discussion and the correct answers can be pushed.  This 
seems the best way for me to learn as a self-proclaimed intermediate JS developer.  I want to 
learn the MEAN (Mongo, Express, Angular, Node) stack and this has everything except Angular.  
I can do that later...

**For those asking, these are needed to do this:  NodeJS and npm (included with node)**

**I'm new to Git as well so bear with me...**

	1.  Install node
		1.  Linux: Available for all package managers I would imagine. 
		    Archlinux has it available in official repo.
		2.  Windows: https://nodejs.org/en/
	2.  Install FeathersJS  
		1.  $ npm install -g feathers-cli
	3.  Clone my repo
		1.  git clone https://github.com/waynebunch/feathers-chat.git
	4.  Go to directory and do:
		1.  npm install (it will d/l and install appropiate modules)
		2.  npm start
		3.  You should see 'Feathers application started on localhost:3030'
		    This string is in the `src/app.js` file and prints at execution 
		    of `npm start`
	5.  In your browser, goto localhost:3030 and the chat server should be running.

If this doesn't work let me know what the error is.  Either way, you still have the code and you
can follow along with that. I'm going to learn more ES6, Express, Node, and FeathersJS by breaking
down a test app  that I built, availale at:  

https://docs.feathersjs.com/getting-started/quick-start.html

This looks like a pretty promising framework that I'm sure I'll be using.

What it is:

	1.  Built on top of Express
	2.  Services oriented.  These services are easy to create (takes 10 seconds and is automatic) and provide 
	    full CRUD on a resource. Resource can be located literally anywhwere.
	3.  Hooks!  This is what really piqued my interest.  Allows before and after methods to be performed on services.
		https://docs.feathersjs.com/hooks/readme.html
	3.  Pick and choose what you want to install.  Feathers can be added to an Express program after it's
	    already created!
	4.  Uses socket.io for "real-time" communications
	5.  Supported by a TON of db's
		1. AsyncStorage - feathers-localstorage
		2. localStorage - feathers-localstorage
		3. Memory - feathers-memory
		4. MongoDB
		5. NeDB - feathers-nedb
		6. RethinkDB - feathers-rethinkdb
		7. PostgreSQL, MySQL, MariaDB, and SQLite
		8. Oracle - feathers-knex
		9. Microsoft SQL Server - feathers-sequelize
		10. Redis
		11. Riak
		12. Neo4j
		13. OrientDB
		14. ArangoDB
		15. Apache Cassandra
		16. GraphQL
		17. LevelDB
		18. Amazon DynamoDB
		19. Windows Azure Table Storage
		20. Redis
		21. Riak
		22. Google Sheets

	6.  Full authentication and authorization built in (JWT Web Joken)

Really, check it out as I didn't even scratch the surface.

I'll be adding breakdowns of each file as I see them (breakdown folder), as I try to understand what the hell is going on.

I task you to make me look good.

Thanks!

-Wayne B.

 
