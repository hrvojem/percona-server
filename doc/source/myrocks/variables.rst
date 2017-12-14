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

.. variable:: rocksdb_allow_concurrent_memtable_write

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-allow-concurrent-memtable-write``
  :dyn: No
  :scope: Global
  :vartype: Boolean
  :default: ``OFF``

Specifies whether to allow multiple writers to update memtables in parallel.
Disabled by default.

.. note:: Not all memtables support concurrent writes.

.. variable:: rocksdb_allow_mmap_reads

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-allow-mmap-reads``
  :dyn: No
  :scope: Global
  :vartype: Boolean
  :default: ``OFF``

Specifies whether to allow the OS to map a data file into memory for reads.
Disabled by default.
If you enable this,
make sure that :variable:`rocksdb_use_direct_reads` is disabled.

.. variable:: rocksdb_allow_mmap_writes

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-allow-mmap-writes``
  :dyn: No
  :scope: Global
  :vartype: Boolean
  :default: ``OFF``

Specifies whether to allow the OS to map a data file into memory for writes.
Disabled by default.

.. variable:: rocksdb_base_background_compactions

  :version 5.7.19-17: Implemented
  :version 5.7.20-18: Replaced by :variable:`rocksdb_max_background_jobs`
  :cli: ``--rocksdb-base-background-compactions``
  :dyn: No
  :scope: Global
  :vartype: Numeric
  :default: ``1``

Specifies the suggested number of concurrent background compaction jobs,
submitted to the default LOW priority thread pool in RocksDB.
Default is ``1``.
Allowed range of values is from ``-1`` to ``64``.
Maximum depends on the :variable:`rocksdb_max_background_compactions`
variable. This variable has been replaced in |Percona Server| :rn:`5.7.20-18`
by :variable:`rocksdb_max_background_jobs`, which automatically decides how
many threads to allocate towards flush/compaction.

.. variable:: rocksdb_block_cache_size

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-block-cache-size``
  :dyn: No
  :scope: Global
  :vartype: Numeric
  :default: ``536870912``

Specifies the size of the LRU block cache for RocksDB.
This memory is reserved for the block cache,
which is in addition to any filesystem caching that may occur.

Minimum value is ``1024``,
because that's the size of one block.

Default value is ``536870912``.

Maximum value is ``9223372036854775807``.

.. variable:: rocksdb_block_restart_interval

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-block-restart-interval``
  :dyn: No
  :scope: Global
  :vartype: Numeric
  :default: ``16``

Specifies the number of keys for each set of delta encoded data.
Default value is ``16``.
Allowed range is from ``1`` to ``2147483647``.

.. variable:: rocksdb_block_size

  :version 5.7.19-17: Implemented
  :version 5.7.20-18: Minimum value has chaned from ``0`` to ``1024``
  :cli: ``--rocksdb-block-size``
  :dyn: No
  :scope: Global
  :vartype: Numeric
  :default: ``4096``

Specifies the size of the data block for reading RocksDB data files.
Default value is ``4096``.
Allowed range is from ``1024`` to ``18446744073709551615``.

.. variable:: rocksdb_block_size_deviation

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-block-size-deviation``
  :dyn: No
  :scope: Global
  :vartype: Numeric
  :default: ``10``

Specifies the threshold for free space allowed in a data block
(see :variable:`rocksdb_block_size`).
If there is less space remaining,
close the block (and write to new block).
Default value is ``10``, meaning that the block is not closed
until there is less than 10 bits of free space remaining.

Allowed range is from ``1`` to ``2147483647``.

.. variable:: rocksdb_bulk_load_allow_unsorted

  :version 5.7.20-18: Implemented
  :cli: ``--rocksdb-bulk-load-allow-unsorted``
  :dyn: Yes
  :scope: Global, Session
  :vartype: Boolean
  :default: ``OFF``

By default, the bulk loader requires its input to be sorted in the primary
key order. If enabled, unsorted inputs are allowed too, which are then
sorted by the bulkloader itself, at a performance penalty.

.. variable:: rocksdb_bulk_load

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-bulk-load``
  :dyn: Yes
  :scope: Global, Session
  :vartype: Boolean
  :default: ``OFF``

Specifies whether to use bulk load:
MyRocks will ignore checking keys for uniqueness
or acquiring locks during transactions.
Disabled by default.
Enable this only if you are certain that there are no row conflicts,
for example, when setting up a new MyRocks instance from a MySQL dump.

Enabling this variable will also enable
the :variable:`rocksdb_commit_in_the_middle` variable.

.. variable:: rocksdb_bulk_load_size

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-bulk-load-size``
  :dyn: Yes
  :scope: Global. Session
  :vartype: Numeric
  :default: ``1000``

Specifies the number of keys to accumulate
before committing them to the storage engine when bulk load is enabled
(see :variable:`rocksdb_bulk_load`).
Default value is ``1000``,
which means that a batch can contain up to 1000 records
before they are implicitly committed.
Allowed range is from ``1`` to ``1073741824``.

