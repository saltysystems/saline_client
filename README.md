# Gremlin Client v1.0

## About
This Godot plugin will allow your Godot applications to download and update the
latest & greatest client bindings from your own Gremlin server.

## Usage

1. Open your Godot project, or use an existing one.
2. Copy the `addons` directory from this repository to your project
3. Click `Project`, then `Project Settings`.
4. Choose the `Plugins` tab, and set the GremlinClient plugin to `Active`

At this point, the Gremlin client panel will appear in Godot. 

You will want to add your server address, e.g. 
```
http://address.of.your.server:<port>/client/download
```

The `/client/download` route is the standard route for autogenerated Gremlin
zip files.

Next, you'll want to create or select an output directory. By default, Gremlin
assumes that you will put scripts in `res://scripts`. 

Once Gremlin compiles your client libraries, it will delete the intermediate
format `.proto` files downloaded from the server. You keep these files if you
wish by selecting `Do not delete .proto files`. However, they are not directly
used by any Gremlin client library.