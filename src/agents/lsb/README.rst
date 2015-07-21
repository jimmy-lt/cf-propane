lsb
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

   - ``lsb``

     - ``agent_lsb.cf``
     - ``promises/``
     - ``knowledge/``
     - ``files/``
     - ``templates/``


   ``agent_lsb.cf``
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

   Knowledge is information gathered about the system that may be useful
   to the agent's proper operation. A knowledge can be a variable or
   class to be used by the agent's policies or to be exposed to other
   agents.


   Files
   ^^^^^

   Static files used by the agent.


   Templates
   ^^^^^^^^^

   Template files used by the agent.


`Linux Standard Base (LSB)`_ compliance management in order to find
back common utilities between the Linux distributions. It is not the
objective to have the whole standard installed but only a subset of
it.

.. _Linux Standard Base (LSB): http://www.linuxfoundation.org/collaborate/workgroups/lsb


Bundles
-------


lsb
^^^

Install a subset of the Linux Standard Base utilities that are proven
to be of need when to get information about the running system.


Knowledge
---------


knowledge_lsb
^^^^^^^^^^^^^

Knowledge about the running system using LSB tools.


Examples
--------

.. code-block:: cf3

  bundle agent foo
  {
    methods:
      "lsb" usebundle => lsb;

    reports:
      "$(cfpropane:knowledge_lsb.release[id]) $(cfpropane:knowledge_lsb.release[codename])";
  }

