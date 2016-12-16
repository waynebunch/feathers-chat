** For those asking, these are needed to do this:  NodeJS and npm (included with node)

I'm new to Git as well so bear with me...**

Windows: https://nodejs.org/en/

Linux: Available for all package managers I would imagine. Archlinux has it available in official repo.

#FeathersJS Test Application Breakdown

Next I'm going to learn more ES6, Express, Node, and FeathersJS by breaking down a test app availale at:

https://docs.feathersjs.com/getting-started/readme.html

This looks like a pretty promising framework that I'm sure I'll be using.

What it is:

	1.  Built on top of Express
	2.  Services oriented.  These services are easy to create (takes 10 seconds and is automatic) and provide full CRUD on a resource. 
	    Resource can be located literally anywhwere.
	3.  Hooks!  This is what really piqued my interest.  Allows before and after methods to be performed on services.
		https://docs.feathersjs.com/hooks/readme.html
	3.  Pick and choose what you want to install.  Feathers can be added to an Express program after it's already created!
	4.  Uses socket.io for "real-time" communications
	5.  Supported by a TON of db's

			AsyncStorage - feathers-localstorage
			localStorage - feathers-localstorage
			Memory - feathers-memory
			MongoDB
			NeDB - feathers-nedb
			RethinkDB - feathers-rethinkdb
			PostgreSQL, MySQL, MariaDB, and SQLite
			Oracle - feathers-knex
			Microsoft SQL Server - feathers-sequelize
			Redis
			Riak
			Neo4j
			OrientDB
			ArangoDB
			Apache Cassandra
			GraphQL
			LevelDB
			Amazon DynamoDB
			Windows Azure Table Storage
			Redis
			Riak
			Google Sheets

	6.  Full authentication and authorization built in (JWT Web Joken)

Really, check it out as I didn't even scratch the surface.

I'll be adding breakdowns of each file as I see them (breakdown folder), as I try to understand what the hell is going on.

I task you to make me look good.

Thanks!

-emp[ ]y

 
