http://localhost:5000/project/add?client_id=34

api/test_absence.py

api/intranet4/test_absence.py


|                    | Drop-down | System (project id) | Absence table for DD (presence / type) | Absence table for system (presence / type) |
| ------------------ |:---------:|:-------------------:|:--------------------------------------:|:------------------------------------------:|
| Planned vacation   | ------- |         86          |                                        |              yes / planowany               |
| STX Urlop          | 86 |         ---------|                   no                   |                                -------------            |
| Occasional         | ------- |         86          |                                        |           yes / okolicznościowy            |
| Leave at request   | ------- |         86          |                                        |               yes / zadanie                |
| L4                 |    87     |         87          |                   no                   |                  yes /l4                   |
| STX L4 nieodpłatne |    282    |      ---------      |                   no                   |                     -------------                       |
| Unpaid period      | ------- |         282         |                                        |              yes / bezplatny               |
| Maternity leave    | ------- |    cannot choose    |                                        |               -------------                |
| Paternity leave    | ------- |    cannot choose    |                                        |               -------------                |

LEAVE_PROJECT_ID = 86  
L4_PROJECT_ID = 87  
UNPAID_PROJECT_ID = 282  
BABY_BIRTH_PROJECT_ID = 361

def upgrade():  
    pass  
    # op.execute(user_table.update().  
    #            where(user_table.c.id in (-1, -2, -3, -4, -5, -6) and user_table.c.start_work is None)    #            .values({"start_work": "1900-01-01"}))    # op.create_index(    #     op.f("ix_late_google_event_id"), "late", ["google_event_id"], unique=False    # )    #    # op.alter_column("user", "start_work", existing_type=sa.DATE(), nullable=False)  
  
def downgrade():  
    pass  
#     op.alter_column("user", "start_work", existing_type=sa.DATE(), nullable=True)  
#     op.drop_index(op.f("ix_late_google_event_id"), table_name="late")