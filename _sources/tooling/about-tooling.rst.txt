About the AADL tooling
======================

AI coding agents are getting good at writing and changing text-based
models, and AADL models are no exception. But an agent that edits a
model needs to know whether its changes are correct, and it needs to
run analyses to see what the changes mean for the system. In OSATE,
these steps happen in a graphical desktop application that is built for
people, not for agents.

The AADL tooling closes this gap. It takes the AADL support at the core
of OSATE and makes it available in Visual Studio Code and on the command
line, where AI agents already do their work. People can use it too, of
course, for example to edit AADL in Visual Studio Code or to check
models automatically whenever they change.

The project is open source and hosted at
https://github.com/osate/aadl-tooling.

Visual Studio Code extension
----------------------------

The AADL2 extension turns Visual Studio Code into an AADL editor. It
marks errors as you type, suggests completions, jumps to definitions,
and shows an outline of the model. An agent working in the editor sees
the same error reports and can use the same commands to instantiate a
model and run analyses on it.

The extension runs on Windows, macOS, and Linux.

Command line tool
-----------------

osate-cli offers the same checks and analyses as commands for a
terminal or a script. Many AI agents work by running commands, and
osate-cli lets them treat an AADL model like any other project they
build and test. The tool keeps models loaded between commands, so
checking a large model again after a small change is quick. It can also
set up and manage workspaces with several projects that depend on each
other.

osate-cli runs on macOS and Linux.

What is included
----------------

Both tools check models against the syntax and the rules of the AADL
standard, including models that use the Error Model Annex or the
Behavior Annex. They can
create instance models and run analyses on them, including flow
latency, bus load, and mode reachability.

Behind both tools is the same AADL implementation that OSATE uses. A
model that passes the checks here passes them in OSATE, and the
analyses give the same results.

How it fits with OSATE
----------------------

The AADL tooling is not a replacement for OSATE. The graphical editor
and most analyses and annexes are still only available in OSATE.
Because both work on the same AADL files, a model an agent has worked
on can be opened in OSATE for review or further analysis, and the other
way around.

Each release of the tooling is built on a recent OSATE release.
Feedback and bug reports are welcome in the `issue tracker`_.

Getting started
---------------

To install the extension, search for AADL2 in the Extensions view of
Visual Studio Code. It is also listed in the `Visual Studio
Marketplace`_ and on `Open VSX`_. No separate Java installation is
needed.

On macOS, install osate-cli with Homebrew::

    brew install osate/osate/osate-cli

Linux packages and downloadable archives are available on the `releases
page`_. Here, too, Java is included.

.. _`issue tracker`: https://github.com/osate/aadl-tooling/issues
.. _`Visual Studio Marketplace`: https://marketplace.visualstudio.com/items?itemName=osate.aadl2
.. _`Open VSX`: https://open-vsx.org/extension/osate/aadl2
.. _`releases page`: https://github.com/osate/aadl-tooling/releases
