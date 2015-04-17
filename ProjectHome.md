<p>
Build system based on make, providing a consistent build system across Windows, Linux, Mac, Android, and iPhone.  Supports at least Visual Studio and GCC compilers.<br>
</p>

# Required #
<pre>
For all features to work, your command line should support...<br>
<br>
git, hg, svn, cvs, wget, patch,<br>
bzip2, bunzip2, gzip, gunzip, tar, unzip<br>
</pre>

# Platform #
<pre>
The commands below are simply 'bbb' you should substitute the following...<br>
<br>
Windows		- ./bbb.bat<br>
Linux		- ./bbb.sh<br>
Mac		- ./bbb.sh<br>
<br>
bbb has the following basic command line structure<br>
<br>
bbb [command] [projects] [ext]<br>
<br>
command = build, checkout, compile, diff, archive, makepatch, applypatch<br>
<br>
checkout	- Checks out the specified projects<br>
update		- Updates the specified projects<br>
diff		- Creates diffs of the working directories<br>
archive		- Creates arechives of the working directories<br>
makepatch	- Makes patches of the working directories<br>
applypatch	- applies patches made with makepatch to the working directories<br>
</pre>

# To use #
<pre>
// To get started with a windows build on cygwin,<br>
// do something like the following...<br>
<br>
mkdir buildroot<br>
cd buildroot<br>
git clone https://code.google.com/p/blueberrybuild bbb<br>
cd bbb<br>
bbb checkout zlib<br>
make TGT=windows BBBROOT=/cygdrive/c/bbbroot/bbb GCCROOT=/cygdrive/c/mingw32-win<br>
</pre>

# Directory structure #
<pre>
Following directory structure is assumed<br>
<br>
-- [any directory]			- Build Root<br>
|<br>
+---[bbb]			- This project<br>
|<br>
+---[lib]			- Librarys will go here<br>
|<br>
+---[bin]			- Compiled code will go here<br>
|<br>
+---[dnl]			- Downloaded archive files<br>
|<br>
+---[arc]			- Local archives<br>
|<br>
+---[pat]			- Local patches<br>
</pre>

