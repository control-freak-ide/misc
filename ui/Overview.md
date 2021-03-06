# Control-Freak IDE v3 - Renderers

CF3-IDE will have multiple renderers: Web & Terminal (CLI)

## Web - UI

Given the last 4 years of experience, we can simplify & unclutter the interface. As mentioned in the [overview](../Readme.md), Control-Freak is a 'vertical' or more precise a composition of loose 'components' with defaults and pre-defined layout definitions. A privileged user is free to modify these settings and save it as new 'vertical' in his new catalog of 'solutions'

## Terminal - UI

just as the web-interface just for the CLI.
@Todo: Introduce - Space Projectors here

# Overview - Changes/ New

<!-- toc -->

- [Key components](#key-components)
  * [Command (aka actions) - Renderers](#command-aka-actions---renderers)
    + [Toolbars (Changed)](#toolbars-changed)
    + [Context - Menu (Changed)](#context---menu-changed)
    + [Ribbon - Toolbar (New)](#ribbon---toolbar-new)
    + [Command palette (New)](#command-palette-new)
  * [Perspectives (New)](#perspectives-new)
  * [Navigation (Changed/New)](#navigation-changednew)
    + [New in the navigation tree](#new-in-the-navigation-tree)
      - [Behaviours](#behaviours)
  * [Inspector (New)](#inspector-new)
  * [Behaviour Graphs (New, evtl. for v4 if I run out of time)](#behaviour-graphs-new-evtl-for-v4-if-i-run-out-of-time)

<!-- tocstop -->

;

# Key components

<hr/>

## Command (aka actions) - Renderers

### Toolbars (Changed)

As in CF2, we render commands in global(top-menu), local toolbars and context-menus. Each toolbar can be modified by the user. The modification can be done globally or per context.

### Context - Menu (Changed)

As in CF2 but we will allow more sophisticated widgets in context menus (New).

### Ribbon - Toolbar (New)

- we will make the 'Ribbon' toolbar as default and provide a toggle between 'small' and 'large' icons (classic ribbon).

!['large'](./ribbons.png). Attention, this is only a prototype. The ribbon renderer will be rewritten from scratch and should look more like this : !['large'](./ribbons-fusion.png)

- commands might provide a description or preview inline in most 'command renderers' as seen above.

- recent commands will be placed as well in each command renderer.

### Command palette (New)

We will adopt widely used 'Command Palettes' :

![''](./command-palette.png)

or here a more advanced version which allows to place his preferred 'commands' to the palette it self:

![''](./command-palette-fusion.png)

## Perspectives (New)

As often mentioned (Adobe Products), we will make use of a widely adopted way of showing more customized views for workflow steps as follows:

![''](./perspectives.png)

Additionally, we extend this idea: each perspective shows the more relevant 'outlets' of items in the navigation tree. For instance, in the 'Visual Editor' perspective, we will allow connecting shown device commands to the scene's widgets (a popup will show and enumerates a widget's inputs like onClick).

**Planned perspectives:**

'Drivers/Devices' : Pure device programming

'Preview' : Simulators

'Logs/Analytics' : Device logs

'Deployment/Builds' : Shows running build tasks

'Services' : Acquired external services/APIs

'Design' : A dedicated view to manage widgets/scenes.

'Instances' : Deployed local or remote instances of an authored CF3 application, providing facilities of remote updates or debugging.

'Admin': A dedicated space to manage templates but also to customize the 'vertical' since the IDE is build out of it's own composed parts (eat your own dog food). This allows to customize toolbars, etc...

## Navigation (Changed/New)

We will unify all navigation - trees ('Files', 'Devices') into a single tree! This tree will be adjusted to the current chosen 'perspective' and shows each component's outlets respectively.

The tree however allows all sort of standard commands:

- Copy/Paste
- Dereference
- edit/ edit with,...
- Save to library
- Share to global scopes
- Publish / Preview / Simulate / Isolate,...

### New in the navigation tree

#### Behaviours

Since the IDEs internals is build upon the ideas of 'Meta-Programming', everything can be introspected and enables sort of trackable self-modification, we can apply these patterns to enable parametric 'behaviours'.

A behaviour can be a piece of code or more likely a piece of XBlox script. These scripts will be enumerated in the tree/palette and are extensible by the user. A behaviour can be applied to objects which match the desired target type (device, widget, events).

Behaviours provide inputs, outputs and settings.

**Examples**

**Widgets** : 'Make blue' . This behaviour will make the selected widget's (by expression & direct selection) background 'blue'.

**Devices** : 'Debug on Logly'. This behaviour will print all sorts of debug messages via an online service 'Logly'

**Events** : 'Show Custom Device Commands'. This behaviour could be for extending the IDE it self. The user can select a system event like 'Device became online' and append the IDEs toolbars with custom commands.

Also, behaviours are basically operations, permanent or temp. A new feature called 'timeline' will show however all modifications, and a user can rollback changes to certain moment in time or more likely, modify behaviour parameters for a certain time which then get propagated forward again = parametric.

**Usage**

- Drag'n drop on selection or IDE area/components -> Opens Dialog if the target doesn't type match and offers the new 'Parameter Operations' to assist with conversions. Also settings might be shown in the wizard.

- Command - Palette : Behaviours might get populated as commands, acts on selection, if none selected -> Opens Picker with narrowed type compatible targets.

## Inspector (New)

We will have a fixed 'Inspector' or 'Property Pane' which acts per selection or expression.

A privileged user might also inspect the IDE's own components, being able
to modify underlying XBlox scripts or behaviour graphs whereby changes can modify the 'vertical' globally itself. Again, since the IDE is built out of its own components, users might be notified with deployed instances of CF3 and they should be able to ignore certain changes promoted/deployed by the vertical designer/admin.

## Behaviour Graphs (New, evtl. for v4 if I run out of time)

As mentioned a few times, it makes sense now to introduce a new renderer for XBlox. Most power apps come with a block languages which enable wiring of blocks:

![''](./node-red.png)

My experience (1999-2010) about visual block-languages in this regard tells me that this model is over-simplified in certain complex scenarios. The problem with that single-type of wire is that a user more like would like to design data signal flow separately.
I spoke with leading heads on this subject but we couldn't find consensus due to scope differences. Fow now, I will proceed with what is best to me:

![''](./vpl-2terminal-types.png)

or as extended or pushed by me during my time as game-engine developer (game authoring):

![''](./virtools2.jpg)

I prefer the latter since it gives me the needed control of signal and data flows. Additionally, data flows can be easily intercepted by 'Parameter Operations' which usually take 2 arguments and output a result. Such conversations are better displayed less distracting as shown here (see 'Multiplication' Parameter Operation) :

![''](./virtools.gif)
