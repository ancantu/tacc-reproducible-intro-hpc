
Getting Set Up
==============

To log in to Stampede2, follow the instructions for your operating system below.

Mac / Linux
^^^^^^^^^^^
.. code-block:: bash

   Open the application 'Terminal'
   ssh username@stampede2.tacc.utexas.edu
   (enter password)
   (enter 6-digit token)

Windows
^^^^^^^

Windows users will need to install **PuTTY** to follow along. If you have not done so already, download the **PuTTY** "Windows Installer" `here <https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>`_.

Once **PuTTY** is installed:

* Double-click the **PuTTY** icon
* In the **PuTTY** Configuration window make sure the Connection type is SSH
* enter ``stampede2.tacc.utexas.edu`` for Host Name
* click "Open"
* answer "Yes" to the SSH security question

In the **PuTTY** terminal:

* enter your TACC user id after the "login as:" prompt, then Enter
* enter the password associated with your TACC account
* enter your 6-digit TACC token value

.. code-block:: bash

   Open the application 'PuTTY'
   enter Host Name: stampede2.tacc.utexas.edu
   (click 'Open')
   (enter username)
   (enter password)
   (enter 6-digit token)

Successful Login to Stampede2
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If your login was successful, your terminal will look something like this:


.. code-block:: bash 

   ------------------------------------------------------------------------------
                      Welcome to the Stampede2 Supercomputer
         Texas Advanced Computing Center, The University of Texas at Austin
   ------------------------------------------------------------------------------

              ** Unauthorized use/access is prohibited. **

   If you log on to this computer system, you acknowledge your awareness
   of and concurrence with the UT Austin Acceptable Use Policy. The
   University will prosecute violators to the full extent of the law.

   TACC Usage Policies:
   http://www.tacc.utexas.edu/user-services/usage-policies/
   ______________________________________________________________________________

   Welcome to Stampede2, *please* read these important system notes:

   --> Stampede2 user documentation is available at:
          https://portal.tacc.utexas.edu/user-guides/stampede2

   ---------------------- Project balances for user ancantu ----------------------
   | Name           Avail SUs     Expires | Name           Avail SUs     Expires |
   | Project1           #####  20XX-0X-XX | Project3            ####  20XX-0X-XX | 
   | Project2           #####  20XX-0X-XX | Project4            ####  20XX-0X-XX | 
   ------------------------ Disk quotas for user ancantu -------------------------
   | Disk         Usage (GB)     Limit    %Used   File Usage       Limit   %Used |
   | /home1              0.0      10.0     0.00           23      200000    0.01 |
   | /work              12.6    1024.0     1.23         3131     3000000    0.10 |
   | /scratch            0.0       0.0     0.00            4           0    0.00 |
   -------------------------------------------------------------------------------

A Note About Quotas
^^^^^^^^^^^^^^^^^^^

The welcome message you receive upon successful login to Stampede2 has useful information for you to keep track of. Especially of note is the breakdown of disk quotas for your account, as you can keep an eye on whether your usage is nearing the determined limit. 

Once your usage is nearing the quota, you'll start to experience issues that will not only impact your own work, but also impact the system for others. For example, if you're nearing your quota in ``$WORK``, and your job is repeatedly trying (and failing) to write to ``$WORK``, you will stress that file system.

Another useful way to monitor your disk quotas (and TACC project balances) at any time is to execute:

.. code-block:: bash

   login1$ /usr/local/etc/taccinfo # Generally more current than balances displayed on the portals.


