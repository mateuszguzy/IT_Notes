Testtest1

AZDEV:
admin
test-admin

**Create Training Study** -> **imls** (depends on) requirements (?) -> **snapshots** (**1** - leave default, if not specified different) -> don't have to delete training videos (first two weeks) -> **Full Study** 

Duplicate patient analysis (problematic) -> must be "grouping variable" set to **subject** 

![[Pasted image 20220908092554.png]]

Adding variables in analysis -> through **set up** -> **MUST BE AT LEAST 5 VARIABLES**

![[Pasted image 20220908092728.png]]

Signals - migration

the old one: Draft <--> In Review --> New --> Watch / Alert / Standby / Closed the new one: Draft <--> In Review --> New --> Open <--> Closed

                                                  ręcznie               study loader  
załadowany data source            nie                  tak (ALL stages)  
załadowane datasety                 nie                  tak (DDL Done / Full Study)  
załadowana analiza DQA          nie                  tak (datashort - Full study, ilms-dqa - Full study)  
załadowana anliza KRI               nie                  tak (datashort - Full study, ilms-kris - Full study)  
załadowana analiza  
Duplicate Patients                    nie                    nie



**TRAINING DONE:**
- CMP-14981
- CMP-7066
- CMP-12397
- CMP-7099
- CMP-9774
- CMP-2551
- CMP-8803




**DRY RUN DONE:**
- 13.09 (**Passed: 7**)
	- (DQA) CMP-17890
	- (DQA) CMP-5336
	- (DQA) CMP-6801
	- (DQA)(SDA) CMP-15039
	- (DQA) CMP-7064
	- (DQA) CMP-11736
	- (DQA) CMP-7066
	
- 14.09 (**Passed: 10**)
	- (DQA)(MND)(PD)(PLD) CMP-9694
	- (DQA) CMP-2228
	- (AUTOMATED)(DQA) CMP-17556
	- (DQA) CMP-7068
	- (DQA) CMP-7065
	- (DQA) CMP-17899
	- (DQA) CMP-17914
	- (DQA) CMP-2229
	- (DQA) CMP-15574
	- (DQA) CMP-11005

- 15.09 (**Passed: 5**)
	- (DQA) CMP-12943
	- (PP) CMP-17684
	- (PP) CMP-17647
	- (MND) CMP-12580
	- (MND) CMP-12649
	
- 16.09 (**Passed: 5**)
	- **(BUG)** (DQA)(SIG) CMP-17592 -> already reported
	- **(DEPRECATED)** (PP) CMP-4055
	- **(BUG)** (MND) CMP-12648 -> CMP-19573
	- (MND) CMP-12562
	- (MND) CMP-15270
	- (MND) CMP-12611
	- (DQA) CMP-7325
	- (DQA) CMP-12575

DONE / BLOCKED / BUG / **ALL**:
- MND: 6 / 0 / 1 / **9**
- DQA: 19 / 1 / 0 / **21**
- PP: 2 / 0 / 1 / **3** 


REGRESSION TESTING CYCLE 1:
- 19.09
- 20.09 (Passed: 2)
	- CMP-7596
	- CMP-9595

- 21.09 (Passed: 20, Failed: 9)
	- **(BUG)** CMP-17899
	- CMP-17468
	- CMP-17458
	- **(BUG)** CMP-7066
	- **(BUG)** CMP-12746
	- CMP-11736
	- CMP-6801
	- **(BUG)** CMP-10039
	- **(BUG)** CMP-5336
	- CMP-7068
	- CMP-9693
	- CMP-7325 
	- CMP-7064
	- CMP-11005
	- CMP-7065
	- **(BUG)** CMP-15574
	- CMP-15039
	- CMP-13308
	- CMP-17512
	- CMP-9568
	- CMP-17534
	- CMP-9408
	- CMP-17469
	- **(BUG)** CMP-17890
	- CMP-2229
	- CMP-2228
	- **(BUG)** CMP-17592
	- CMP-12943
	- **(BUG)** CMP-1444 - prereqs

- 22.09 (Passed: 11, Failed: 3)
	- **(BUG)** CMP-17914 - wrong grouping
	- CMP-1731
	- CMP-17105
	- CMP-17684
	- **(BUG)** CMP-4055
	- **(BUG)** CMP-18940
	- CMP-2671
	- CMP-5319
	- CMP-5316
	- CMP-1354
	- CMP-2648
	- CMP-2650
	- CMP-1394
	- CMP-18899

- 23.09 (Passed: 9, Failed: 2)
	- CMP-1382
	- CMP-13259
	- CMP-13468
	- CMP-1393
	- **(BUG)** CMP-1378
	- CMP-1383
	- CMP-1391
	- CMP-2734
	- **(BUG)** CMP-5331
	- CMP-1397
	- CMP-18900

- 25.09 (Passed: 4, Failed: 1)
	- CMP-13263
	- CMP-13473
	- CMP-2470
	- CMP-5571
	- **(BUG)** CMP-10032

- 26.09 (Passed: 2, Failed: 0)
	- CMP-7669
	- CMP-12580

- 27.09 (Passed: 0, Failed: 0, Blocked: 11)
	- **(BLOCKED)** CMP-12575 - disappearing analysis
	- **(BLOCKED)** CMP-9394 - disappearing analysis
	- **(BLOCKED)** CMP-17925 - CP Admin
	- CMP-17562 - TODO - new/old workflow
	- CMP-6092- to fail - Gantt not displaying
	- CMP-2654- to fail - Gantt not displaying
	- CMP-7298 - to fail - Gantt not displaying
	- **(BLOCKED)** CMP-4893 - had problems with prereqs - details on slack
	- CMP-9694 - to fail - details on slack
	- CMP-18313 - automated


TODO:
- CMP-17279
- 

BEY:
- CMP-9923 
- CMP-9924
- CMP-9929
- CMP-15027
- CMP-14986
- CMP-17581
- CMP-17578

AUTOMATED:
- CMP-9914
- CMP-9758
- CMP-12755
- CMP-12519
- CMP-17556
  
Gantt not shown bug - CMP-19614

Testtest1


After completing "Editor" step and transfer to "Data Mapping" all the data is marked as "Unused" and after going back to "Editor" all data is lost.
But when doing it "step-by-step" I mean filling first "Subject visits" -> transfer to "Data Mapping", then filling "Adverse Events" (WITHOUT legend) -> transfer to "Data Mapping" everything seems to be fine. When I fill "Adverse Events" with legend in "Data Mapping" it's still marked as "Unused"
![[Pasted image 20220923142001.png]]

