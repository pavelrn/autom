This is a automation test repo. 

You will find nothing interesting here :(. At least for now.

Test target is a simple network that has 
- 2 access switch (Extreme XOS), 
- 2 core/dc switches (Cumulus Linux), 
- 1 lab switch (Extreme XOS), 
- 1 edge UTM device (FortiGate).

We would like to build a solution that could do:
- compare Extreme XOS current config block against the golden config block, generate delta and install delta (NAPALM-style device configuration management). Target: to run config check for many switches (branch offices) and to keep their configs in sync.
- compare Cumulus Linux current config against golden config block, fix the delta if needed. Target: to see if core switch configs differ in some way.
- test NAPALM with FortiGate to see if:
  * error handling is ok,
  * we can rollback if anything goes wrong (even if management is lost due to incorrect automation),
  * we can run a diagnose command on many devices (how to run ping specifying source IP with NAPALM?)
  Targets: to configure many FortiGate devices and to keep their configs in sync, perform diag tests (connectivity tests) from the device after a FortiGate is installed at the branch.  
 
