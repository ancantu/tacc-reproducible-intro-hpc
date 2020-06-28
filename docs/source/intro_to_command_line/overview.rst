
Introduction to the Command Line 
=================================

Getting Set Up
^^^^^^^^^^^^^^

To log in to Stampede2, follow the instructions for your operating system below.

**Mac / Linux**

.. code-block:: bash

   Open the application 'Terminal'
   ssh username@stampede2.tacc.utexas.edu
   (enter password)
   (enter 6-digit token)

**Windows**

.. code-block:: bash

   Open the application 'PuTTY'
   enter Host Name: stampede2.tacc.utexas.edu
   (click 'Open')
   (enter username)
   (enter password)
   (enter 6-digit token)

Module Objectives
^^^^^^^^^^^^^^^^^

This module will be fully interactive. Participants are **strongly encouraged** to follow along on the command line. Even if you already have command line familiarity, please follow along because we will create files / directories that we use later on in the session. After completing this module, participants should be able to:

 * Describe basic functions of essential Linux commands
 * Use Linux commands to navigate a file system and manipulate files
 * Edit files directly on a Linux system using a command line utility (e.g. vim, nano, emacs)
 * Transfer data to a remote Linux file system
 * Print, identify, and modify environment variables

Topics Covered
^^^^^^^^^^^^^^

 * Creating and changing folders (``pwd``, ``ls``, ``mkdir``, ``cd``, ``rmdir``)
 * Creating and manipulating files (``touch``, ``rm``, ``mv``, ``cp``)
 * Looking at the Contents of files (``cat``, ``more``, ``less``, ``head``, ``tail``, ``grep``)
 * Text editing with vim (insert mode, normal mode, navigating, saving, quitting)
 * Network and file transfers (``hostname``, ``whoami``, ``logout``, ``ssh``, ``scp``, ``rsync``)
 * Environment variables - purpose, printing, and defining

.. toctree::
   :maxdepth: 1
   :caption: Sections:

   command_line_01.rst
   command_line_02.rst
   command_line_03.rst
   command_line_04.rst
   command_line_05.rst
   command_line_06.rst

