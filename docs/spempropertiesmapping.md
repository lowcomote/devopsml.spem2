



| Property code | Property description | Spem implementation |
| ---- | ------------------------------ | ------------------- |
|P1|A process type (such as claim handling) is defined by the composition of one or more task types  (receive claim, assess claim, pay premium) and their relation |In Spem 2.0 Activities represent processes. Activity is a group of  nested BreakdownElements  such as other Activity instances, Task Uses, Role Uses,Milestones (pag. 46, 97)|

|P2|Ordering constraints between task types of a process type are established through gateways, which may be sequencing, and-split, or-split, and-join and or-join.|Supported by Spem Workflow Diagram (pag. 143)|

|P3|A process type has one initial task type (with which all its executions begin), and one or more final task types (with which all its executions end)|Supported by Spem Workflow Diagram (pag. 143)|

|P4|Each task type is created by an actor, who will not necessarily perform it. For example, Ben Boss created the task type assess claim.|TaskDefinition are related to many Default Task Definition Performers that are related to many Role Definitions (pag 83). As Default Task Definition Performer (pag. 85) extends Work Definition Performer, that (pag. 41) extends Extensible Element, that (pag. 36) can have a kind, Task Definition can have many kind of performers.
Typical examples are (pag. 85): Primary Performer, Responsible, Accountable, and so many as one wishes|

|P5|For each task type, one may stipulate a set of actor types whose instances are the only ones that may perform instances of that task type. For example, in the XSure insurance company, only a claim handling manager or a financial  officer may authorize payments.|In SPEM a Qualification (pag.86) is an element that documents zero or more required qualifications, skills, or competences for Role and/or Task Definitions.|

|P6|A task type may alternatively be assigned to a particular set of actors who are authorized (e.g., John Smith and Paul Alter may be the only actors who are allowed to assess claims).|NO MAPPING FOUND|

|P7|For each task type (such as authorize payment)  one may stipulate the artifact types which are  used and produced. For example, assess claim uses a claim and produces a claim payment decision.|In SPEM a Task Definition have has (pag. 83) Work Product Definition that are artifact types used (in parameter) or produced (out parameter)|

|P8|Task types have an expected duration (which is not necessarily respected in particular occurrences).|Spem has the Planning Data element (pag. 106) with properties: startDate, finishDate and duration|

|P9|Critical task types are those whose instances are critical tasks; each of the latter must be performed by a senior actor and the artifacts they produce must be associated with a validation task.|SPEM doens't ship with this concepts out of the box but a plugin with this concepts can be done.|

|P10|Each process type may be enacted multiple times.|Reusability is a key factor for SPEM|

|P11|Each process comprises one or more tasks.|Activities can be nested and can contain task Use|

|p12|Each task has a begin date and an end date.  (e.g., Assessing Claim 123 has begin date 01-Jan-19  and end date 02-Jan-19).|Spem has the Planning Data element (pag. 106)
with properties: startDate, finishDate and duration|









