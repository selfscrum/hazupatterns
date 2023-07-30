## Use Case "Store Reference Data in a Database"

Hazu doesn't provide a feature to maintain reusable data entities. Thus we have to implement this as an application extension.
To do this, we utilitze make.com to create a data sync process. It is called via webhook when the user presses the ```Update Reference Data```button.

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/e33989d6-f065-4d3c-87de-8613d2a154a9)

All entries' titles in that hazu are then synchronized with a ReferenceData database in make.com. This can be repeated, and the data stays in sync.

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/15a04db9-1e43-4670-8ac5-60a5a3a7d73a)

Note that Hazu exports the title including the paragraph tags which is ok when we reimport the data later into Hazu. Otherwise, some additional cleanup code must happen in the Make workflow.
