==================================================================
ARK
==================================================================

    The details are not the details. They make the design.
    - Charles Eames

ARK is a Content Management System that has been designed with a bias towards symmetry, semantics and scalability. It's unique design introduces a powerful set of concepts and capabilities that streamlines communication and workflow between developers, designers and content managers.

.. _TOP:
.. contents:: Table of Contents
   :depth: 2

Terminology
-----------

Architecture
************
ARK is broken up into three applications.

ARK.Tektonik
   A RESTful api service providing all the create, read, update and delete methods for each of the resources used in your ARK websites.
ARK.Tekt
   A WYSIWYG website building tool used to create ARK websites.
ARK.Tekture
   A hosting platform for your ARK sites. 

Types
*****
ARK organizes content into a hierarchical set of types.  There are five different types:

Property
   A domain name. Example: *website.com*. 

Path
   A "slug" or "endpoint". Example: */contact*. Together with a ``Property`` they form a web address. Example: *website.com/contact*. 

Page
   A ``Page`` is a configuration, orientation and layout of ``Parts``. 

Part
  A ``Part`` is a configuration, orientation and layout of ``Pieces``. 

Piece
  A ``Piece`` is a piece of content such as text, images, documents, etc. 


How It Works
------------
Like the keys on a piano, ARK's types have been designed to enable developers and designers to create compositions that are artistically and technically harmonious. The beauty is that you don't need another piano just to create a new composition.

At the top of the ``Type`` hierarchy you have *Properties*. A ``Property`` is the name of the website you'd like to host. You can host multiple properties. For example you can host *website.com* and *my.othersite.com*. 

Once you've defined your properties, you can start creating ``Paths``. ``Paths`` provide a routing mechanism unique to ARK. Each ``Path`` is configured to point to a ``Page``. Although ``Paths`` can only serve a single ``Page`` at any one time, they can be configured to point to a set of pages based on effective dates and times, round robin or even at random. This allows for scheduling out updates, running A/B tests and maintaining a well organized site map.

``Pages`` in ARK serve as a configuration of ``Parts``. Different "versions" of a ``Page`` is nothing more than a different configuration of ``Parts``. Pages can be copied, organized, even shared across ``Properties``. They are your compositions. 

``Parts`` then become central to ARK's content management solution. Menus, galleries, maps, sliders, forms, etc are all implemented as prebuilt ``Parts``. Sometimes called "widgets" ``Parts`` have their own unique logic, assets, configurations and requirements. Some ``Parts`` however require assets that are complex, such as an images and video, or even another ``Part``. These reusable assets are called ``Pieces``. 

Now that you understand the basics of our our different types work together here's another way to look out their relationships. ``Properties`` are just website names that have different ``Paths`` that point to ``Pages`` which are just stored configurations of ``Parts`` which are comprised of various ``Pieces``. 


**Illustration**

The following diagram illustrates the relationship between these various types:

.. image:: ARK.png
   :scale: 75 %
   :alt: ARK.Types
   :align: right


A Real Life Example
-------------------
The following example aims to provide a short story about how ARK's design facilitates workflow, instills separation of concerns and allows for quick and effective collaboration between departmental initiatives which are commonly at odds.

2legit2quit.
   Our fake company
Billy Brains
   Our intimidating and sometimes insulting Software Engineer.
Fiona Fotoshop
   Our designer who unknowingly explodes the technical scope with each new mockup
Mark Eting
   Our marketing manager who has quarterly goals he's trying to reach and who's about to kill Billy
Sally Scribe
   Our content producer who's more concerned about the information getting out there than anything else
Project Peimp
   Redesign the corporate site, increase conversions and start marketing the unknown power behind 2L2Q's services.

Mark, Fiona and Sally have just come back from a retreat with a kick butt six month plan to send numbers through the roof. They are even wondering if the project could be completed in 4-6 weeks. They round up the development staff and try to get a plan going. Immediately they are hit with reality. Development states that their six month plan is more like a two year plan. However if they are willing to make a number of concessions, parts of it can be accomplished. Yet, nobody's really happy. The Marketing staff feel as if their plan lacks any of the purity they had envisioned and the Development staff feels like accommodating these demands is a full scale abandoment of fixing problems that could potentially take down the entire company. 





