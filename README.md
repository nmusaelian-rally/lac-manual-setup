# lac-manual-setup

## two flows in Jira to Rally direction

### `ac_system` table  
![ac_system](img/ac_system-J2R-S2S.png "ac_system")
### `jira_system` table  
![jira_system](img/jira_system-J2R-S2S.png "jira_system")


### `cfg_obj` table  
The names of flows are arbitrary, make them descriptive, e.g.
* Jira 2 Rally Epic 2 Feature 
* Jira 2 Rally Story 2 Story
![cfg_obj](img/two-flows.png "cfg_obj")

### insert fields
This is how this page looks like with both left and right frame when we add entries to `Cfg Obj Fld` on the bottom right.  
![cfg_obj_fld](img/cfg_obj-J2R-S2S.png "cfg_obj_fld")

This has to be done for both flows:
![cfg_obj_fld1](img/flow2-cfg_obj-1.png "Epic/Feature mapping")
![cfg_obj_fld1](img/flow2-cfg_obj-2.png "Story/User Story mapping")

