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

- We keep xblox as primary DSL but extend it with a more visual editor (xblox-v2)

## Documentation / Support

- a human or machine facilitator can suggest/play commands at any time

## Storage

We keep 'files' as default and primary storage for everything but we do add adapters for databases and version control systems. Each storage system has to provide minimum set of features: versioning, branching,... The user has to be warned that a storage system's  may not be present on certain platforms (ie: mysql in chrome) and thus commercial services should be offered to fullfil exports/bundlings.

## Machine Learning system

We do introduce finally a deep learning system which acts adhoc wise on the system-bus. It can be trained and is there to provide  the machine facilitator. It consumes user meta (score -> weights) context, commands, interactive documentation and content meta information as inputs.

## Interfaces

General note: This version will return to the initial platform requirements in regard of US gov. and european regulations. We will support disabled people with voice over caps., high contrast switches but also alternative keyboard methods. We will also make excessive use of the browser's accessibility APIs (no known fallbacks). Furthermore, VR renderers will become a first citizen.

Finally,

New renderers on board as built-in : CLI, text-to-speech, VR, AR glasses, local & remote APIs

New inputs: voice and gesture recognition, GPIO protocols, local & remote APIs

<hr/>

That's it for now. Specifics will be outlined in the new 'CF Platform Software Functional Specifications' & 'CF-Platform Features Summary' - V3.1 document.


## Networking

I gonna apply the last years here too and there a few minor changes:

- a main server application creates multiple contexts (multi-tenant)
- a user/tenant had til now a space on the file-system and with the new online-service capabilities this storage will be extended to data-base adapters. A user will always be alway to sync the online copy with the local version
- as mentioned, CF3 can be run entirely from terminal. The authoring or end-applications can have optional 'gui'-s as in VLC : "Add ...GUI". Such GUI can be "terminal", "blessed" (menues,...), web-ui (as we had til now) and of course full RPC interfaces to rollout your own interface.
- Protocols become inheritable, in a way that 'HTTP' will be built on 'TCP' and so forth

## Users

- As we have online service interface, users (or sub users) can be created according to ACLs (controlled by the business model intentions of MediaMerge and Pearls-Media Ltd.)
- There is a 'impose' feature to see applications as specified user


