# Component Syncer for Room Combiner

Syncronises groups of like components based on a Room Combiner's state.

## Setup

![Setup](https://github.com/jcerecke/Component-Syncer-for-Room-Combiner/raw/master/images/setup.gif)

### Synced Component Names

You need to specify at least two component names, but you do not need to specify a component for every room in your room combiner. You may have a design that does not need a synced component in every room.  Non-valid component names will turn the textbox red.

### Sync By Property

These buttons specify which property from the changed control that will be pushed to other controls.

### Detected Component Type

This will show which component type is currently being detected for syncing.  This is taken from the first room that has a valid component specified.

### Synced Controls

When a component type is detected, Synced Controls will show all the controls that exist within this component type.  You can choose which controls that you would like to sync within a component.

### Room Combiner Name

Select which Room Combiner component you want to use for your component syncronisation groups.

## Usage

Just use your Room Combiner component as usual to group rooms together.  When room groups change, all synced components/controls will update to the current state of the lowest number room (with valid component) within the group.  Any control within a group can be changed, and all others will syncronise with it.

![Usage](https://github.com/jcerecke/Component-Syncer-for-Room-Combiner/raw/master/images/usage.gif)
