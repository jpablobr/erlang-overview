!SLIDE center

## Who?

![Joe Armstrong](Joe-Armstrong.jpg)

### Joe Armstrong

!SLIDE center

# Erlang? #

### Short for "Ericsson Language" or named after the Danish mathematician Agner Krarup Erlang? 

![Erlang Man](erlang-man.png)

["We have never revealed which of these is true, so you'll have to keep guessing!"](http://www.cio.com.au/article/307418/a-z_programming_languages_erlang/)

!SLIDE center bullets incremental 

#  How does it work?

![How do they work?](fat-guy.png)

!SLIDE bullets incremental

## (Hint: no magic!)

* Functional
* Dynamically typed
* Concurrent (actor model)
* Distributed


!SLIDE bullets incremental

* ! objects
* processes !

!SLIDE bullets incremental

# Actor model 

* No shared state
* Lightweight processes
* Asynchronous message-passing
* Mailboxes to buffer incoming messages
* Mailbox processing with pattern matching

!SLIDE bullets

# Get Erlang

* OS X: `brew install erlang`
* Linux: `apt-get install erlang`
* Windows: Who cares?!

!SLIDE bullets

# Get Erlang

* OS X: `brew install erlang`
* Linux: `apt-get install erlang`
* Windows: Who cares?! <br /> <span class="smaller">(Actually, go to erlang.org/download.html)</span>

!SLIDE center 

![Hello World](crazy-baby-killer.jpg)

!SLIDE code transition=uncover

## hello.erl

	@@@ Ruby
	-module(hello).
	-export([hello_world/0]).

	hello_world() ->
		io:fwrite("hello, world\\n").

!SLIDE commandline incremental

	$ erl
	Eshell V4.9.1  (abort with ^G)

	1>

!SLIDE commandline

	$ erl
	Eshell V4.9.1  (abort with ^G)

	1> c(hello).
	{ok,hello}

!SLIDE commandline

	$ erl
	Eshell V4.9.1  (abort with ^G)

	1> c(hello).
	{ok,hello}

	2> hello:hello_world().

!SLIDE commandline

	$ erl
	Eshell V4.9.1  (abort with ^G)

	1> c(hello).
	{ok,hello}

	2> hello:hello_world().
	hello, world
	ok
