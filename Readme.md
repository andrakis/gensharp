GenSharp
========

GenSharp is a C# implementation of various generic behaviors such as those
found in Erlang.
In this case, we use interfaces rather than behaviors, but the same actor
model and state system is used.

Currently provides:
 * Generic callbacks allow the more functional side of C# to be used
   (anonymous functions and lambdas may be used.)
 * A simple multihreaded worker system that is thread-safe.

Goals:
 * Generic server (`gen_server`) behaviour.
 * Generic finite state machine (`gen_fsm`) behaviour.


Design
======

GenSarp is built around the Callback series of classes.
By using callbacks and strictly adhering to type specifications, we can create
functions that are (almost) immutable (there is nothing stopping that function
from modifying its own data, but this is discouraged.)

Using the actor model of Erlang, callbacks can create an initial state for a
process, and when their handling functions are called will receive their state
and may optionally update that state, which will be passed in to the next
handling function.


Requirements
------------

* Visual Studio 2010 or 2012 (Express editions are fine)
* .NET 4.0

Note: the project aims to be compatible with MonoDevelop, however this
compatibility will be in a future release.


By
--
Julian "Andrakis" Thatcher <julian@noblesamurai.com>


License - MIT License
---------------------
Copyright (C) 2013 Julian Thatcher

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
