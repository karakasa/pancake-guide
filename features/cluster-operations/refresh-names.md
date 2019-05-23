# Refresh Names

After you change the name of a paremeter inside a pre-existing cluster, the new name will not reflect outside. This feature refreshes names of clusters inside a document.

### What else should I also notice?

* Pancake doesn't update referenced clusters automaically. So if you change the name in a `ghcluster` file outside current GH session, you need to update it by hand before using the feature.
* Name, nickname \(shorter name\), description are refreshed.
* As of now, Pancake doesn't refresh the type hint of parameter. The defect will be solved in following updates.

