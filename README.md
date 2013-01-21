nifti-vtk 
=========

This is a simple code I've gathered to load volumetric NIFTI data into VTK using
ITK. 

Notice that it should load a bunch of [volume formats supported by
ITK](http://www.itk.org/Wiki/ITK/File_Formats) too.

It is a minimal adaptation of code from
[here](http://www.vtk.org/Wiki/index.php?title=VTK/ExamplesBoneYard/Cxx/VolumeRendering/itkVtkImageConvert&oldid=50606),
and
[here](http://public.kitware.com/Wiki/ITK/Examples/WishList/IO/itkVtkImageConvertDICOM),
but it's handy in case you're wondering how to get there ;)

Building 
========

Just follow the instructions:

1. Build VTK and ITK from their git repositories.

		cd && mkdir VTK-ITK && cd VTK-ITK

		git clone git://vtk.org/VTK.git && git clone git://vtk.org/VTKData.git
		git clone git://itk.org/ITK.git && git clone git://itk.org/ITKData.git
	
2. Run respective CMAKE configuration. Remember to set ITK with
   **Module\_ITKVtkGlue = TRUE** :exclamation:

3. Run respective ```make && make install``` 

4. After that, the following command should work :P 

		cmake && make && ./nifti-vtk <Path_to_you_nifti_file>

5. Enjoy!
