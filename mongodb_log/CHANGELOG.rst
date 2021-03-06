^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package mongodb_log
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.1.6 (2014-11-06)
------------------

0.1.5 (2014-11-05)
------------------

0.1.4 (2014-10-29)
------------------

0.1.3 (2014-10-21)
------------------

0.1.2 (2014-10-20)
------------------

0.1.1 (2014-10-17)
------------------

0.1.0 (2014-10-16)
------------------
* This adds latched recording and playback to the log and playback nodes.
  This is the final part of the functionality to close `#5 <https://github.com/strands-project/mongodb_store/issues/5>`_
* Added meta logging to other C++ loggers.
* Calling on correct document.
* Building up type processing knowledge.
* Adding meta information to C++-logged documents.
* Handlings strings which cannot be treated as UTF-8 as binary.
* Moved back to processes to test.
* Debugging ulimit issue.
* Contributors: Nick Hawes

0.0.5 (2014-10-09)
------------------

0.0.4 (2014-09-13)
------------------
* added libssl and libcrypto for ubuntu distros where this is needed due to the static nature of the libmongoclient.a
* Contributors: Marc Hanheide

0.0.3 (2014-08-18)
------------------
* Renamed rosparams `datacentre_` to `mongodb_`.
  Fixes `#69 <https://github.com/strands-project/ros_datacentre/issues/69>`_
* Renamed ros_datacentre to mongodb_store for to fix `#69 <https://github.com/strands-project/ros_datacentre/issues/69>`_.
* Contributors: Nick Hawes

0.0.2 (2014-08-07)
------------------
* Dynamically choose MongoDB API
  Use Connection if using an older mongopy, otherwise use MongoClient.
* Cleaned up boilerplate in mongodb_log package.xml
  Removed a bunch of XML comments (that came from the package.xml
  template) from the package.xml file. Added pymongo as a run dependency.
* Main process no longer calls init_node.
  This fixes bugs related to calling init_node multiple times in the same
  process. Main process now has its own signal handler for shutting down
  cleanly.
* Added 'inserted_at' meta with proper date object to logged data.
  This added compatibility with message store and also allows native date queries on results.
* Changes to how meta info is stored.
* Added boost filesystem for new version of ld.
* Added mongo dependency
* More benchmark removal
* REmoved rrd bits.
* Removing benchmarking stuff.
* Restructuring for new repo position.
* Moved all files into mongodb_log subdirectory for later inclusion in a broader package.
* Contributors: Alex Bencz, Christian Dondrup, Nick Hawes
