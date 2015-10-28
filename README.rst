Superquine
==========

Everybody loves `quines <https://en.wikipedia.org/wiki/Quine_(computing)>`_,
because it seems so counterintuitive that a program could print its own source
code.

Tell me, how often do you have this problem: You've just run a quine, and it
printed its code to your screen, but you have to redirect the input and compile
it again, and it's just such a hassle.

Never? Too bad.

Those days are now a thing of the past.
This quine not only writes its code to a new file, but also compiles and invokes
it as well!

But that's not all.

Superquine writes a copy of its own code, compiles it, and recursively does it
again, but what does it really use all this complexity for?

All of this builds up to solve one of the oldest and best known problems in math
and computing: counting to 99.

So, there you have it.
One of the more convoluted ways to write a program to count to 99 in C.

Requirements
------------

You must have the ``gcc`` compiler in your ``PATH``, or superquine will be
unable to compile itself.
Also, if you want to use the ``Makefile``, you must have some sort of make
utility as well.

Superquine was written and tested on Linux.
There are no guarantees are made that it will run on other platforms, even if
``gcc`` is installed.

Running
-------

To run Superquine, first compile it with either::

    gcc -o 0 0.c

or by running::

    make

Keep in mind, however, that the program must be called ``0`` after being
compiled (no extensions, for example), since it uses its own name when invoked
to count.

Now, you're ready to run Superquine::

    ./0

You'll see it print the numbers from 0 to 99, although it may take some time due
to all the recursion and compiling.

If you want to play around, try changing some of the code, particularly the
number in the ``if`` statement (you'll have to change it in two places: once in
a string and once in the actual code).

To clean up all of the generated copies of the quine, just run::

    make clean

Notes
-----

I'm sure there is a much shorter way to write a quine like this in C.
However, this was my first quine, so I don't have too much experience doing
this.

Also check out `David Madore's page on quines
<http://www.madore.org/~david/computers/quine.html>`_, which I found incredibly
helpful when coding Superquine.
