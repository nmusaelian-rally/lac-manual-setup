# lac-manual-setup

## two flows in Jira to Rally direction

### `ac_system` table  
![ac_system](img/ac_system-J2R-S2S.png "AC system")
### `jira_system` table  
![jira_system](img/jira_system-J2R-S2S.png "JIRA system")


### `cfg_obj` table  
The names of flows are arbitrary, make them descriptive, e.g.
* Jira 2 Rally Epic 2 Feature 
* Jira 2 Rally Story 2 Story
![cfg_obj](img/two-flows.png "Cfg obj")

### insert fields
This is how this page looks like with both left and right frame when we add entries to `Cfg Obj Fld` on the bottom right.  
![cfg_obj_fld](img/cfg_obj-J2R-S2S.png "Cfg Obj Fld")

This has to be done for both flows.
### Epic/Feature field mapping  
![cfg_obj_fld1](img/flow2-cfg_obj-1.png "Epic/Feature mapping")
### Story/HierarchicalRequirement field mapping  
![cfg_obj_fld1](img/flow2-cfg_obj-2.png "Story/User Story mapping")

### `jira_sync_config` table
Jira is the source sysetm in this configuration, so `jira_sync_config` has to be configured. Here is a screenshot for configuring Story related entries:  

![jira_sync_config](img/flow2-jira_sync_cfg.png "Jira Sync Config")

Here is how `jira_field_def` looked like before I added is `duplicated by` field.  All these entries were propagated automatically: this table was not configured manually.  
![jira_sync_config](img/flow2-jira_field_def.png "Jira Field Def")

Specific to mapping of Jira's field (e.g. `duplicated by`) to Rally's `Predecessors` (don't pay attention to mismatch of duplicated to predecessor - this is just an example) an extra step is required. Attribute Type Def (`attribute_type_def`) in `ac_field_def `table has to be modified. It has to say "HiererchicalRequirement" only:  
![jira_sync_config](img/flow2-ac_field_def-4-predecessor-attrib.png "Attribute Type Def")


