# =============================================================================
# Oracle DBA Helpers                   (c) 2004 by IzzySoft (devel@izzysoft.de)
# -----------------------------------------------------------------------------
# $Id$
# -----------------------------------------------------------------------------
# Little helper scripts to ease the DBA's every day work
# =============================================================================

Contents
--------

1) Copyright and warranty
2) Requirements
3) Limitations
4) Scripts in this package and their usage
5) Installation

===============================================================================

1) Copyright and Warranty
-------------------------

These little programs are (c)opyrighted by Andreas Itzchak Rehberg
(devel@izzysoft.de) and protected by the GNU Public License Version 2 (GPL).
For details on the License see the file LICENSE in this directory. The
contents of this archive may only be distributed all together.

===============================================================================

2) Requirements
---------------

Since these are scripts for the Oracle DBA, it implies one simple requirement:
an Oracle Database to work on. Additionally, you must have a shell available -
what implies that you run a *NIX operating system. Tested on RedHat Linux with
the bash shell v2.

===============================================================================

3) Limitations
--------------

I tested the scripts successfully with Oracle v8.1.7, v9.0.1 and v9.2. Basically,
they should work with any version - but I cannot promise this (reports are
welcome). So far, no limitations are known - except that it will probably work
on Oracle databases only :-)

===============================================================================

4) Scripts in this package and their usage
------------------------------------------

For the syntax of all scripts, just see within their header - or run them
without any argument, so they will show it.

  Script        | Intention
  --------------+---------------------------------------------------------
  analobj.sh    | Analyzes Objects for a given schema and outputs an ASCII
                | report on chained/migrated rows.
  idxmove.sh    | Moves indices from one tablespace to another
  idxrebuild.sh | Rebuilds all INVALID indices in a given tablespace
  tabmove.sh    | Moves tables from one tablespace to another

All scripts run via Sql*Plus and use its SPOOL command to log their activities.

===============================================================================

5) Installation
---------------

1. Put all scripts into any directory you like. Make sure to keep them together
   with the "globalconf" file.
2. Edit the "globalconf" file for the database user and password to use by all
   scripts. We have to do so - no "CONNECT /" will work with remote databases
   for security reasons (although there is a way to do so, this is not
   recommended)
3. See the "Configuration section" of each script whether you need to adjust
   anything else. Usually there's no need for. Don't change things you are not
   sure about (or be aware of side effects ;)

Provided that your Oracle environment is set up properly, you should no be able
to run the scripts.

Have fun!
Izzy.