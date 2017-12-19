# Control-Freak - v3

## General changes

- All features will be split into components even more 
- All components can be run as stand-alone
- All components have to provide some instrospection information such as platform-capability, user ACL, provided commands (per data structure/file format).
- Components can be re-composed into new 'verticals' which then later can be listed in a catalog
- Components can be re-composed into new components with the help of visual mapping tools as seen in 'Virtools'. I proposed this earlier in regard of xblox & behaviours
- Components provide 'commands' aka 'actions'. These commands must be compatible with the user's selection. 
- Each component's outlets (commands) and intakes may provide different implementations per interface (console, ui, micro-service)

## User - interface changes

### Settings

- we will finally introduce user ACLs (permissions) per command/settings which control the visibility in a component or 'vertical'
- settings can be inherited from a parent's scope (defaults from a 'vertical'). 
- we will keep & extend the model of scopes (project, workspace & system)
- a user can set & reset defaults per settings & scope. this will be done per popups
- the user's capabilty to change settings is controlled by the ACL's of a vertical or component's defaults
- settings are adaptive and their usage is tracked in a meta-database and is being consumed/controlled by an optional event bus (scoring components)

### Component Layout

- we will extend actions for component layouts and make them accessible as 'perspectives'

## XBlox

We keep xblox as primary DSL but extend it with a more visual editor (node-red)












