# ESK CHANGELOG
## RELEASE 1.0 CHANGELOG (LATEST):
- Switch to new versioning system (1.0, 1.1, 1.2,...)
- Kernel rebase
- Drop zram writeback
- Adapt zram entropy calculation
- Reduce ntp wakeups
- Drop bfq i/o scheduler
- Silence more logspam
- Introduce SBalance IRQ balancer (3,7 CPU excluded)
- Change default SCHED_RR timeslice from 100 ms to 1 jiffy
- Use SCHED_RR in place of SCHED_FIFO
- Set sched_nr_migrate back to 32 on RT for Android
- Forbid Unity-based games from changing their CPU affinity
- Enable O3 optimzation
- Drop menu cpuidle gorvernor
- Remove DEBUGFS
- Implement a simple task exit notifier when disabled
- Remove dependency on the profiling subsystem
- Remove DEBUG_KERNEL depend on DEBUG_KMEMLEAK|SCHED_DEBUG|SCHEDSTATS
- F2FS improvement
- kernfs: Avoid dynamic memory allocation for small write_iter() buffers
- fscrypt: Avoid dynamic memory allocation during impl selection
- selinux: Avoid dynamic memory allocation for INITCONTEXTLEN buffers
- bpf: Avoid allocating small buffers for map keys and values
- selinux: Avoid dynamic memory allocation for temporary scontext buffers

-----------------------------------------------------

## RELEASE 250406 CHANGELOG:
- Builtin BIC, Westwood, H-TCP tcp congestion control
- Enable ECN negotiation
- Bump TTL to 255
- Bump tcp_wmem to 20KB
- Make tcp westwood 'rtt_min' and init_rtt' tunable
- Some tcp westwood tuning
- Set FQ as default net scheduler
- Builtin zram, zsmalloc
- Enable zram writeback
- Set LZ4 as default zram compression method
- Add some wireguard tweaks
- Add many logspam filtering
- Set schedutil as default scheduler
- Add uname override for GMS
- Drop Xiaomi's zram optimization
- Drop LZ4KD
