# Control-Freak IDE v3 - Renderers

CF3-IDE will have multiple renderers: Web & Terminal (CLI)

## Web - UI

Given the last 4 years of experience, we can simplify & unclutter the interface. As mentioned in the [overview](../Control-Freak-v3.md), Control-Freak is a 'vertical' or more precise a composition of loose 'components' with defaults and pre-defined layout definitions. A privileged user is free to modify these settings and save it as new 'vertical' in his new catalog of 'solutions'

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

![''](./command-palette-fusion.png)

Additionally, we extend this idea: each perspective shows the more relevant 'outlets' of items in the navigation tree. For instance, in the 'Visual Editor' perspective, we will allow connecting shown device commands to the scene's widgets (a popup will show and enumerates a widget's inputs like onClick).

**Planned perspectives:**

'Drivers/Devices' : Pure device programming

'Preview' : Simulators

'Logs/Analytics' : Device logs

'Deployment/Builds' : Shows running build tasks

'Services' : Acquired external services/APIS

'Design' : A dedicated view to manage widgets/scenes.

'Instances' : Deployed local or remote instances of an authored CF3 application, providing facilities of remote updates or debugging.

'Admin': A dedicated space to manage templates but also to customize the 'vertical' since the IDE is build from out it's own composed parts (eat your own dog food). This allows to customize toolbars, etc...

## Navigation (Changed/New)

We will unify all navigation - trees ('Files', 'Devices') into a single tree! This tree will be adjusted to the current chosen 'perspective' and shows each component's outlets respectively.

The tree however allows all sort of standard commands:

- Copy/Paste
- Dereference
- edit/ edit with,...
- Save to library
- Share to global scopes
- Publish / Preview / Simulate / Isolate,...