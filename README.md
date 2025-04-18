# ESK CHANGELOG
## RELEASE 1.3 CHANGELOG (LATEST):
#### Add:
- Some optimization to DAMON
- Enable DAMON sysfs interface
- Increase thermal trip points to 16
- Upstream 5.10.236 lts
#### Removed:
- MGLRU
- sched/core: Use SCHED_RR in place of SCHED_FIFO for all users
- schedutil : cap iowait boost by uclamp_max

-----------------------------------------------------

## RELEASE 1.2 CHANGELOG:
#### Add:
- Builtin lz4hc
- Upstream lz4 1.10.0
- Don't affine sugov kthreads if DVFS is allowed from any CPU
- Always update CPU capacity when load balancing
- Allow CPU frequency changes to be amended before they're set
- Ignore rate limit when scaling up with FIE present
- Set default rate limit to 2000 us
- Allow single-CPU frequency to drop without idling
- Disable profiling subsystem
- Further logspam filtering
#### Removed:
- lz4: improve pipeline efficiency
- lz4: remove unnecessary check of ip
- lz4: reduce usage of variable cpy on decompression
- lz4: removed a few more usages of base ptr
- lz4: remove another usage of base
- lz4: simplify getPosition
- lz4_decompress: declare LZ4_decompress_safe_withPrefix64k static
- schedutil : cap iowait boost by uclamp_max
- ANDROID: cpufreq/schedutil: add up/down frequency transition rate limits
- cpufreq: schedutil: Set default up/down rate limits to 500/1000 us

-----------------------------------------------------

## RELEASE 1.1 CHANGELOG:
#### Add:
- Disabled Gentle Fair Sleepers
- Enable NEXT_BUDDY feature
- Upstream 5.10.235 lts

-----------------------------------------------------

## RELEASE 1.0 CHANGELOG:
#### Add:
- Switch to new versioning system (1.0, 1.1, 1.2,...)
- Kernel rebase
- Adapt zram entropy calculation
- Reduce ntp wakeups
- Silence more logspam
- Introduce SBalance IRQ balancer (3,7 CPU excluded)
- Change default SCHED_RR timeslice from 100 ms to 1 jiffy
- Use SCHED_RR in place of SCHED_FIFO
- Set sched_nr_migrate back to 32 on RT for Android
- Forbid Unity-based games from changing their CPU affinity
- Enable O3 optimzation
- Implement a simple task exit notifier when disabled
- Remove dependency on the profiling subsystem
- Remove DEBUG_KERNEL depend on DEBUG_KMEMLEAK|SCHED_DEBUG|SCHEDSTATS
- F2FS improvement
- kernfs: Avoid dynamic memory allocation for small write_iter() buffers
- fscrypt: Avoid dynamic memory allocation during impl selection
- selinux: Avoid dynamic memory allocation for INITCONTEXTLEN buffers
- bpf: Avoid allocating small buffers for map keys and values
- selinux: Avoid dynamic memory allocation for temporary scontext buffers
#### Removed:
- bfq i/o scheduler
- menu cpuidle gorvernor
- DEBUGFS
- zram writeback

-----------------------------------------------------

## RELEASE 250406 CHANGELOG:
#### Add:
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
#### Removed:
- Xiaomi's zram optimization
- LZ4KD
