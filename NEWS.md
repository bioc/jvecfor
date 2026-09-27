# Changes in jvecfor 1.0.3 (2026-09-28)

* Fix fastFindKNN() returning distances as character on Windows, where
  Java writes CRLF line endings

# Changes in jvecfor 1.0.2 (2026-09-28)

* Remaining Java integration tests in test-utils.R now also skip when
  Java < 20 is on PATH

# Changes in jvecfor 1.0.1 (2026-09-27)

* Examples, vignette and tests now skip when Java < 20 is on PATH,
  instead of failing (fixes build ERROR on kunpeng2)

# Changes in jvecfor 1.0.0 with java backend 4.0.0-rc.8 (2026-04-30)

* Release of Bioconductor Version 3.23

# Changes in jvecfor 0.99.5 (2026-03-31)

* Fix NOTES

# Changes in jvecfor 0.99.4 (2026-03-31)

* Remove `inst/NEWS.Rd`

# Changes in jvecfor 0.99.3 (2026-03-31)

* Adapt BiocNeighbors integration to 2.5.4 API (Bioc 3.23)

# Changes in jvecfor 0.99.2 (2026-03-31)

* JvecforParam/JvecforIndex S4 classes for BNPARAM drop-in integration
* Native sparse matrix support via MatrixMarket in Java backend
* Binary format for dense matrices, processx for process management
* jvecfor_setup() uses tools::R_user_dir() per Bioconductor policy
* Test coverage 70.9\% -> 85.5\%
* BiocNeighbors moved to Imports; vignette updates

# Changes in jvecfor 0.99.0

* Submitted to Bioconductor.
* Initial implementation of `fastFindKNN()`, drop-in replacement for
  `BiocNeighbors::findKNN` using the jvecfor Java backend (HNSW-DiskANN and VP-tree).
* Added `fastMakeSNNGraph()` and `fastMakeKNNGraph()` convenience wrappers
  delegating graph construction to the bluster package.
* Supports euclidean, cosine, and dot_product distance metrics.
* Multi-threaded index build and search via Java ForkJoinPool.
* Optional Product Quantization (PQ) for approximately 4-8x search speedup.
