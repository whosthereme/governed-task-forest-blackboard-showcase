# Governed Task-Forest Blackboard

**A Governed Task-Forest Blackboard Framework for Verifiable Long-Horizon Multi-Robot Execution**

This page is a lightweight public showcase for reviewers. The full source code and experimental scripts are kept private during review to protect unpublished implementation details.

## v17 Dashboard Progression

The dashboard combines the 3D lunar worksite, the evolving task forest, the standalone Execution Coupling Topology (ECT) projection, governed blackboard events, and mission metrics. The frames below are representative snapshots from one medium-scenario run.

![Dashboard progression](assets/dashboard-progression-v17.png)

## Evolving Task Forest + ECT Projection

The task forest is not a static tree. During execution, lazy nodes become grounded, recovery branches are inserted, local replacements appear, and the derived ECT exposes hard, soft, protective, and affected couplings without becoming a third persistent mission state.

![Task forest and ECT progression](assets/task-forest-ect-progression-v17.png)

## Lunar Worksite Projection

Temporary constraints, affected regions, resource holds, and robot/task markers are projected onto the lunar terrain surface to avoid misleading floating rings or terrain intersections.

![Lunar worksite](assets/lunar-worksite-v17.png)

<details>
<summary>Individual high-resolution frames</summary>

### Full Dashboard Frames

![Dashboard early](assets/dashboard-v17-t0060.png)

![Dashboard middle](assets/dashboard-v17-t0360.png)

![Dashboard late](assets/dashboard-v17-t0900.png)

### Focused Panels

![Task forest and ECT](assets/task-forest-ect-v17.png)

![ECT panel](assets/ect-panel-v17.png)

![Governed blackboard](assets/governed-blackboard-v17.png)

### Earlier Legacy Frames

The following earlier frames are retained only as historical visual context.

![Legacy dashboard progression](assets/dashboard-progression.png)

![Legacy task forest progression](assets/task-forest-evolution.png)

</details>

## What This Demonstrates

- A long-horizon lunar construction mission with a heterogeneous robot team.
- An evolving task forest with delayed grounding, recovery insertion, branch replacement, and bounded local repair.
- A standalone ECT view derived from the current task forest and governed blackboard.
- A governed blackboard that records proposals, verification records, temporary constraints, protective holds, and committed traces.
- A Three.js worksite dashboard showing terrain, zones, robot state, projected constraints, task-frontier evolution, and mission metrics.

## Review Artifact Scope

This public artifact intentionally includes only a visual demonstration and high-level method summary. It does not include:

- simulator source code,
- task-forest generation code,
- governed blackboard implementation,
- verifier and repair algorithms,
- full experiment scripts.

The complete implementation is maintained in a private repository during review and can be shared with reviewers through a controlled artifact channel if required.

## Paper Summary

The framework represents a long-horizon multi-robot mission as an evolving task forest. Online observations are projected into a governed blackboard, and decision modules may only submit typed proposals. Each proposal is verified before it can atomically update the task forest and blackboard. When faults, blocked regions, or delayed grounding events invalidate a branch, the system repairs only the affected subforest while preserving protected work outside that region.

## Contact

Repository owner: `whosthereme`
