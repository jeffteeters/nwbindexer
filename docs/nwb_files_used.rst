.. index::
   single: NWB files used

NWB files used
==============

This sections lists the NWB files used for the :ref:`speed_check.py <speed_check>`
utility example run which has partial output given in the previous section.  The
files used are:

* File: *Steinmetz2019_Forssmann_2017-11-05.nwb* (267.96 MB).
  From an NWB-formatted dataset referenced in Steinmetz et al. Nature 2019.
  Available at: https://figshare.com/articles/Datasets_from_Steinmetz_et_al_2019_in_NWB_format/11274968
  MD5: fc4052bffd3c2f4cf8d42f000696348c

* A data file from Buzsaki Lab. File: *YutaMouse41-150903.nwb* (10 GB).  It is available from
  https://buzsakilab.nyumc.org/datasets/NWB/SenzaiNeuron2017/
  MD5: 3dd2251ba2c61abb9edae1117bbaecf0

* The first 16 files from the alm-1 data set at CRCNS.org, which contains anterior motor
  cortex recordings from the Svoboda Lab at Janelia Farm. (Total 2.2 GB).
  Available from: http://crcns.org/data-sets/motor-cortex/alm-1
  MD5 sums are listed with the files at CRCNS.org.

* Files in file *nwb_1_28.zip* from the Anne K Churchland lab.17 (28 files, 17 GB).
  Available from: http://labshare.cshl.edu/shares/library/repository/37693/
  MD5: b9890ad36b7721a1b1c921289f19c698

* Files generated from the PyNWB tutorials. (22 files, 542 MB total).  The tutorials
  (Python code to generate the files) are at:
  https://pynwb.readthedocs.io/en/latest/tutorials/index.html
  The version of the tutorials used here was from commit 4f054b87 (which was the
  latest on Dec 27, 2019).  Steps for generating the same version of the files are:

  ``git clone --recurse-submodules https://github.com/NeurodataWithoutBorders/pynwb.git``

  ``cd pynwb``

  ``git log --oneline -1``

  If output is NOT:

    4f054b87 (HEAD -> dev, tag: latest, origin/dev, origin/HEAD) Update legacy import of ObjectMapper (#1124)

  then do:
  
    ``git checkout 4f054b87``

  (To checkout the version of PyNWB used to generate the version of the NWB files used in the *speed_check.py* run).
  Once the proper version of PyNWB is checked-out, do:

    ``pip install -r requirements.txt``

    ``pip install .``

    ``cd docs/gallery/general``

    ``python file.py``

   (The 'python' command generates file *example_file_path.nwb*).  To generate the other NWB files,
   run the python command on the other .py files in both general and the "gallery/domain" directory.
   (In directory "general" files: *advanced_hdf5_io.py*, *extensions.py*, *iterative_write.py*,
   *linking_data.py*, *scratch.py*);
   in directory "domain" files: *ecephys.py*, *icephys.py*, *ophys.py*, and *brain_observatory.py*).
   A total of 24 NWB files should be generated.  They are included in the list below.

The list of files (in the index file, e.g. *nwb_index.db*) used in the 
:ref:`speed_check.py example run <speed_check>` is given below.
This list was displayed by running the *query_index.py* program in interactive
mode in the directory containing file *nwb_index.db*.

