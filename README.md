### l2arc_feed_again
### l2arc_feed_min_ms
### l2arc_feed_secs
### l2arc_headroom
### l2arc_headroom_boost
### l2arc_nocompress
### l2arc_noprefetch
### l2arc_norw
### l2arc_write_boost
### l2arc_write_max
### metaslab_debug
### spa_config_path
### zfetch_array_rd_sz
### zfetch_block_cap
### zfetch_max_streams
### zfetch_min_sec_reap
### zfs_arc_grow_retry
### zfs_arc_max
---
**Value Type:** Number of bytes

**Default Value:** Half of system ram

**Tuning:**

By changing this number you change the amount of memory zfs will use for its
[Adaptive Replacement Cache]
(http://open-zfs.org/wiki/Performance_tuning#Adaptive_Replacement_Cache)
. Increasing this number will help read speeds from your pools, as zfs will
store data it needs in fast RAM instead of needing to get it off the disk.

### zfs_arc_memory_throttle_disable
**Value Type:** A boolean, 0 or 1

**Default Value:** 0 after 0.6.1

**Tuning:**

This boolean was used to enable or disable improvements made to the
arc_memory_throttle so it could be tested by interested parties prior to it
being the default. The only version where you should worry abut setting this
would be 0.6.0 and you would want to set it to 0.

### zfs_arc_meta_limit
**Value Type:** Number of bytes

**Default Value:** 1/4 of zfs_arc_max

**Tuning:**

By changing this number you change the amount of ARC memory that will be used
for metadata. Metadata is anything that is not actual data asked for, for
example block checksums and tree traversal data. This tunable is unique to ZoL
other OpenZFS may not place a limit on metadata (so zfs_arc_meta_limit =
zfs_arc_max). Check /proc/spl/kstat/zfs/arcstats/arc_meta_used vs
/proc/spl/kstat/zfs/arcstats/arc_meta_limit to see if you should consider
increasing this value.

### zfs_arc_meta_prune
### zfs_arc_min
### zfs_arc_min_prefetch_lifespan
### zfs_arc_p_min_shift
### zfs_arc_shrink_shift
### zfs_autoimport_disable
### zfs_deadman_enabled
### zfs_deadman_synctime
### zfs_dedup_prefetch
### zfs_disable_dup_eviction
### zfs_expire_snapshot
### zfs_flags
### zfs_free_min_time_ms
### zfs_immediate_write_sz
### zfs_mdcomp_disable
### zfs_nocacheflush
### zfs_no_scrub_io
### zfs_no_scrub_prefetch
### zfs_no_write_throttle
### zfs_pd_blks_max
### zfs_prefetch_disable
### zfs_read_chunk_size
### zfs_recover
### zfs_resilver_delay
### zfs_resilver_min_time_ms
### zfs_scan_idle
### zfs_scan_min_time_ms
### zfs_scrub_delay
### zfs_sync_pass_deferred_free
### zfs_sync_pass_dont_compress
### zfs_sync_pass_rewrite
### zfs_top_maxinflight
### zfs_txg_history
### zfs_txg_synctime_ms
### zfs_txg_timeout
### zfs_vdev_aggregation_limit
### zfs_vdev_cache_bshift
### zfs_vdev_cache_max
### zfs_vdev_cache_size
### zfs_vdev_max_pending
### zfs_vdev_min_pending
### zfs_vdev_mirror_switch_us
### zfs_vdev_ramp_rate
### zfs_vdev_read_gap_limit
### zfs_vdev_scheduler
### zfs_vdev_time_shift
### zfs_vdev_write_gap_limit
### zfs_write_limit_inflated
### zfs_write_limit_max
### zfs_write_limit_min
### zfs_write_limit_override
### zfs_write_limit_shift
### zfs_zevent_cols
### zfs_zevent_console
### zfs_zevent_len_max
### zil_replay_disable
### zil_slog_limit
### zio_bulk_flags
### zio_delay_max
### zio_injection_enabled
### zio_requeue_io_start_cut_in_line
### zvol_inhibit_dev
### zvol_major
### zvol_max_discard_blocks
### zvol_threads
