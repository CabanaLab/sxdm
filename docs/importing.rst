=============================
 Importing Data into SXDM
=============================

The first step in any SXDM workflow will be to **import the raw
data into a common format**. These importer functions are written as
needed: if your preferred beamline is not here, `submit an issue`_.


APS Beamline 26-ID-C
====================

**Experimental Data (.mda) Import:**

The raw data file ``file.mda`` given to the User at 26-ID-C saves all source
data as a matlab binary file. SXDM preserves the original ("source") file
and saves imported and processed data in a second ("destination") HDF file
to be used in later analysis. The source ``file.mda`` file can be easily
imported:

.. code:: python

   import_mda(mda_path='path/to/.mda_file',
                hdf5_save_directory='path/to/save/dir', 
                hdf5_save_filename='file')

This function will iterate through all ``file.mda`` files and import all
detector channel data into the User defined hdf5 destination/file. Raw
reader values are flipped and inverted to match 26-ID-C beamline MatLab
Viewer output. 



**Diffraction Image (.tif) Import:**

The raw diffraction images ``image_#####.tif`` given to the User at 26-ID-C
will be imported based on this protocal. This saves all source data as a matlab
binary file. SXDM preserves the original ("source") file and saves imported and
processed data in a second ("destination") HDF file to be used in later analysis.
The source ``image_#####.tif`` file can be easily imported:

.. code:: python

    import_images(
        file='path/to/save/dir/file.h5',
        images_loc='/path/to/master/images/directory',
        scans=False,
        fill_num=4,
        delete=False,
        import_type='uint32',
        delimiter_function=<function delimiter_func at 0x7f0873f3fe18>,
        force_reimport=False,
        )

This function will iterate through all folders in the ``images_loc`` folders and import all
``images_####.tif`` image data into the User defined hdf5 destination/file. This will **Not**
reimport the .tif images. If the User would like to do this they can set ``force_reimport=True``