.. code-block:: none

   $ query_nwbindex ./
   Using index_path: './nwb_index.db'
   Opening './nwb_index.db'
   Searching 70 files:
   1. ./Steinmetz2019_Forssmann_2017-11-05.nwb
   2. ./YutaMouse41-150903.nwb
   3. ./alm-1/data_structure_ANM210861_20130701.nwb
   4. ./alm-1/data_structure_ANM210861_20130702.nwb
   5. ./alm-1/data_structure_ANM210861_20130703.nwb
   6. ./alm-1/data_structure_ANM210862_20130626.nwb
   7. ./alm-1/data_structure_ANM210862_20130627.nwb
   8. ./alm-1/data_structure_ANM210862_20130628.nwb
   9. ./alm-1/data_structure_ANM210863_20130626.nwb
   10. ./alm-1/data_structure_ANM210863_20130627.nwb
   11. ./alm-1/data_structure_ANM210863_20130628.nwb
   12. ./alm-1/data_structure_ANM214427_20130805.nwb
   13. ./alm-1/data_structure_ANM214427_20130806.nwb
   14. ./alm-1/data_structure_ANM214427_20130807.nwb
   15. ./alm-1/data_structure_ANM214427_20130808.nwb
   16. ./alm-1/data_structure_ANM214429_20130805.nwb
   17. ./alm-1/data_structure_ANM214429_20130806.nwb
   18. ./alm-1/data_structure_ANM214429_20130807.nwb
   19. ./churchland/mouse1_fni16_150817_001_ch2-PnevPanResults-170808-190057.nwb
   20. ./churchland/mouse1_fni16_150818_001_ch2-PnevPanResults-170808-180842.nwb
   21. ./churchland/mouse1_fni16_150819_001_ch2-PnevPanResults-170815-163235.nwb
   22. ./churchland/mouse1_fni16_150820_001_ch2-PnevPanResults-170808-185044.nwb
   23. ./churchland/mouse1_fni16_150821_001-002_ch2-PnevPanResults-170808-184141.nwb
   24. ./churchland/mouse1_fni16_150825_001-002-003_ch2-PnevPanResults-170814-191401.nwb
   25. ./churchland/mouse1_fni16_150826_001_ch2-PnevPanResults-170808-002053.nwb
   26. ./churchland/mouse1_fni16_150827_001_ch2-PnevPanResults-170807-171156.nwb
   27. ./churchland/mouse1_fni16_150828_001-002_ch2-PnevPanResults-170807-204746.nwb
   28. ./churchland/mouse1_fni16_150831_001-002_ch2-PnevPanResults-170807-193348.nwb
   29. ./churchland/mouse1_fni16_150901_001_ch2-PnevPanResults-170807-072732.nwb
   30. ./churchland/mouse1_fni16_150903_001_ch2-PnevPanResults-170809-075033.nwb
   31. ./churchland/mouse1_fni16_150904_001_ch2-PnevPanResults-170809-073123.nwb
   32. ./churchland/mouse1_fni16_150915_001_ch2-PnevPanResults-170806-163508.nwb
   33. ./churchland/mouse1_fni16_150916_001-002_ch2-PnevPanResults-170806-114920.nwb
   34. ./churchland/mouse1_fni16_150917_001_ch2-PnevPanResults-170806-110934.nwb
   35. ./churchland/mouse1_fni16_150918_001-002-003-004_ch2-PnevPanResults-170715-124821.nwb
   36. ./churchland/mouse1_fni16_150921_001_ch2-PnevPanResults-170715-114212.nwb
   37. ./churchland/mouse1_fni16_150922_001_ch2-PnevPanResults-170715-120548.nwb
   38. ./churchland/mouse1_fni16_150923_001_ch2-PnevPanResults-170715-124558.nwb
   39. ./churchland/mouse1_fni16_150924_001_ch2-PnevPanResults-170715-124619.nwb
   40. ./churchland/mouse1_fni16_150925_001-002-003_ch2-PnevPanResults-170715-164713.nwb
   41. ./churchland/mouse1_fni16_150928_001-002_ch2-PnevPanResults-170716-002540.nwb
   42. ./churchland/mouse1_fni16_150929_001-002_ch2-PnevPanResults-170715-205011.nwb
   43. ./churchland/mouse1_fni16_150930_001-002_ch2-PnevPanResults-161221-134921.nwb
   44. ./churchland/mouse1_fni16_151001_001_ch2-PnevPanResults-161220-141515.nwb
   45. ./churchland/mouse1_fni16_151002_001-002_ch2-PnevPanResults-161221-152112.nwb
   46. ./churchland/mouse1_fni16_151005_001-002-003-004_ch2-PnevPanResults-161221-150439.nwb
   47. ./tutorials/domain/brain_observatory.nwb
   48. ./tutorials/domain/ecephys_example.nwb
   49. ./tutorials/domain/icephys_example.nwb
   50. ./tutorials/domain/ophys_example.nwb
   51. ./tutorials/general/advanced_io_example.nwb
   52. ./tutorials/general/basic_alternative_custom_write.nwb
   53. ./tutorials/general/basic_iterwrite_example.nwb
   54. ./tutorials/general/basic_sparse_iterwrite_compressed_example.nwb
   55. ./tutorials/general/basic_sparse_iterwrite_example.nwb
   56. ./tutorials/general/basic_sparse_iterwrite_largearray.nwb
   57. ./tutorials/general/basic_sparse_iterwrite_largechunks_compressed_example.nwb
   58. ./tutorials/general/basic_sparse_iterwrite_largechunks_example.nwb
   59. ./tutorials/general/basic_sparse_iterwrite_multifile.nwb
   60. ./tutorials/general/cache_spec_example.nwb
   61. ./tutorials/general/example_file_path.nwb
   62. ./tutorials/general/external1_example.nwb
   63. ./tutorials/general/external2_example.nwb
   64. ./tutorials/general/external_linkcontainer_example.nwb
   65. ./tutorials/general/external_linkdataset_example.nwb
   66. ./tutorials/general/processed_data.nwb
   67. ./tutorials/general/raw_data.nwb
   68. ./tutorials/general/scratch_analysis.nwb
   69. ./tutorials/general/test_cortical_surface.nwb
   70. ./tutorials/general/test_multicontainerinterface.nwb
   Enter query, control-d to quit
