.. image:: https://readthedocs.org/projects/cf-propane/badge/?version=latest
  :target: https://readthedocs.org/projects/cf-propane/?badge=latest
  :alt: Documentation Status

cf-propane
==========

*cf-propane* is a collection of generic `CFEngine 3`_ master policies
to drive the management of your IT infrastructure.

CFEngine is a configuration management and automation framework that
lets you securely manage your IT infrastructure. If you don't know yet
about CFEngine, you can take a look at its `documentation
<https://docs.cfengine.com/latest/guide-introduction.html>`_ to get a
first grasp of it.

The goal of *cf-propane* is to provide an easy and ready to use
framework for administrators to securely build and manage their IT
infrastructure.


.. _CFEngine 3: https://cfengine.com/


Development
-----------

*cf-propane* make use of various Python 3 utilities to drive its
development. If you wish to bring some changes to the project and
build it, you'll need to set up your working environment first.

In bellow instructions, each command states the level of privileges
they should be run with the command prompt. The prompt can be one of the
following:

- ``$`` for normal user privileges. Just run the command as is.
- ``#`` for administrative privileges, either run as ``root`` or other
  administrative user or by prefixing the command with ``sudo``.

Make sure to have Python 3 installed in version *3.5* or later. If you
are running Fedora or one of its `derivatives <Fedora derivatives_>`_,
you can run the following command:

  .. code-block:: console

    # yum install python3

On the other hand if you are using Debian or one of its
`derivatives <Debian derivatives_>`_, run the following command:

  .. code-block:: console

    # apt-get install python3

For any other system, you can find installation instructions on the
Python's project `website <Python_>`_.


.. _Debian derivatives: https://www.debian.org/derivatives/
.. _Fedora derivatives: https://distrowatch.com/search.php?basedon=Fedora
.. _Python: https://www.python.org/


Virtual environment
^^^^^^^^^^^^^^^^^^^

In order to keep your system clear from the development tools needed
for the project, it is advised to set up a Python 3 virtual
environment using `pipenv <https://pipenv.readthedocs.io/>`_.

Go to the project's directory and run the following command:

  .. code-block:: console

    $ pipenv --three

To activate the environment, you can enter the following command:

  .. code-block:: console

    $ pipenv shell
    (pipenv)$

When a command should be entered within the virtual environment, we
use the following ``(pipenv)$``  prompt in console examples. Such
command can also be prefixed with ``pipenv run`` when not in an
activated environment.


Installation requirements
^^^^^^^^^^^^^^^^^^^^^^^^^

All the utilities required to build or ease project's development are
listed in the ``Pipfile`` file. To install the project's dependencies
run the command bellow:

  .. code-block:: console

    $ pipenv install -d

This file will be updated each time a new dependency is added. Be sure
to re-run this command each time you notice a change to the ``Pipfile``
file.


Invoke tasks
^^^^^^^^^^^^

Building the project involves many different tasks. To ease the
operation, needed actions grouped together in the ``tasks.py`` file and
ran using the `Invoke`_ tool as simple shell commands.


.. _Invoke: http://www.pyinvoke.org/


Licensing
---------

This software project is provided under the licensing terms of the
MIT License stated in the file ``LICENSE.rst``.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
