# intents

An asset-structure defines the prim-hierarchy and the kind-hierarchy of the data in USD, as well as defining how the final stage is going to be composed with various composition arcs in various prims.

What we are measing is a way to define the meaning of the prims and the layers that define them.

If we are working on a animation task in a DCC, we need to be aware of the asset-structure we are going to be using, we need to know which prim and/or layer to address and which composition arc, and we might have to navigate the stage to find what we need.

With a way to identify intents in an asset-structure, and marry our specific intent with the right one, we could simplify the aforementioned process and make it generic.

An artist working on an animation task in a DCC would need to address the layer(s) and prim(s) for the "animation intent".

The DCC could find all the intents in the loaded usd-stage, and ask for the "animation intent", which could return a specific layer and a specific prim with the overridable primvars required for the animation overlay.

With a more abstract access to the intents, we don't necessarily know the actual structure in use.

And it could make transforming structures easier, as to be able to "just" map intents across structures, when we need to export for other clients.

An agreed "shareable asset structure" could actually have an agreed "list of intents".

Some companies don't have the need for a specific "binding intent", as it could be directly integrated in the "surfacing intent".

Having a naming convention and/or a list of possible intents (basic ones), could allow to have intents possible included in other intents.

For example, a "surfacing intent" could include the "binding intent" for a company, and in a DCC, asking for the "binding intent" will mean to actually modify both surfacing and binding at the same time, because the "binding intent" is included in the "surfacing intent".
