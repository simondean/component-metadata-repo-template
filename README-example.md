# Example Component Metadata

The [component-metadata.yaml](component-metadata.yaml) defines components, teams and areas in the Example space.

## Confirming the contents of the `component-metadata.yaml` file is valid after making a change

You can run the following command to validate the contents of the `component-metadata.yaml` file:

```shell
$ ./gradlew build
```

The following command can also be used:

```shell
$ ./gradlew validateComponentMetadata
```

## Releasing changes to `component-metadata.yaml` file

There is no need to release changes to the [component-metadata.yaml](component-metadata.yaml) file in this repo.
When changes to the [component-metadata.yaml](component-metadata.yaml) file are merged to the main branch,
those changes will automatically become visible in the Component Catalog within the next 15 to 30 minutes, as
part of the automated refreshes of the Component Catalog.  Refreshes start every 15 minutes but take 10
to 30 minutes to complete.

## Example YAML for areas, teams and components

See the https://github.com/moneysupermarket/component-metadata-repo-template/blob/main/component-metadata.yaml
file for example YAML for areas, teams and components.

## Updating the dependency on the `com.moneysupermarket.componentcatalog:component-catalog-component-metadata` library

From time to time, the Component Catalog will make changes to the objects and fields that are supported in
`component-metadata.yaml` files. When this happens, you can bring in support for those changes to this repo by 
updating the version of the `componentMetadataVersion` setting in the [gradle.properties](gradle.properties)
file in this repo.
