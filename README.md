# ESK CHANGELOG
## RELEASE 250406 CHANGELOG:
- TCP:
    + Builtin BIC, Westwood, H-TCP tcp congestion control
    + Enable ECN negotiation
    + Bump TTL to 255
    + Bump tcp_wmem to 20KB
    + Make tcp westwood 'rtt_min' and init_rtt' tunable
    + Some tcp westwood tuning
    + Set FQ as default net scheduler

- ZRAM:
    + Builtin zram, zsmalloc
    + Enable zram writeback
    + Set LZ4 as zram compression method

- Add some wireguard tweaks
- Add many logspam filtering
- Set schedutil as default scheduler
- Add uname override for GMS
- Remove Xiaomi's zram optimization
- Remove LZ4KD
