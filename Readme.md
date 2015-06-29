Linkto
===

Linkto is a URL shortener. It shortens a long URL (such as https://np.reddit.com/r/IAmA/comments/2wwdep/we_are_edward_snowden_laura_poitras_and_glenn/courx1i?context=3) to a shorter, more memorable URL like http://nindalf.com/OverconfidentArowana, making it much easier to share.

####Advantages

1. Simple REST API to interact with. Creating links is as easy as `curl --data 'longurl=http://reddit.com/r/programming' http://nindalf.com/shorten` (Try it!)
2. Very configurable. Its possible to change the kind of links generated by changing the files in the words directory. You could use AdjectiveScientist instead of AdjectiveAnimal if that's your thing.
3. Easy to deploy. Once you install Docker, deploying this app will take only 3 commands

####Deploying

Edit the `.env` file with your hostname and the kind of URLs you'd like to generate.

1. Install [Docker](http://docs.docker.com/installation/ubuntulinux/) and [Docker Compose](http://docs.docker.com/compose/install/)
2. `git clone https://github.com/nindalf/linkto` - clone this repo
3. `docker-compose build` - create a Docker image out of this repo
4. `docker-compose up` - deploy linkto and redis containers and link them. Also expose linkto publicly.

####Contributing

Create pull requests or open an issue for any improvements, whether that's adding a feature in the server, improving the docker files or even adding your favourite scientist or animal to the word list. I would appreciate both :) 

I'm working on these features next

* Statistics for each link
* Creation of user accounts

####Acknowledgements

I'd like to thank Gary Burd for his excellent [redis client](github.com/garyburd/redigo/redis), Salvatore Sanfilippo for [redis](http://redis.io/) and the Go Authors for the excellent standard library.

I got the list of adjectives from [momswhothink.com](http://www.momswhothink.com/reading/adjectives-that-start-with-a-to-z-list.html) and the list of scientists from [famousscientists.org](http://www.famousscientists.org/list/), so thanks to them too.