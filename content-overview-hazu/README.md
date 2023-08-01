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

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/48cec5f6-25c3-4c04-99a3-d0834f59cbea)

All entries' titles in that hazu are then synchronized copied into a bullet list in the hazus description field.

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/15a04db9-1e43-4670-8ac5-60a5a3a7d73a)

