Work in Progress

<h1>OpenFace++</h1>

<h2>Introduction</h2>
OpenFace++ was created for my diploma thesis. 

<h2>Comparison to OpenFace</h2>

<h3>Facial Expression Detection</h3>
The original <a href="https://github.com/TadasBaltrusaitis/OpenFace">OpenFace</a> provides excellent extraction of <a href="https://en.wikipedia.org/wiki/Facial_Action_Coding_System">Action Units</a>. OpenFace++ examines the extracted data using following two different techniques.

<h4>Logical Expressions</h4>
A rather simple approach which uses the binary AU-SVM classifications.

<h4>Support Vector Regression</h4>
More advanced. Uses libsvm trained regression. Training was done on the CK+ database.

<h3>Attention Estimation</h3>

<h3>Android Support</h3>
<img src="http://i.imgur.com/fjspkXg.jpg"/>

<h2>Dependencies</h2>
The sources of following third party components have been added to this repository. These components are linked statically into the final executable or library. You must respect their licenses.

<table>
<tr>
  <td><b>Name</b></td>
  <td><b>Description</b></td>
  <td><b>License</b></td>
  <td><b>Website</b></td>
</tr>
<tr>
  <td>OpenCV</td>
  <td>Computer Vision Framework</td>
  <td><a href="http://opencv.org/license.html">Link</a></td>
  <td><a href="http://opencv.org">http://opencv.org</a></td>
</tr>
<tr>
  <td>dlib</td>
  <td>Machine Learning</td>
  <td><a href="http://dlib.net/license.html">Link</a></td>
  <td><a href="http://dlib.net">http://dlib.net</a></td>
</tr>
<tr>
  <td>LibPNG</td>
  <td>PNG-Fileformat</td>
  <td><a href="http://www.libpng.org/pub/png/src/libpng-LICENSE.txt">Link</a></td>
  <td><a href="http://www.libpng.org/pub/png/libpng.html">http://www.libpng.org/pub/png/libpng.html</a></td>
</tr>
<tr>
  <td>LibSVM</td>
  <td>Support Vector Machines</td>
  <td><a href="http://www.csie.ntu.edu.tw/~cjlin/libsvm/COPYRIGHT">Link</a></td>
  <td><a href="http://www.csie.ntu.edu.tw/~cjlin/libsvm/">http://www.csie.ntu.edu.tw/~cjlin/libsvm/</a></td>
</tr>
<tr>
  <td>zlib</td>
  <td>ZIP-Compression</td>
  <td><a href="http://en.wikipedia.org/wiki/Zlib_License">zlib</a></td>
  <td><a href="http://www.zlib.net">http://www.zlib.net</a></td>
</tr>
<tr>
  <td>Intel TBB</td>
  <td>Multi Threading Toolkit</td>
  <td><a href="https://www.threadingbuildingblocks.org/faq/10">Apache 2.0</a></td>
  <td><a href="https://www.threadingbuildingblocks.org/">https://www.threadingbuildingblocks.org/</a></td>
</tr>
</table>

<h2>Build Instructions</h2>
Visual Studio 2015 is required. Make sure to selected C++ and Android NDK related components at setup stage.

<h3>Engine</h3>
The <a href="https://github.com/cyberjunk/OpenFace/tree/master/Engine">Engine</a> subfolder contains all libraries including the dependencies and OpenFace++ itself. These libraries are statically built and not precompiled. The first step is to build the engine using the Visual Studio 2015 solutions below. It is recommended to build the engine for all possible configurations (e.g. x86/debug being one). This step must only be done once or in case there are changes in the dependencies.

Compiled libraries are placed in: _Engine/lib/[platform]_ </br>
Debug builds include additional filename appendix: _\_d_

<ul>
<li>Windows: <a href="https://github.com/cyberjunk/OpenFace/blob/master/Engine/Engine.sln">Engine.sln</a></li>
<li>Android: <a href="https://github.com/cyberjunk/OpenFace/blob/master/Engine/Engine-Android.sln">Engine-Android.sln</a></li>
</ul>
