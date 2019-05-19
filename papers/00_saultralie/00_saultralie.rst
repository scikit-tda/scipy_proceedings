:author: Nathaniel Rivera Saul
:email: nat@riverasaul.com
:institution: Department of Mathematics, Washington State University Vancouver
:institution: New Relic
:corresponding:

:author: Christopher Tralie
:email: abc
:institution: abc

:author: HJ van Veen
:email: abc
:institution: abc
:bibliography: scikit

------------------------------------------------------------------
Scikit-TDA: Topological Data Analysis for the Python ecosystem.
------------------------------------------------------------------

.. class:: abstract

Scikit-TDA is a new suite of Python libraries that provide implementations of the major algorithms from Topological Data Analysis. With easy installation, an intuitive interface, and comprehensive documentation, Scikit-TDA allows data scientists and academic researchers alike to explore the application of Topological Data Analysis to their favorite data. 


.. class:: keywords

   Topological Data Analysis, Mapper, filtrations, homology

Introduction
------------

There is a growing need for an ecosystem of TDA libraries that is approachable to non-experts in the fields of Algebraic Topology. 
This project aims to provide a curated library for Python tools that are widely usable and easily approachable. 
Each is easy to install through traditional Python mechanisms, portable to all platforms, requires no dependencies outside of what is available on Pypi, has comprehensive documentation, is open source, provides an issue tracker and is responsive to issues and questions, and exposes an intuitive API for developers familiar with the Python scientific computing ecosystem.

Each project can stand alone, or be used as part of the scikit-tda bundle. This project curates the group of packages and houses extensive documentation and examples on how each package can be used together.

Scikit-TDA is a home for compatible TDA libraries intended for non-researchers. We provide detailed documentation and unified APIs so that using TDA can be used in the wild.

The TDA ecosystem is rapidly growing. Below is the list of current projects, either built or in development, to be included in scikit-tda.


Test ref: :cite:`kerber2017geometry`.



Background
-----------


Topological Data Analysis consists of two main tools, Persistent homology and Mapper.

Mapper history :cite:`singh2007topological`.
For a great introduction to persistent homology :cite:`ghrist2008barcodes`.



Library Design
----------------

The design of Scikit-TDA is inspired to two prominent libraries in the data science world, the TidyVerse and Scikit-Learn.  

From Scikit-Learn, we adopt the clean, uniform, and established API for all of our projects (as much as possible) :cite:`scikit-learn`. This allows developers fluent in the idioms of `sklearn` to quickly incorporate techniques from TDA into their workflow without learning many new idioms or patterns.

From the TidyVerse, we adopt the structure of one governing package with many small and specific tools, all designed to interact together.
We believe this design is the right choice because of the new nature of TDA, many new algorithms and techniques are being developed. 
By keeping entire systems self contained behind a clean interface, we allow for **hot swapping** of libraries and algorithms.  
This also produces considerably less stress on the Scikit-TDA project, as each individual library can move it its own pace with its own developers.


Packages
------------

Scikit-TDA consists of 6 different packages, each responsible for a small piece of the TDA ecosystem.


- Kepler Mapper - Mapper implementation :cite:`KeplerMapper2017`.
- Ripser.py - Super fast rips cohomology with sublevelset and cocycles (cite ripser.py)
- Cechmate - 
- Persim - Persistence Images, in batch too.
- TaDAsets - Constructors for data sets nice for demonstrating TDA benefits.


Kepler Mapper
~~~~~~~~~~~~~~~

Implementation of the Mapper algorithm :cite:`singh2007topological`.

Riper.py
~~~~~~~~~


We provide a renovated Python implementation of the Ripser package.  Because of the sheer speed of Ripser, it has created a large user base. The library as stands is only as a command line tool. Multiple efforts have been made to wrap the C++ library for use in other languages.  TDAstats\footnote{cite correctly: https://github.com/rrrlw/TDAstats} supplies an R interface, Ripser.jl\footnote{https://github.com/mtsch/Ripser.jl} provides a wrapper for Julia, wrapper, and this library provides a Python wrapper. 

As in the spirit of the rest of Scikit-TDA, we provide a a object-oriented interface designed to fit within the Scikit-Learn transformer paradigm \cite{scikit-learn} as well as expose a lightweight functional interface.

Cechmate
~~~~~~~~~~

Persim
~~~~~~~~~

Currently implements the Persistence Images :cite:`adams2017persistence`.

And now all the distances that we have


TaDAsets
~~~~~~~~~

TaDAsets is a small library designed to provide constructors for data sets particularly interesting to a topologist. These data sets have known homologies, but varying magnitudes or noise, orientation, and size. 
This package can be thought of as an extension of scikit-learn's `datasets` module.



Conclusion
------------


Scikit-TDA is a library of special purpose tools, all designed and currated to fit together and be natural for Python developers and researchers. This library would be suitable for students learning the fundamentals of Topological Data Analysis, as well as researchers exploring the applicability of these methods for their own research.

These tools are not necessarily intended for researchers of Applied Topology or Topological Data Analysis to use. For specialists in the field, more customized and flexible tools might be more usable. Rather than building blocks for TDA algorithms, such as the PHAT library supplies, we provide complete and usable solutions that work out of the box with little need for expertise in the field or in expertise in software development.

