.. _myrocks_server_variables:

MyRocks Server Variables
------------------------

The MyRocks server variables expose configuration
of the underlying RocksDB engine.
There several ways to set these variables:

* For production deployments,
  you should have all variables defined in the configuration file.

* *Dynamic* variables can be changed at runtime using the ``SET`` statement.

* If you want to test things out, you can set some of the variables
  when starting ``mysqld`` using corresponding command-line options.

If a variable was not set in either the configuration file
or as a command-line option,
the default value is used.

Also, all variables can exist in one or both of the following scopes:

* *Global* scope defines how the variable affects overall server operation.

* *Session* scope defines how the variable affects operation
  for individual client connections.

.. tabularcolumns:: |p{9cm}|p{2cm}|p{2cm}|p{2cm}|

.. list-table::
   :header-rows: 1

   * - Name
     - Command Line
     - Dynamic
     - Scope
   * - :variable:`rocksdb_access_hint_on_compaction_start`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_advise_random_on_open`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_allow_concurrent_memtable_write`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_allow_mmap_reads`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_allow_mmap_writes`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_base_background_compactions`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_block_cache_size`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_block_restart_interval`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_block_size`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_block_size_deviation`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_bulk_load`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_bulk_load_allow_unsorted`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_bulk_load_size`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_bytes_per_sync`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_cache_index_and_filter_blocks`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_checksums_pct`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_collect_sst_properties`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_commit_in_the_middle`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_compact_cf`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_compaction_readahead_size`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_compaction_sequential_deletes`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_compaction_sequential_deletes_count_sd`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_compaction_sequential_deletes_file_size`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_compaction_sequential_deletes_window`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_concurrent_prepare`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_create_checkpoint`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_create_if_missing`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_create_missing_column_families`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_datadir`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_db_write_buffer_size`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_deadlock_detect`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_deadlock_detect_depth`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_debug_optimizer_no_zero_cardinality`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_debug_ttl_ignore_pk`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_debug_ttl_read_filter_ts`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_debug_ttl_rec_ts`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_debug_ttl_snapshot_ts`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_default_cf_options`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_delayed_write_rate`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_delete_obsolete_files_period_micros`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_enable_bulk_load_api`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_enable_ttl`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_enable_ttl_read_filtering`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_enable_thread_tracking`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_enable_write_thread_adaptive_yield`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_error_if_exists`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_flush_log_at_trx_commit`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_flush_memtable_on_analyze`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_force_compute_memtable_stats`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_force_compute_memtable_stats_cachetime`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_force_flush_memtable_and_lzero_now`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_force_flush_memtable_now`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_force_index_records_in_range`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_hash_index_allow_collision`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_ignore_unknown_options`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_index_type`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_info_log_level`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_is_fd_close_on_exec`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_keep_log_file_num`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_large_prefix`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_lock_scanned_rows`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_lock_wait_timeout`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_log_file_time_to_roll`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_manifest_preallocation_size`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_manual_wal_flush`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_max_background_compactions`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_max_background_flushes`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_max_background_jobs`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_max_latest_deadlocks`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_max_log_file_size`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_max_manifest_file_size`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_max_open_files`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_max_row_locks`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_max_subcompactions`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_max_total_wal_size`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_merge_buf_size`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_merge_combine_read_size`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_merge_tmp_file_removal_delay_ms`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_new_table_reader_for_compaction_inputs`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_no_block_cache`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_override_cf_options`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_paranoid_checks`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_pause_background_work`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_perf_context_level`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_persistent_cache_path`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_persistent_cache_size_mb`
     - Yes
     - No
     - Global, Session
   * - :variable:`rocksdb_pin_l0_filter_and_index_blocks_in_cache`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_print_snapshot_conflict_queries`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_rate_limiter_bytes_per_sec`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_read_free_rpl_tables`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_records_in_range`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_reset_stats`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_rpl_skip_tx_api`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_seconds_between_stat_computes`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_signal_drop_index_thread`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_sim_cache_size`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_skip_bloom_filter_on_read`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_skip_fill_cache`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_sst_mgr_rate_bytes_per_sec`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_stats_dump_period_sec`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_store_row_debug_checksums`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_strict_collation_check`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_strict_collation_exceptions`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_table_cache_numshardbits`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_table_stats_sampling_pct`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_tmpdir`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_trace_sst_api`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_unsafe_for_binlog`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_update_cf_options`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_use_adaptive_mutex`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_use_direct_io_for_flush_and_compaction`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_use_direct_reads`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_use_fsync`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_validate_tables`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_verify_row_debug_checksums`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_wal_bytes_per_sync`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_wal_dir`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_wal_recovery_mode`
     - Yes
     - Yes
     - Global
   * - :variable:`rocksdb_wal_size_limit_mb`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_wal_ttl_seconds`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_whole_key_filtering`
     - Yes
     - No
     - Global
   * - :variable:`rocksdb_write_batch_max_bytes`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_write_disable_wal`
     - Yes
     - Yes
     - Global, Session
   * - :variable:`rocksdb_write_ignore_missing_column_families`
     - Yes
     - Yes
     - Global, Session


.. variable:: rocksdb_access_hint_on_compaction_start

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-access-hint-on-compaction-start``
  :dyn: No
  :scope: Global
  :vartype: String or Numeric
  :default: ``NORMAL`` or ``1``

Specifies the file access pattern once a compaction is started,
applied to all input files of a compaction.
Possible values are:

* ``0`` = ``NONE``
* ``1`` = ``NORMAL`` (default)
* ``2`` = ``SEQUENTIAL``
* ``3`` = ``WILLNEED``

.. variable:: rocksdb_advise_random_on_open

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-advise-random-on-open``
  :dyn: No
  :scope: Global
  :vartype: Boolean
  :default: ``ON``

Specifies whether to hint the underlying file system
that the file access pattern is random,
when a data file is opened.
Enabled by default.

