apt
===

.. Placeholder for the agent's documentation.

   Use this file to document the agent and its behavior under various use
   cases. This is to be included in the cf-propane's user documentation.

   Agents are how the cf-propane project organizes CFEngine policies.
   Each agent should bring a consolidated bundle of CFEngine policies to
   ensure a particular feature. For example, an agent can be about
   installing a software and providing ways to maintain its configuration.


   Agent layout
   ------------

   Agents are directory trees under the ``agents`` folder. Each agent
   should follow a simple directory structure.

   - ``apt``

     - ``agent_apt.cf``
     - ``promises/``
     - ``knowledge/``
     - ``files/``
     - ``templates/``


   ``agent_apt.cf``
   ^^^^^^^^^^^^^^^^

   Agent's definition file. Defines files to be loaded with the agent and
   do a set up job by defining variables or classes that will be used by
   the agent's policies.


   Promises
   ^^^^^^^^

   This folder contains the business logic of the agent. This is where the
   policies defined by the agent are located.


   Knowledge
   ^^^^^^^^^

   Knowledge are information gathered about the system that may be useful
   to the agent's proper operation. A fact can be a variable or class to
   be used by the agent's policies or to be exposed to other agents.


   Files
   ^^^^^

   Static files used by the agent.


   Templates
   ^^^^^^^^^

   Template files used by the agent.


Agent for Debian's Advance Package Tool, a package management system.


Bundles
-------


apt
^^^

Install and configure Debian APT's package management system.


apt_config
^^^^^^^^^^

Manage APT's configuration within the ``/etc/apt/apt.conf.d`` folder.


apt_key
^^^^^^^

Manage APT's keyring for package authentication.


apt_source
^^^^^^^^^^

Manage APT's package sources within the ``/etc/apt/sources.list.d``
folder.


Knowledge
---------


knowledge_apt
^^^^^^^^^^^^^

Common knowledge about APT, the package management system.


Examples
--------

< AGENT USAGE EXAMPLES HERE >

