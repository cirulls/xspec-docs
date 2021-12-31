What is XSpec
=============

XSpec is a unit test and `behaviour-driven development`_ (BDD) framework
for XSLT, XQuery, and Schematron. It is based on the Spec framework of
`RSpec`_, which is a BDD framework for Ruby.

XSpec consists of a syntax for describing the behaviour of XSLT, XQuery,
or Schematron code, and some code that enables to test code against
those descriptions.

What is BDD?
------------

BDD is like Test Driven Development (TDD) in that it encourages to
develop code by

-  describing a behaviour (or writing a test)
-  testing whether the code gives that behaviour
-  if it doesn’t, fixing the code until it does and the test passes

The difference between BDD and TDD is about how to write the tests. In
BDD, the focus is on the **behaviour of the code**: the descriptions
form the double role of both a **human-readable documentation** of what
the code should do and runnable tests that can test whether the code
does what it should do.

In BDD, the focus in on **scenarios** and the expected behaviour of the
application with these scenarios. Scenarios fit particularly well with
XSLT’s source-driven (or template-driven) approach. For example, a
scenario might be:

   when processing a ``para`` element, it should create a ``p`` element

or something more complex like:

   | when processing a ``fn`` element with a ``label`` attribute in
     ``footnote`` mode,
   | it should create a ``p`` element with a ``sup`` child holding the
     value of the ``label`` attribute

Scenarios written like this naturally map onto XSLT templates.

.. _behaviour-driven development: https://en.wikipedia.org/wiki/Behavior-driven_development
.. _RSpec: https://rspec.info/
