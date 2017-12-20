# Public

## Outlets ( introspection )

### Provides

- Types
- Commands
- Parameter Operations [Type-Types:Type-Types]
- Signals [RUN | STOP | RESUME | STOPPED | LOAD | UNLOAD | SUSPEND | STORE | ERRORS]
- Statics (introspect, ...)
- Behaviours | Behaviour-Graphs

### Supports

- Platform {Mask}
- Stores [Components]
- Signals [RUN | STOP | RESUME | STOPPED | LOAD | UNLOAD | SUSPEND | STORE | ERRORS]
- Parameter Operations [Type-Types]
- Commands
- Types
- Renderers [CLI|SPEECH|AR|VR|WEBKIT|TEXT|API|CUSTOM|CASCADE]

### Emits | Consumes 

For 3th parties only, we don't want to use 'events' anymore !!!

- Event[Type-Types]

## Protocols

- Built-Ins
- [Components]

## Statics

- stats (object|self)
- diagnose (self)
- inspect (object, type-type)
- info (version, deps, ...)
- signals (ie: a component as command)

@TODO
