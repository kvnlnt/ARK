==================================================================
ARK
==================================================================

ARK is a pet project that I've been looking to build for over a decade. It is my attempt at building the content management system I always wanted and/or needed. A CMS that by nature is easy to understand and meets the technical, functional and design needs for all parties involved. 

.. _TOP:
.. contents:: Table of Contents
   :depth: 2

Architecture
------------
ARK is comprised of three "micro" applications. A clear separation of concerns between the content being stored, the interactive management of that content and it's presentation.

ARK.Tektonik
   A RESTful api service to the tektonik database. It is responsible for providing all create, read, update and delete methods for each of ARK's resource types (aptly named ARK.Types).
ARK.Tekt
   A WYSIWYG site building tool. It implements the ARK.Tektonik api and is the application users interact with to manage their content.
ARK.Tekture
   A Theming Engine.

Taxonomy
-------------
ARK organizes content into a simple predefined hierarchical set of types called ARK.Types. Like a tree, each type branches down to the lower types. There are five ARK.Types:

Property
   A ``Property`` is a domain name. Example: *www.website.com* or *my.website.com*. 

Path
   A ``Path`` is an "endpoint" sometimes called a slug. Example: */home* or */contact*. Paths point to pages. Paths can point to a single ``Page`` or schedule out a set of pages based on date and time. This allows content managers to automate A/B testing, content postings, workflow, etc. Think of it as a programmable router.

Page
   A ``Page`` is a configuration, orientation and layout of ``Parts``. Think of it as a web page. 

Part
  A ``Part`` is a configuration, orientation and layout of ``Pieces``. Think of it as a part of a web page.

Piece
  A ``Piece`` is the actual content in the system. This includes all the text, images, documents, etc. Think of it as a piece of a web page.

I've found that this simple taxonomy of terms provides a powerful way to reason about a website. Understanding that each type serves a particular purpose and is itself an anatomic part of the whole picture creates a natural bridge of communication between the technical implementation and the end user experiences.

**Illustration**

The following diagram illustrates the ARK.Types hierarchy:

.. image:: ARK.png
   :scale: 75 %
   :alt: ARK.Types
   :align: right

Architects
----------
ARK defines three types of users. Each user type (called an Architect) directly relates to each of the three application architecture tiers.

Developer
   Developers work with ``ARK.tektonik`` to set up and provide development support for the ARK system.

Director
   Directors use ``ARK.tekt`` (or ARK) to manage all the content in the system.

Designer
   A designer uses ``ARK.tekture`` to create themes.


