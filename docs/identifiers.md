# Identifiers
All objects in the Kubernetes REST API are unambiguously identified by a Name and a UID.

For non-unique user-provided attributes, Kubernetes provides [labels](labels.md) and [annotations](annotations.md).

## Names
Names are generally client-provided.  Only one object of a given kind can have a given name at a time (i.e., they are spatially unique).  But if you delete an object, you can make a new object with the same name.  Names are the used to refer to an object in a resource URL, such as `/api/v1/pods/some-name`.   By convention, the names of Kubernetes resources should be up to maximum length of 253 characters and consist of lower case alphanumeric characters, `-`, and `.`, but certain resources have more specific restructions.  See the [identifiers design doc](design/identifiers.md) for the precise syntax rules for names.

## UIDs
UID are generated by Kubernetes.  Every object created over the whole lifetime of a Kubernetes cluster has a distinct UID (i.e., they are spatially and temporally unique).


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/docs/identifiers.md?pixel)]()