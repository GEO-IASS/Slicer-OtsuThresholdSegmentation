Otsu Threshold Segmentation
===========================

This module is _NOT_ actively supported or maintained (See [#3401](http://na-mic.org/Mantis/view.php?id=3401)).
The associated code has been copied from Slicer [r23589](http://viewvc.slicer.org/viewvc.cgi/Slicer4?view=revision&revision=23589)

Note also the code will _NOT_ compile is its current state. The CMakeLists.txt
will have to be tweaked.

Description
-----------

This filter creates a labeled image from a grayscale image. First, it calculates an optimal threshold that separates the image into foreground and background. This threshold separates those two classes so that their intra-class variance is minimal (see http://en.wikipedia.org/wiki/Otsu%27s_method). Then the filter runs a connected component algorithm to generate unique labels for each connected region of the foreground. Finally, the resulting image is relabeled to provide consecutive numbering.

Contributors
------------

Bill Lorensen (GE)

Acknowledgements
----------------

This work is part of the National Alliance for Medical Image Computing (NAMIC), funded by the National Institutes of Health through the NIH Roadmap for Medical Research, Grant U54 EB005149.

Licensing
---------
Materials in this repository are distributed under the following licenses:

* All software is licensed under BSD style license, with extensions to cover
contributions and other issues specific to 3D Slicer. 
See License.txt file for details.
