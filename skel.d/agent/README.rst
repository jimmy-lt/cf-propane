{{ agent.name }}
{% for _ in agent.name %}={% endfor %}

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

   - ``{{ agent.name }}``

     - ``agent_{{ agent.name }}.cf``
     - ``promises/``
     - ``knowledge/``
     - ``files/``
     - ``templates/``


   ``agent_{{ agent.name }}.cf``
   ^^^^^^^^{% for _ in agent.name %}^{% endfor %}^^^^^

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


< AGENT DESCRIPTION HERE >


Bundles
-------

< BUNDLES DESCRIPTION HERE >
{% if agent.has_knowledge %}


Knowledge
---------

< KNOWLEDGE DESCRIPTION HERE >
{% endif %}


Examples
--------

< AGENT USAGE EXAMPLES HERE >
