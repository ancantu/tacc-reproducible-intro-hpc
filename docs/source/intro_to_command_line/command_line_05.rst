Network and File Transfers
==========================

In order to login or transfer files to a remote Linux file system, you must know the hostname (unique network identifier) and the username. If you are already on a Linux file system, those are easy to determine using the following commands:

.. code-block:: bash

   $ whoami
   wallen
   $ hostname -f
   login4.stampede2.tacc.utexas.edu

Given that information, a user would remotely login to this Linux machine using the Terminal command:

.. code-block:: bash

   $ ssh wallen@stampede2.tacc.utexas.edu
   (enter password)
   (enter token)

Windows users would typically use the program **PuTTY** to perform this operation. Logging out of a remote system is done using the ``logout`` command, or the shortcut ``<Ctrl+d>``:

.. code-block:: bash

  [stampede2]$ logout
  [local]$

To practice transferring files to Stampede2's ``$WORK`` and ``$SCRATCH``, we need to identify the path to our ``$WORK`` and ``$SCRATCH`` directory. To identify these paths, we can use helpful command shortcuts.

To identify the path to our ``$WORK`` directory, we can use ``cd $WORK`` or the helpful shortcut ``cdw``:

.. code-block:: bash
   
   $ cdw
   $ pwd
   /work/03439/wallen/stampede2

To identify the path to our ``$SCRATCH`` directory, we can use ``cd $SCRATCH`` or the helpful shortcut ``cds``:

.. code-block:: bash
   
   $ cds
   $ pwd
   /scratch/03439/wallen    

Copying files from your local computer to Stampede2's ``$WORK`` would require the ``scp`` command (Windows users use the program "WinSCP"):

.. code-block:: bash

   [local]$ scp my_file wallen@stampede2.tacc.utexas.edu:/work/03439/wallen/stampede2
   (enter password)
   (enter token)

In this command, you specify the name of the file you want to transfer (``my_file``), the username (``wallen``), the hostname (``stampede2.tacc.utexas.edu``), and the path you want to put the file (``/work/03439/wallen/stampede2``). Take careful notice of the separators including spaces, the @ symbol, and the colon. 

Copying files from your local computer to Stampede2's ``$SCRATCH`` using ``scp``:

.. code-block:: bash

   [local]$ scp my_file wallen@stampede2.tacc.utexas.edu:/scratch/03439/wallen
   (enter password)
   (enter token)

Copy files from Stampede2 to your local computer using the following:

.. code-block:: bash

   [local]$ scp wallen@stampede2.tacc.utexas.edu:/work/03439/wallen/stampede2/my_file ./
   (enter password)
   (enter token)

Note: If you wanted to copy ``my_file`` from ``$SCRATCH``, the path you would specify after the colon would be ``/scratch/03439/wallen/my_file``.
 
Instead of files, full directories can be copied using the "recursive" flag (``scp -r ...``). The ``rsync`` tool is an advanced copy tool that is useful for synching data between two sites. Although we will not go into depth here, example ``rsync`` usage is as follows:

.. code-block:: bash

   $ rsync -azv local remote
   $ rsync -azv remote local

This is just the basics of copying files. See example ``scp`` usage `here <https://en.wikipedia.org/wiki/Secure_copy>`_ and example ``rsync`` usage `here <https://en.wikipedia.org/wiki/Rsync>`_.

Exercise
^^^^^^^^

1. Identify which Stampede2 login node you are on (login1, login2, login3)
2. Remotely login to a different Stampede2 login node and list what files are available.
3. Logout until you are back to your original login node.
4. Copy the file ``chr21.fa`` to your local computer.

Review of Topics Covered
^^^^^^^^^^^^^^^^^^^^^^^^

+------------------------------------+-------------------------------------------------+
| Command                            |          Effect                                 |
+====================================+=================================================+
| ``hostname -f``                    |  print hostname                                 |
+------------------------------------+-------------------------------------------------+
| ``whoami``                         |  print username                                 |
+------------------------------------+-------------------------------------------------+
| ``ssh username@hostname``          |  remote login                                   |                                                 
+------------------------------------+-------------------------------------------------+
| ``logout``                         |  logout                                         |
+------------------------------------+-------------------------------------------------+
| ``cd $WORK``, ``cdw``              |  navigate to $WORK file system                  |
+------------------------------------+-------------------------------------------------+
| ``cd $SCRATCH``, ``cds``           |  navigate to $SCRATCH file system               |
+------------------------------------+-------------------------------------------------+
| ``scp local remote``               |  copy a file from local to remote               |
+------------------------------------+-------------------------------------------------+
| ``scp remote local``               |  copy a file from remote to local               |
+------------------------------------+-------------------------------------------------+
|  ``rsync -azv local remote``       |  sync files between local and remote            |
+------------------------------------+-------------------------------------------------+
|  ``rsync -azv remote local``       |  sync files between remote and local            |
+------------------------------------+-------------------------------------------------+
|  ``<Ctrl+d>``                      |  logout of host                                 |
+------------------------------------+-------------------------------------------------+
