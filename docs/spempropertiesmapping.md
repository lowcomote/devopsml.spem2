

The following table show the mapping between the Multi Process properties identified in the challenge (https://ieeexplore.ieee.org/document/8904775) and their implementation in the SPEM metamodel (https://www.omg.org/spec/SPEM/About-SPEM/). The page numbers in the Spem implementation column refers to the official Spem book (https://www.omg.org/spec/SPEM/About-SPEM/).

| Property code | Property description | Spem implementation |
| ---- | ------------------------------ | ------------------- |
|P1|A process type (such as claim handling) is defined by the composition of one or more task types  (receive claim, assess claim, pay premium) and their relation.|In Spem 2.0 Activities represent processes. Activity is a group of  nested BreakdownElements  such as other Activity instances, Task Uses, Role Uses, Milestones (pp. 46, 97).|
|P2|Ordering constraints between task types of a process type are established through gateways, which may be sequencing, and-split, or-split, and-join and or-join.|Supported by Spem Workflow Diagram (p. 143).|
|P3|A process type has one initial task type (with which all its executions begin), and one or more final task types (with which all its executions end).|Supported by Spem Workflow Diagram (p. 143).|
|P4|Each task type is created by an actor, who will not necessarily perform it. For example, Ben Boss created the task type assess claim.|TaskDefinition are related to many Default Task Definition Performers that are related to many Role Definitions (p. 83). As Default Task Definition Performer (p. 85) extends Work Definition Performer, that (p. 41) extends Extensible Element, that (p. 36) can have a kind, Task Definition can have many kind of performers. Typical examples are (p. 85): Primary Performer, Responsible, Accountable, and so many as one wishes.|
|P5|For each task type, one may stipulate a set of actor types whose instances are the only ones that may perform instances of that task type. For example, in the XSure insurance company, only a claim handling manager or a financial  officer may authorize payments.|In SPEM a Qualification (p. 86) is an element that documents zero or more required qualifications, skills, or competences for Role and/or Task Definitions.|
|P6|A task type may alternatively be assigned to a particular set of actors who are authorized (e.g., John Smith and Paul Alter may be the only actors who are allowed to assess claims).|NO MAPPING FOUND|
|P7|For each task type (such as authorize payment)  one may stipulate the artifact types which are  used and produced. For example, assess claim uses a claim and produces a claim payment decision.|In SPEM a Task Definition has (p. 83) Work Product Definition that are artifact types used (in parameter) or produced (out parameter).|
|P8|Task types have an expected duration (which is not necessarily respected in particular occurrences).|Spem has the Planning Data element (p. 106) with properties: startDate, finishDate and duration.|
|P9|Critical task types are those whose instances are critical tasks; each of the latter must be performed by a senior actor and the artifacts they produce must be associated with a validation task.|SPEM doens't ship with this concepts out of the box but a plugin with this concepts can be built.|
|P10|Each process type may be enacted multiple times.|Reusability is a key factor for SPEM.|
|P11|Each process comprises one or more tasks.|Activities can be nested and can contain Task Use.|
|P12|Each task has a begin date and an end date.  (e.g., Assessing Claim 123 has begin date 01-Jan-19  and end date 02-Jan-19).|Spem has the Planning Data element (p. 106) with properties: startDate, finishDate and duration.|
|P13|Tasks are associated with artifacts used and produced, along with performing actors.|A Task Definition is associated with in and out parameters that are associated with Work Product Definitions. A Task Definition is also related to Role Definitions through Task Definition Perfomer associations. (p.83).|
|P14|Every artifact used or produced in a task must instantiate one of the artifact types stipulated for the task type.| Every Work Product Use is an occurrence of a Work Product Definition that can be related to a Task Definition.|
|P15|An actor may have more than one actor type (e.g., Senior Manager and Project Leader.).|To manage actor types in Spem there are the class of RoleDefinition, RoleUse , CompositeRole and TeamProfile.|
|P16|Likewise, an artifact may have more than one artifact type.|NOT POSSIBLE In SPEM. A WorkProductUse is associated with 0 or 1 WorkPRoductDefinition.|
|P17|An actor that performs a task must be authorized for that task. Typically, a class of actors is automatically authorized for certain classes of tasks.|RoleDefinition, RoleUse , CompositeRole and TeamProfile can be associated directly or indirectly to TaskDefinition (p.110).|
|P18|Actor types may specialize other actor types, in which case, all the rules that apply to instances of the specialized actor type must apply to instances of the specializing actor type. For example, if a Manager is allowed to perform tasks of a certain task type,so is a Senior Manager.|The same of P17|
|P19|Artifacts, actors and all types (including process, task, artifact and actor types) are given a set of alternative names (e.g., to cope with internationalization require- ments or variation in terminology).|NO MAPPING FOUND|








