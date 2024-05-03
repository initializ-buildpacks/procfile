The Procfile Buildpack is a Cloud Native Buildpack that turns the contents of a Procfile into process types.

## Behavior
This buildpack will participate if one or all of the following conditions are met:

* The application contains a `Procfile`
* A Binding exists with type `Procfile` and secret containing a `Procfile`

The buildpack will do the following:

## Bindings

The buildpack optionally accepts the following bindings:

|Key                   | Value   | Description
|----------------------|---------|------------
|`Procfile` |List of`<process-type>: <command>` entries | The entries from this Binding will be merged with those from the application's `Procfile`, if both are present. The commands from this Binding take precedence over the application's `Procfile` if there are duplicate process-types.



## License
This buildpack is released under version 2.0 of the [Apache License][a].

[a]: http://www.apache.org/licenses/LICENSE-2.0

