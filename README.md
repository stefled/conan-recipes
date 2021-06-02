# conan-recipes
conan recipes added and modified

# prerequisite

- install Cuda
- linux : 
	- install last cmake version
	- install libgoogle-perftools-dev


# build

- common (from conan-solar github recipes, no change)

	used by Ceres

		conan create . 1.0.2@ -tf None -s arch=x86_64 -s compiler.cppstd=17 -s build_type=Debug --build=missing

- Ceres (from conan-solar github recipes modified for 2.0.0 version instead 2.0.0rc1)

		conan create . 2.0.0@ -tf None -s arch=x86_64 -s compiler.cppstd=17 -s build_type=Debug --build=missing -o shared=True -o use_glog=True -o use_gflags=True -o use_cxsparse=False

- flann (from conan-solar github recipes, no change)

	(linux => update with last cmake version 3.20!!!)

		conan create . 1.9.1@ -tf None -s arch=x86_64 -s compiler.cppstd=17 -s build_type=Debug --build=missing -o shared=True

- jxrlib (recipe : jxrlib_conan)
		
	used by freeimage

		conan create . v2019.10.9@ -tf None -s arch=x86_64 -s compiler.cppstd=17 -s build_type=Debug --build=missing

- libjpeg/9d (from conan-solar github recipes, no change)

	used by freeimage

		conan create . 3.18.0@ -tf None -s arch=x86_64 -s compiler.cppstd=17 -s build_type=Debug --build=missing -o shared=True

- Colmap (recipe: colmap_3_6_recipe)


		conan create . 3.6@ -tf None -s arch=x86_64 -s compiler.cppstd=17 -s build_type=Debug --build=missing -o shared=True	

# conan dependencies

## Windows : 

	FreeImage/3.18.0
    boost/1.75.0
    brotli/1.0.9
    bzip2/1.0.8
    ceres-solver/2.0.0
    colmap/3.6
    common/1.0.2
    double-conversion/3.1.5
    eigen/3.3.7
    flann/1.9.1
    freetype/2.10.4
    gflags/2.2.2
    glew/2.2.0
    glib/2.67.0
    glog/0.4.0
    glu/system
    harfbuzz/2.7.2
    jasper/2.0.16
    jbig/20160605
    jxrlib/v2019.10.9
    lcms/2.11
    libelf/0.8.13
    libffi/3.3
    libgettext/0.20.1
    libiconv/1.16
    libjpeg/9d
    libpng/1.6.37
    libpq/11.5
    libraw/0.19.5
    libtiff/4.1.0
    libwebp/1.1.0
    openexr/2.5.4
    opengl/system
    openjpeg/2.3.1
    openssl/1.1.1h
    pcre/8.44
    pcre2/10.33
    qt/5.15.2
    sqlite3/3.31.0
    xz_utils/5.2.5
    zlib/1.2.11
    zstd/1.4.8

## Linux 

	FreeImage/3.18.0
	b2/4.5.0
	boost/1.75.0
	brotli/1.0.9
	bzip2/1.0.8
	ceres-solver/2.0.0
	colmap/3.6
	common/1.0.2
	double-conversion/3.1.5
	eigen/3.3.7
	expat/2.3.0
	flann/1.9.1
	fontconfig/2.13.92
	freetype/2.10.4
	gflags/2.2.2
	glew/2.2.0
	glib/2.67.0
	glog/0.4.0
	glu/system
	harfbuzz/2.7.2
	icu/68.1
	jasper/2.0.16
	jbig/20160605
	jxrlib/v2019.10.9
	lcms/2.11
	libbacktrace/cci.20210118
	libelf/0.8.13
	libffi/3.3
	libiconv/1.16
	libjpeg/9d
	libmount/2.36
	libmysqlclient/8.0.17
	libpng/1.6.37
	libpq/11.5
	libraw/0.19.5
	libselinux/3.1
	libtiff/4.1.0
	libuuid/1.0.3
	libwebp/1.1.0
	libxml2/2.9.10
	odbc/2.3.7
	openexr/2.5.4
	opengl/system
	openjpeg/2.3.1
	openssl/1.1.1h
	pcre/8.44
	pcre2/10.33
	qt/5.15.2@bincrafters/stable
	sqlite3/3.31.0
	xkbcommon/1.0.1
	xorg/system
	xz_utils/5.2.5
	zlib/1.2.11
	zstd/1.4.8
	

	 


