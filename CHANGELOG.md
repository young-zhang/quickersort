2.2.0
-----

 * Add `#[no_std]` support, now that it's supported in Stable Rust.
 * Use the pivot-selection-sorting-network to detect already-sorted sublists,
   and use a capped insertion sort when they're truly that easy to handle.
   This technique is credited to the LLVM project's libc++.
 * Use `no_drop` to reduce the number of swaps in the dual-pivot partitioning
   algorithm.

2.1.1
-----

 * Fix documentation typos.


2.1.0
-----

 * Add the `sort_by_key` function.


2.0.1
-----
 * Update unreachable.


2.0.0
-----

 * Use the new standalone `num_traits` crate. Because it's a part of the
   external API, this is a breaking change.
 * Prevent broken comparators from forcing the sorting algorithm to index
   out-of-bounds.


1.1.0
-----

 * Switch to a four-heap instead of a two-heap, to improve the cache locality
   on large lists.
 * Fix soundness problems in the heapsort, if the comparison function panics
   while sorting.


1.0.0
-----

 * Forked from [veddan/rust-introsort], because it didn't run on stable Rust.

[veddan/rust-introsort]: https://github.com/veddan/rust-introsort

