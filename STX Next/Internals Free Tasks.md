**TAKEN:**
- INT-79
- INT-96
- INT-39
- INT-40
- INT-90




INT-38
INT-44
INT-46
INT-47
INT-48

# **INT-47**
http://localhost:5000/client/map

| Permission            | Product Design Team Lead   | Payroll Lead     | Scrum Master    | Head of Product design   | Office Manager    | Coordinator        |
| --------------------- | :------------------------: | : ------------ : | :------------ : | :----------------------: | :-------------- : | :----------------- |
| can edit own projects | yes / no                   | yes / no (2)     | yes / no        | yes / yes                |                   |                    |
| can edit projects     |                            |                  |                 | yes / yes                | yes / yes         | yes / yes          |
| can view projects     | yes / no                   |                  | no / yes        | yes / yes                | yes / yes         | yes / yes          |

**(1) PD TL - project edit error**

![[Pasted image 20220809131700.png]]


**(2) Payroll lead - project edit error**
Gets inside project view function but don't show details

![[Pasted image 20220809142313.png]]
![[Pasted image 20220809142442.png]]

Tried:
- can_view_project_client_times
- can_view_time_client_report
- 
![[Pasted image 20220810104013.png]]

![[Pasted image 20220810144511.png]]

What happens here is a conflict of permissions. 
1. In `intranet4/project_card.py` views are decorated with Pyramid built-in `view_config()` decorator which can take only one permission. Since it's set to `can_edit_projects` users who only has permission `can_edit_own_projects` will receive `403` error.
2. Users cannot be permitted to `can_edit_projects` along with `can_edit_own_projects` because there is no validation in code which project is "own" and which not. 
3. Since `view_config()`  is a built-in decorator it requires either some big code rearrangements or maybe it can be solved with permissions rebuild.
4. Topic discussed with Krzysztof Sobolewski, and decided to leave it until proper cleaning of permissions will be done.
5. Product Design Team Lead / Payroll Lead need `can_view_projects` permission, Scrum Master, can see projects thanks to `can_see_clients` permission. But it's not consistent that way.

Deleted permission verification made on in-build Pyramid `view_config()` decorator. Instead expanded permission verification made either way on `ProjectService` UPDATE method. 

Also `ProjectService` method updated with logic verifying if user with `can_edit_own_project` permission has authority to update that certain project.


# **INT-46**
has `can_edit_prev_month_time_entry`

**Coordinator, Office Manager, Training Budget Approver**

added in `user_times.py` verification of `can_edit_prev_month_time_entry` permission


# **INT-139**
### Unnecessary date_start update after every save on user account

![[Pasted image 20220812112640.png]]
