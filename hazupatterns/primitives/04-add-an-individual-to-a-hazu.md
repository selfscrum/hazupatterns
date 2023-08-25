# Add an Individual ID to a hazu

## What

* Every hazu has a permanent ID that can be used to navigate to it (via the URL in the browser). In addition,  users can apply an individual ID.

## Why

* While this is a good thing to keep identities of hazus consistent, it hurts templating. Templating is used to build a reusable structure in one part of the account, and make it available repeatedly at other parts, e.g. a predefined page for a contact profile. Each new instance of a template is an individual copy with new permanent IDs.
* But sometimes, parts of templates need to link to other parts in the same template. E.g. a link in a menu. If you would need to modify all links in a copy after having it created from the template, this would be very cumbersome. For this purpose, you can give every hazu an own individual ID. which is kept when a template is being copied.
* Another reason to create own ids if "speaking URLs" are important. The individual IDs can be used as part of the link to a hazu, thus making offline communication much easier.

## How

* Go to the settings of the hazu, and click on the link. The ID name is prepopulated with the title, but can be changed. Press "Save" to fix the new ID for this hazu.

## Caveats

* per hazu, all sub-hazus must have different ids. 
* Hazu doesn't allow to save the same id twice, unfortunately there is no warning message if you try. The Save command is simply ignored in this case.
*    If you copy a hazu with an set id to a place where already a hazu with this id exists, the new id gets a number suffix. "a" will become "a-1", the next copy "a-2" etc. Make sure that after copying the ids are set as you intended.
* Points have no visible IDs in the user interface, thus they cannot be changed that way.