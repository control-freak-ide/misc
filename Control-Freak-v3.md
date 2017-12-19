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

### General

- Any user command is being tracked and is subject to xblox - macrofication, ie: being able to build compound commands. This compound commands can be stored into the User's behaviour palette whereby a wizard should assist to define outlets, intakes and content compatibility
- Most new platform features will be composed out of these behaviours and thus provide parametric functionality which then later can be de-composed or adjusted on the timeline

### Settings

- we will finally introduce user ACLs (permissions) per command/settings which control the visibility in a component or 'vertical'.
- settings can be inherited from a parent's scope (defaults from a 'vertical').
- we will keep & extend the model of scopes (project, workspace & system).
- a user can set & reset defaults per settings & scope. this will be done per popups.
- the user's capability to change settings is controlled by the ACL's of a vertical or component's defaults.
- settings are adaptive and their usage is tracked in a meta-database and is being consumed/controlled by an optional event bus (scoring components)
- A user settings or variables can be exposed/flagged by the user
- A user can expose his configuration as new 'vertical' and make it subject to the vertical library (user compositions of components and settings)
- Settings are basically distributed objects and optionally synced with other instances of the vertical

### Component Layout

- we will extend actions for component layouts and make them accessible as 'perspectives'
- users may remove components or parts (in the vertical's admin/design mode)

## XBlox

- We keep xblox as primary DSL but extend it with a more visual editor (node-red)

## Documentation / Support

- a human or machine facilitator can suggest/play commands at any time

## Storage

We keep 'files' as default and primary storage for everything but we do add adapters for databases and version control systems. Each storage system has to provide minimum set of features: versioning, branching,... The user has to be warned that a storage system's  may not be present on certain platforms (ie: mysql in chrome)

## Machine Learning system

We do introduce finally a deep learning system which acts adhoc wise on the system-bus. It can be trained and is there to provide  the machine facilitator. It consumes a user meta (scoring) context, commands, interactive documentation and content meta information as inputs. 

<hr/>

That's it for now. Specifics will be outlined in the new 'CF Platform Software Functional Specifications' & 'CF-Platform Features Summary' - V3.1 document.








