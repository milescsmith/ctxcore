.. _change-log-label:

Change Log
==========

Version History
---------------

0.4.0
    * Add support for Python 3.12 and 3.13.
      * Cannot yet use 3.14 because for some reason, `scipy.__version__` does not work and causes numba to throw a fit.
    * Get rid of using `pkg_resources` since that is deprecated and instead use `importlib.resources`
    * Pin all dependencies to specific versions
    * Update code to use Path objects instead of strings for file paths.
    * Add nox for testing
    * Change build system from setuptools to uv

0.3.0
    * Add binarize function from pySCENIC.
    * Add aucell function from pySCENIC.

0.2.0
    * Remove unused RankingsDatabase classes and conversion functions.
    * Add CisTargetDatabase class for reading rankings/scores for
      regions/genes from a cisTarget scores or rankings database
      (only Feather v2 format), which requires pyarrow >= 8.0.0
      instead of <=0.17.1 needed for the old FeatherRankingDatabase
      class.
    * Update FeatherRankingDatabase to use CisTargetDatabase to read
      cisTarget databases.
    * Reformat code and update type annotations.


0.1.1
    * Add support for reading rankings databases created by
      create_cisTarget_databases as the index column in the
      Feather file is "motifs" or "tracks" instead of "features".

0.1.0
    * Project created.
