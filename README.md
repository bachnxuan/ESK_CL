# ESK CHANGELOG
## RELEASE 1.6 CHANGELOG (LATEST):
#### Add:
- Kernel Rebase
- Re-submodule KernelSU-Next
- Add support for SukiSU-Ultra and Original KernelSU Manager
- Turn on CONFIG_HZ_300
- alarmtimer: Increase wakeup safety margin
  
#### Removed:
- None

#### Patch changes:
- lxc.patch:
  + Add (halium) GKI: use Android ABI padding for SYSVIPC task_struct fields
- Add next_manager.patch (Multi-manager patch):
  + Add support for manager below:
    * Official KernelSU
    * MKSU
    * KernelSU-Next
    * backslashxx's MKSU
    * rsuntk's MKSU
    * SukiSU-Ultra


-----------------------------------------------------

## RELEASE 1.5 CHANGELOG:
#### Add:
- Unsubmodule KernelSU-Next
- Add managers' signing key (KernelSU-Next, MKSU, rsuntk, xx)
- Add binder_prio drivers (May useless for AOSP)
- Add support for LXC build in workflows
- PM / freezer: Adjust the freeze timeout to 3 seconds
- mm: kmemleak: Don't die when memory allocation fails
- mm: vmpressure: Fix a race that would erroneously clear accumulated data
- mm: vmpressure: Don't cache the window size
- mm: vmpressure: Interpret zero scanned pages as 100% pressure
- mm: vmpressure: make vmpressure window variable
- mm: vmpressure: allow in-kernel clients to subscribe for events
- kernel: module.c: Force loading of modules that fail symbol version checks
- thermal: mi_thermal_interface: Add `thermal_max_brightness` node
- fs/ntfs3: Fix WARNING in ntfs_extend_initialized_size
  
#### Removed:
- None

-----------------------------------------------------

## RELEASE 1.4 CHANGELOG:
#### Add:
- sched: reduce softirq conflicts with RT
- sched/fair: Remove throughput optimization that keeps tasks on big CPUs
- sched: Allow newidle balancing to bail out of load_balance
- sched/fair: Don't needlessly migrate a lone task to a higher capacity CPU
- sched/fair: Skip idle cfs_rq
- sched/fair: Don't set LBF_ALL_PINNED unnecessarily
- sched/fair: Reduce cases for active balance
- sched/fair: Move avg_scan_cost calculations under SIS_PROP
- sched/fair: Remove SIS_AVG_CPU
- sched/features: Distinguish between NORMAL and DEADLINE hrtick
- sched/fair: Fix negative energy delta in find_energy_efficient_cpu()
- sched/fair: Fix initial util_avg calculation
- sched: Fix erroneous definition of sched_feat(RT_PUSH_IPI)
- sched/pelt: Avoid underestimation of task utilization
- PM / devfreq: Make the monitor workqueue high priority
- sched/fair: Set asym priority equally for all CPUs in a performance domain
- sched/pelt: Relax the sync of load_sum with load_avg
- sched/pelt: Relax the sync of runnable_sum with runnable_avg
- sched/pelt: Continue to relax the sync of util_sum with util_avg
- sched/fair: Prevent dead task groups from regaining cfs_rq's
- sched/fair: Remove sysctl_sched_migration_cost condition
- sched/fair: Wait before decaying max_newidle_lb_cost
- sched/fair: Skip update_blocked_averages if we are defering load balance
- sched/fair: Account update_blocked_averages in newidle_balance cost
- sched/fair: Sync load_sum with load_avg after dequeue
- sched/fair: Ensure that the CFS parent is added after unthrottling
- sched/fair: Return early from update_tg_cfs_load() if delta == 0
- sched/fair: Correctly insert cfs_rq's to list on unthrottle
- sched/pelt: Ensure that *_sum is always synced with *_avg
- sched/fair: Keep load_avg and load_sum synced
- sched,fair: Skip newidle_balance if a wakeup is pending
- sched/fair: Introduce a CPU capacity comparison helper
- sched/fair: Clean up active balance nr_balance_failed trickery
- sched/fair: Reduce long-tail newly idle balance cost
- sched/fair: Optimize test_idle_cores() for !SMT
- sched/fair: Reorder newidle_balance pulled_task tests
- sched: Use task_current() instead of 'rq->curr == p'
- sched/fair: Make sure to try to detach at least one movable task
- setlocalversion: Switch to ~
- fs: Upstream SUSFS 1.5.7
- zram: Prioritize the use of lz4 compression algorithm
- fs/ntfs3: Fix a couple integer overflows on 32bit systems
- kernel: printk: Filter out some userspace logs
- kernel/cpu: Silence abundance of logspam
- iommu: Silence logging
- kernel: printk: suspend-resume stfu
- mm: oom_kill: Reduce some verbose logging
- dtc: quiet
- cpufreq: Don't WARN_ON on non-existent cpu
- build.config.gki: Nuke check_defconfig
- kernel: Use the stock config for /proc/config.gz
  
#### Removed:

-----------------------------------------------------

## RELEASE 1.3 CHANGELOG:
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

#### Removed:
- None

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
