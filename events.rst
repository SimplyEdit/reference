SimplyEdit Events
=================

SimplyEdit uses events to allow you to extend the functionality.

simply-content-loaded
---------------------

This event fires when SimplyEdit is finished initializing the page content.
It has no parameters. Use this event instead of `DocumentReady`.

simply-editmode
---------------

Fires when the user starts the editor. You can't prevent this.

simply-toolbars-loaded
----------------------

Fires when the editor is finished loading all the toolbars and plugins.


simply-data-changed
-------------------

Fires whenever data managed by SimplyEdit changes. It is fired after the 
change is resolved, so the DOM and the Editor should be in sync.

Parameters:
- dataBinding

simply-data-applied
-------------------

Fires after a data-simply-list has been updated. 

Parameter:
- Target list element.


simply-data-saved
-----------------



simply-storage-init
-------------------

simply-storage-file-saved
-------------------------

simply-storage-file-deleted
---------------------------

simply-stash
------------

simply-stashed
--------------

simply-image-save-error
-----------------------

simply-file-save-error
----------------------

simply-page-save-error
----------------------

simply-selectable-inserted
--------------------------

databind:elementresolved
------------------------

databind:resolved
-----------------

databinding:valuechanged
------------------------

databinding:pause
-----------------

databinding:resume
------------------
