# Component Syncer for Room Combiner

Syncronises groups of like components based on a Room Combiner's state.

## Setup

![Setup](https://github.com/jcerecke/Component-Syncer-for-Room-Combiner/raw/master/images/setup.gif)

### Synced Component Names

You need to specify at least two component names, but you do not need to specify a component for every room in your room combiner. You may have a design that does not need a synced component in every room. Non-valid component names will turn the textbox red.

### Sync By Property

These buttons specify which property from the changed control that will be pushed to other controls.

### Detected Component Type

This will show which component type is currently being detected for syncing. This is taken from the first room that has a valid component specified.

### Synced Controls

When a component type is detected, Synced Controls will show all the controls that exist within this component type. You can choose which controls that you would like to sync within a component. Indicator controls, such as LEDs, Meters, should be avoided

### Room Combiner Name

Select which Room Combiner component you want to use for your component syncronisation groups.

## Usage

Just use your Room Combiner component as usual to group rooms together. When room groups change, all synced components/controls will update to the current state of the lowest number room (with valid component) within the group. Any control within a group can be changed, and all others will syncronise with it.

### Example with Gain Components

![Usage](https://github.com/jcerecke/Component-Syncer-for-Room-Combiner/raw/master/images/usage.gif)

## Caveats

There are likely some weird edge cases around syncing components that regardless of being the same type, contain different controls within them.  EG. Custom Controls, or Crossovers with different properties.  Proceed with caution if attempting this.

## Not implemented ideas

- **Remove synced property selection** I suspect all states for all controls have a String property associated with them, so could potentially remove the property selection and just use a String property for everything.
- **Sets of Rooms** Instead using multiple instances of the plugin to syncronise multiple sets of components, the plugin could implement sets of components. Not sure how to do Synced Control selection for each set - possible in a combo box instead of a list box beside each set.
- **Restricted Values** Consider this example: 2 combinable rooms with video switchers. There are local inputs in Room A and in Room B, and also a set of Global inputs. When uncombined both rooms should only be able to access it's own local inputs, both can access global inputs at anytime. When combined, both rooms should be able to access the other rooms local inputs also. When rooms move from combined to un-combined they must not remain on a local input that belongs to the other room. Still considering how to implement for any component/control type. See my [Room Combine Switcher](https://github.com/jcerecke/Switcher-Room-Combiner) for an example of this feature.