.. variable:: rocksdb_bytes_per_sync

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-bytes-per-sync``
  :dyn: No
  :scope: Global
  :vartype: Numeric
  :default: ``0``

Specifies how often should the OS sync files to disk
as they are being written, asynchronously, in the background.
This operation can be used to smooth out write I/O over time.
Default value is ``0`` meaning that files are never synced.
Allowed range is up to ``18446744073709551615``.

.. variable:: rocksdb_cache_index_and_filter_blocks

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-cache-index-and-filter-blocks``
  :dyn: No
  :scope: Global
  :vartype: Boolean
  :default: ``ON``

Specifies whether RocksDB should use the block cache for caching the index
and bloomfilter data blocks from each data file.
Enabled by default.
If you disable this feature,
RocksDB will allocate additional memory to maintain these data blocks.

.. variable:: rocksdb_checksums_pct

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-checksums-pct``
  :dyn: Yes
  :scope: Global, Session
  :vartype: Numeric
  :default: ``100``

Specifies the percentage of rows to be checksummed.
Default value is ``100`` (checksum all rows).
Allowed range is from ``0`` to ``100``.

.. variable:: rocksdb_collect_sst_properties

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-collect-sst-properties``
  :dyn: No
  :scope: Global
  :vartype: Boolean
  :default: ``ON``

Specifies whether to collect statistics on each data file
to improve optimizer behavior.
Enabled by default.

.. variable:: rocksdb_commit_in_the_middle

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-commit-in-the-middle``
  :dyn: Yes
  :scope: Global
  :vartype: Boolean
  :default: ``OFF``

Specifies whether to commit rows implicitly
when a batch contains more than the value of
:variable:`rocksdb_bulk_load_size`.
This is disabled by default
and will be enabled if :variable:`rocksdb_bulk_load` is enabled.

.. variable:: rocksdb_compact_cf

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-compact-cf``
  :dyn: Yes
  :scope: Global
  :vartype: String
  :default:

Specifies the name of the column family to compact.

.. variable:: rocksdb_compaction_readahead_size

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-compaction-readahead-size``
  :dyn: Yes
  :scope: Global
  :vartype: Numeric
  :default: ``0``

Specifies the size of reads to perform ahead of compaction.
Default value is ``0``.
Set this to at least 2 megabytes (``16777216``)
when using MyRocks with spinning disks
to ensure sequential reads instead of random.
Maximum allowed value is ``18446744073709551615``.

.. note:: If you set this variable to a non-zero value,
   :variable:`rocksdb_new_table_reader_for_compaction_inputs` is enabled.

.. variable:: rocksdb_compaction_sequential_deletes

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-compaction-sequential-deletes``
  :dyn: Yes
  :scope: Global
  :vartype: Numeric
  :default: ``0``

Specifies the threshold to trigger compaction on a file
if it has more than this number of sequential delete markers.
Default value is ``0`` meaning that compaction is not triggered
regardless of the number of delete markers.
Maximum allowed value is ``2000000`` (two million delete markers).

.. note:: Depending on workload patterns,
   MyRocks can potentially maintain large numbers of delete markers,
   which increases latency of queries.
   This compaction feature will reduce latency,
   but may also increase the MyRocks write rate.
   Use this variable together with
   :variable:`rocksdb_compaction_sequential_deletes_file_size`
   to only perform compaction on large files.

.. variable:: rocksdb_compaction_sequential_deletes_count_sd

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-compaction-sequential-deletes-count-sd``
  :dyn: Yes
  :scope: Global
  :vartype: Boolean
  :default: ``OFF``

Specifies whether to count single deletes as delete markers
recognized by :variable:`rocksdb_compaction_sequential_deletes`.
Disabled by default.

.. variable:: rocksdb_compaction_sequential_deletes_file_size

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-compaction-sequential-deletes-file-size``
  :dyn: Yes
  :scope: Global
  :vartype: Numeric
  :default: ``0``

Specifies the minimum file size required to trigger compaction on it
by :variable:`rocksdb_compaction_sequential_deletes`.
Default value is ``0``,
meaning that compaction is triggered regardless of file size.
Allowed range is from ``-1`` to ``9223372036854775807``.

.. variable:: rocksdb_compaction_sequential_deletes_window

  :version 5.7.19-17: Implemented
  :cli: ``--rocksdb-compaction-sequential-deletes-window``
  :dyn: Yes
  :scope: Global
  :vartype: Numeric
  :default: ``0``

Specifies the size of the window for counting delete markers
by :variable:`rocksdb_compaction_sequential_deletes`.
Default value is ``0``.
Allowed range is up to ``2000000`` (two million).

.. variable:: rocksdb_concurrent_prepare

  :version 5.7.20-18: Implemented
  :cli: ``--rocksdb-concurrent_prepare``
  :dyn: No
  :scope: Global
  :vartype: Boolean
  :default: ``ON``

When enabled this variable allows/encourages threads that are using
two-phase commit to ``prepare`` in parallel.
