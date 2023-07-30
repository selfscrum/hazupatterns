# Reference Data Pattern

## Use Case "Store Reference Data in a Database"

Hazu doesn't provide a feature to maintain reusable data entities. Thus we have to implement this as an application extension.
To do this, we utilitze make.com to create a data sync process. It is called via webhook when the user presses the ```Update Reference Data```button.
All entries' titles in that hazu are then synchronized with a ReferenceData database in make.com. This can be repeated, and the data stays in sync.

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/650aa864-f7c1-42f2-b5a4-4f5d7cd4fc5a)

Note that Hazu exports the title including the paragraph tags which is ok when we reimport the data later into Hazu. Otherwise, some additional cleanup code must happen in the Make workflow.
