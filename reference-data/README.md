# Reference Data Management

## Artifacts in Hazu
* Reference Data Entity
* Reference Point

## Artifacts in Make
### Flows
* Store Reference Data in a Database - synchronize a Hazu Reference Data Entity to Make

### Data Stores
* Reference Data Dictionary - list of all reference data entities
* Reference Data Store - all reference data is stored here

## Use Case "Store Reference Data in a Database"

Hazu doesn't provide a feature to maintain reusable data entities. Thus we have to implement this as an application extension.
To do this, we utilitze make.com to create a data sync process. It is called via webhook when the user presses the ```Update Reference Data```button.

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/48cec5f6-25c3-4c04-99a3-d0834f59cbea)

All entries' titles in that hazu are then synchronized with a ReferenceData database in make.com. Additionaly, the Reference Data entity itself is stored in the ReferenceDataDictionary table. This can be repeated, and the data stays in sync.

![image](https://github.com/selfscrum/hazupatterns/assets/64983267/15a04db9-1e43-4670-8ac5-60a5a3a7d73a)

Note that Hazu exports the title including the paragraph tags which is ok when we reimport the data later into Hazu. Otherwise, some additional cleanup code must happen in the Make workflow.
