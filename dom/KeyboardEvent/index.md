---
title: 'KeyboardEvent'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Summary/overview, compatibility, possible examples, clean-up of MSDN headings'
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: UIEvent
    href: /dom/UIEvent
tags:
  - API_Objects
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/KeyboardEvent

---
Inherits from [UIEvent](/dom/UIEvent)[UIEvent](/dom/UIEvent)

## Properties

[altKey](/dom/KeyboardEvent/altKey)
:

[altLeft](/dom/KeyboardEvent/altLeft)
:

[char](/dom/KeyboardEvent/char)
:

[charCode](/dom/KeyboardEvent/charCode)
:

[ctrlKey](/dom/KeyboardEvent/ctrlKey)
:

[ctrlLeft](/dom/KeyboardEvent/ctrlLeft)
:

[key](/dom/KeyboardEvent/key)
:

[keyCode](/dom/KeyboardEvent/keyCode)
:

[location](/dom/KeyboardEvent/location)
:

[metaKey](/dom/KeyboardEvent/metaKey)
:

[repeat](/dom/KeyboardEvent/repeat)
:

[shiftKey](/dom/KeyboardEvent/shiftKey)
:

[shiftLeft](/dom/KeyboardEvent/shiftLeft)
:

[which](/dom/KeyboardEvent/which)
:

## Methods

[getModifierState](/dom/KeyboardEvent/getModifierState)
:   Queries the state of the specified modifier key.

[initKeyboardEvent](/dom/KeyboardEvent/initKeyboardEvent)
:   Initializes a new keyboard event that the [**createEvent**](/dom/Document/createEvent) method created.

## Events

[keydown](/dom/KeyboardEvent/keydown)
:

[keypress](/dom/KeyboardEvent/keypress)
:   Deprecated event for detecting when a key was pressed on the keyboard.

[keyup](/dom/KeyboardEvent/keyup)
:

## Inherited from UIEvent

### Properties

[detail](/dom/UIEvent/detail)
:   Gets additional, developer defined, information about an event.

[view](/dom/UIEvent/view)
:   Gets the **window** object that an event is generated from.

    [object window]

### Methods

[initUIEvent](/dom/UIEvent/initUIEvent)
:   Initializes a new user interface event that the [createEvent](/dom/Document/createEvent) method created.

### Events

[abort](/dom/UIEvent/abort)
:   Fires when the user aborts the download.

[activate](/dom/UIEvent/activate)
:   Fires when the object is set as the active element.

### Standards information

-   [Document Object Model (DOM) Level 3 Events Specification](http://go.microsoft.com/fwlink/p/?linkid=203756), Section 5.2.6
