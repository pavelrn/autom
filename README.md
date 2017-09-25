This is a automation test repo. 

You will find nothing interesting here :(. At least for now.

Test target is a simple network that has 
- 2 access switch (Extreme XOS), 
- 2 core/dc switches (Cumulus Linux), 
- 1 lab switch (Extreme XOS), 
- 1 edge UTM device (FortiGate).

We would like to build a solution that could do:
- compare Extreme XOS current config against the golden config block, generate delta and install delta (NAPALM-style device configuration management). Target: to run config check against many devices to sync their configs.
- compare Cumulus Linux current config against golden config block, fix the delta if needed. Target: to see if core switch configs differ in some way.
- test NAPALM with FortiGate to see if:
  * error handling is ok,
  * we can rollback if anything goes wrong (even if management is lost due to incorrect automation),
  * we can run a duag command on many devices (how to run ping specifying source IP?)
  Targets: to keep many FortiGate's configs in sync, perform diag tests (connectivity tests) after FortiGate are installed at the remote site.  
 
