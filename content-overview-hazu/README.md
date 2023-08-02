# Content Overview Hazu

## Artifacts in Hazu
* Content Overview Hazu

## Artifacts in Make
### Flows
* Content Overview Hazu - synchronize a hazu's underlying objects with the description of the hazu.

### Data Stores
none

## Use Case "Content Overview Hazu"

Using a hazu to collect different types of data like in a form is valuable for different processes. Sometimes, a data selection can be quite lenghty, and the "form hazu" shall not be cluttered with the selection.

The idea of this use case is to reflect the underlying objects (which might be selected from an Import) as a bullet list in the hazu's description field.
To do this, we utilitze make.com to create a data sync process. It is called via webhook when the user presses the ```Update Overview ```button.

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/6e3beac0-1a12-4ad4-8ff5-4c5e81f613c2)

All entries' titles in that hazu are then synchronized copied into a bullet list in the hazus description field.

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/a9645bba-e481-4ad5-b415-60dedbe8627e)# Content Overview Hazu

## Setup
Creators of a Content Overview Hazu must prepare its usage:
Open the description in code mode and replace the upper case placeholders with the correct values

* WEBHOOK_ID_FROM_MAKE - the make.com id of the content-overview-hazu flow. This can be set in the template because it will not change after initial setup.
* HAZU_URL_OF_REFERENCE_DATA - the URL postfix that identifies the permalink to the hazu in question. To be replaced per instance.
* THE_ID_OF_THE_NODE - the internal ID, or the last part of the URL string. To be replaced per instance.
* THE_INVITE_CODE - the invite code of the hazu. To be replaced per instance.
* THE_PARENT_INVITE_CODE - To be replaced per instance. Unfortunately, the modification of a hazu description is considered a change in the hazu's parent's realm, so we need to set this too.

## Note
* Nested display is not supported, only the upper level is shown

