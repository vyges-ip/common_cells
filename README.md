# common_cells

Vyges catalog mirror of [pulp-platform/common_cells](https://github.com/pulp-platform/common_cells) — PULP's shared SystemVerilog utility library.

Provides FIFOs (`fifo_v3`, `fifo_async_fwft`), CDC primitives (`cdc_2phase*`, `cdc_fifo_gray*`, `sync`), arbiters, round-robin schedulers, counters, one-hot encoders/decoders, stream elements, and RR-FIFO/register variants used across PULP IPs.

## Used by

- `vyges-ip/pulp-riscv-dbg` (`fifo_v3` inside `dm_csrs`; `cdc_2phase_clearable` inside `dmi_cdc`)
- Other PULP-sourced Vyges catalog IPs

## Key modules (86 total)

- **FIFOs**: `fifo_v3`, `fifo_async_fwft`, `stream_fifo`
- **CDC**: `sync`, `cdc_2phase`, `cdc_2phase_clearable`, `cdc_fifo_gray`, `cdc_reset_ctrlr`
- **Arbitration**: `rr_arb_tree`, `rrarbiter`
- **Encoding/Decoding**: `onehot_to_bin`, `lzc`, `popcount`
- **Stream**: `stream_arbiter`, `stream_delay`, `stream_fork`, `stream_filter`, `stream_register`
- **Counters**: `counter`, `delta_counter`, `mv_filter`

See `rtl/` for the full list.

## License

Solderpad Hardware License 0.51 — Licensees may opt to treat the Work as Apache 2.0 licensed. See `LICENSE`.

## Upstream sync

Commit pinned in `upstream.yaml`. Weekly sync via `.github/workflows/upstream-sync.yml`.
