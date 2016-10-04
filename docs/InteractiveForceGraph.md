# `<InteractiveForceGraph />`

## Usage

```javascript
import React from 'react';
import { ForceGraph, ForceGraphNode, ForceGraphLink } from 'react-vis-force';

<InteractiveForceGraph
  simulationOptions={{ height: 300, width: 300 }}
  labelAttr="label"
  onSelectNode={(node) => console.log(node)}
  highlightDependencies
>
  <ForceGraphNode node={{ id: 'first-node', label: 'First node', radius: 5 }} fill="red" />
  <ForceGraphNode node={{ id: 'second-node', label: 'Second node', radius: 5 }} fill="blue" />
  <ForceGraphLink link={{ source: 'first-node', target: 'second-node' }} />
</InteractiveForceGraph>
```

## Props

`<InteractiveForceGraph />` inherits all of the props from [`<ForceGraph />`](ForceGraph.md), and adds:

### onSelectNode(event, node)
Called each time the user selects a new node.

### onDeselectNode(event, node)
Called each time the user deselects a node.

### defaultSelectedNode(node)
The node to set as selected by default.

### highlightDependencies
When true, the dependencies of a hovered or selected node are given the highlighted treatment.

### opacityFactor
Used to scale opacity when hovering or selecting nodes. Ex. `0.6`