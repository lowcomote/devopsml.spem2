



| Property code | Property description | Spem implementation |
| ---- | ------------------------------ | ------------------- |
|P1|A process type (such as claim handling) is defined by the composition of one or more task types  (receive claim, assess claim, pay premium) and their relation |In Spem 2.0 Activities represent processes. Activity is a group of  nested BreakdownElements  such as other Activity instances, Task Uses, Role Uses,Milestones (pag. 46, 97)|
|--------|-----------|------------|
|P2|Ordering constraints between task types of a process type are established through gateways, which may be sequencing, and-split, or-split, and-join and or-join.| Supported by Spem Workflow Diagram (pag. 143)|