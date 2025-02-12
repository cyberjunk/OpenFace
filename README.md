<h1>OpenFace++</h1>

<h2>Introduction</h2>
OpenFace++ was created for my diploma <a href="https://drive.google.com/file/d/0B-6rsj6uHlolcml6S3NDdm9BQlE/view?usp=sharing&resourcekey=0-LHcb6tKBHsOFe0-8GQDphA">thesis</a>. It is based on the original <a href="https://github.com/TadasBaltrusaitis/OpenFace">OpenFace</a> codebase from August 2016. OpenFace++ contains several modifications and extensions described below.

<hr/>
<h2>Comparison to OpenFace</h2>
OpenFace++ does NOT contain any major changes to the facial data extraction techniques already used in OpenFace. However, OpenFace++ includes the following changes compared to OpenFace.

<ul>
<li>Facial Expression Detection (using Action Units)</li>
<li>Attention Estimation (using Eye-Gaze)</li>
<li>Android Support</li>
<li>Background Worker Thread</li>
<li>Simplified API</li>
<li>Code Refactoring</li>
<li>Static Linking and Optimized Building</li>
</ul>

For more detailed information please refer to the thesis document.

<img src="http://i.imgur.com/fjspkXg.jpg"/>

<hr/>
<h2>Downloads</h2>
<table>
<tr>
<td><b>Project</b></td>
<td><b>Platform</b></td>
<td><b>Distribution</b></td>
<td><b>Download</b></td>
</tr>
<tr>
<td>MiniExample</td>
<td>Windows</td>
<td>ZIP</td>
<td>Link</td>
</tr>
<tr>
<td>FaceSensor</td>
<td>Windows</td>
<td>ZIP</td>
<td><a href="https://drive.google.com/file/d/0B-6rsj6uHlolb2t2eVVPYW12aHM/view?usp=sharing&resourcekey=0-5_eQNbXgh_B81B1NGP-yIQ">Link</a></td>
</tr>
<tr>
<td>OpenFaceAndroid</td>
<td>Android 4.4+</td>
<td>APK</td>
<td><a href="https://drive.google.com/file/d/0B-6rsj6uHlolMDZ2aDZqaTZ0aDg/view?usp=sharing&resourcekey=0-Mx98lT3H2Lj5acL6p-HoAA">Link</a></td>
</tr>
</table>

<hr/>
<h2>License</h2>
OpenFace++ was created for research purposes and does not have any additional license requirements. However, you must respect the original OpenFace <a href="https://github.com/TadasBaltrusaitis/OpenFace/blob/master/Copyright.txt">license</a> as well as the licenses of dependencies listed below.

<hr/>
<h2>Dependencies</h2>
The sources of following third party components have been added to this repository. These components are linked statically into the final application. You must respect their licenses. Unlike OpenFace, OpenFace++ does NOT require boost.

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

<hr/>
<h2>Build Instructions</h2>
Visual Studio 2015 is required. Make sure to selected C++ and Android NDK related components at setup stage.

<h3>Engine</h3>
<ul>
<li><a href="https://github.com/cyberjunk/OpenFace/tree/master/Engine">Engine</a> folder contains all dependencies and OpenFace++</li>
<li>All libraries are compiled statically from sources, no precompiled binaries!</li>
<li>Build the engine for Windows or Android using the Visual Studio 2015 solutions below.</li>
<li>Recommendation: Build engine for all available configurations (e.g. x86/debug being only one!).</li>
<li>This step must be done only once; or in case there are changes in the dependencies.</li>
<li>Compiled libraries are placed in: _Engine/lib/[platform]_</li>
<li>Debug builds include additional filename appendix: _\_d_</li>
</ul>

<h4>Windows</h4>
<table>
<tr>
  <td>VS2015 Solution:</td>
  <td><a href="https://github.com/cyberjunk/OpenFace/blob/master/Engine/Engine.sln">Engine.sln</a></td>
</tr>
<tr>
  <td>Platforms:</td>
  <td>x86, x64</td>
</tr>
</table>

<h4>Android</h4>
<table>
<tr>
  <td>VS2015 Solution:</td>
  <td><a href="https://github.com/cyberjunk/OpenFace/blob/master/Engine/Engine-Android.sln">Engine-Android.sln</a></td>
</tr>
<tr>
  <td>Platforms:</td>
  <td>ARM, ARM64, x86, x64</td>
</tr>
<tr>
  <td>Target:</td>
  <td>android-19</td>
</tr>
</table>

_Note_: The Android solution includes the additional <a href="https://github.com/cyberjunk/OpenFace/tree/master/Engine/src/openface-jni">openface-jni</a> project. This is the <a href="https://en.wikipedia.org/wiki/Java_Native_Interface">Java JNI</a> wrapper used to access OpenFace from a managed Java APP on Android. This project generates the _SO_ library file which can be loaded and called in an Android App using the _native_ keyword in Java.

<h3>MiniExample</h3>
<ul>
<li><a href="https://github.com/cyberjunk/OpenFace/tree/master/MiniExample">Folder</a></li>
<li>Minimal example as presented in my thesis.</li>
<li>For Windows only; requires Webcam.</li>
<li>Building requires successfully compiled engine for Windows!</li>
<li>Includes the openface library project. You can change, rebuild and test from here!</li>
<li>VS2015 Solution: <a href="https://github.com/cyberjunk/OpenFace/blob/master/MiniExample/MiniExample.sln">MiniExample.sln</a></li>
</ul>

<h3>FaceSensor</h3>
<ul>
<li><a href="https://github.com/cyberjunk/OpenFace/tree/master/FaceSensor">Folder</a></li>
<li>Application used for the user study in my thesis</li>
<li>For Windows only; requires Webcam.</li>
<li>Building requires successfully compiled engine for Windows!</li>
<li>Streams facial data data using OSC network protocol.</li>
<li>Includes the openface library project. You can change, rebuild and test from here!</li>
<li>VS2015 Solution: <a href="https://github.com/cyberjunk/OpenFace/blob/master/FaceSensor/FaceSensor.sln">FaceSensor.sln</a></li>
</ul>

<h3>OpenFaceAndroid</h3>
<ul>
<li><a href="https://github.com/cyberjunk/OpenFace/tree/master/OpenFaceAndroid">Folder</a></li>
<li>Test project for Android Studio</li>
<li>(!) Requires compatible SO library from _openface-jni_</li>
<li>(!) Contains duplicated resources from _Engine/res_</li>
</ul>
