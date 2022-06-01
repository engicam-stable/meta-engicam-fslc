
meta-engicam-fslc
================

Engicam meta-layer based on yocto freescale community http://freescale.github.io/.

**alpha-release**


Installation
------------

To download the platform source code, you need to have repo installed.

Install the repo utility:


	mkdir ~/bin
	curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
	chmod a+x ~/bin/repo

Download the source code:


	PATH=${PATH}:~/bin
	mkdir fsl-community-bsp
	cd fsl-community-bsp
	repo init -u https://github.com/Freescale/fsl-community-bsp-platform -b kirkstone
	repo sync


Supported Machine
-----------------

- imx6ull-microgea-microdev-lcd7-can
- imx6ull-microgea-microdev-rev3
- imx6ull-microgea-microdev-lcd7
- imx6ull-microgea-microdev


First Build
-----------

	MACHINE=imx6ull-microgea DISTRO=fslc-framebuffer . setup-environment build2
	bitbake-layers add-layer ../sources/meta-engicam-fslc/
	bitbake engicam-evaluation-image-mx6ull




