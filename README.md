Microdosimetry extensions for TOPAS
---

  - Jan Schuemann and Hongyu Zhu. First implementation. 11/2019
  - Jose Ramos-Mendez. Update to OpenTOPAS v4.0/Geant4 v11.1.3 05/2024

---

The microdosimetry extension provides settings for common microdosimeters, scoring of lineal energy (y/dy) and a biological weight function based on microdosimetric properties.

## The extension is described in:

### :books: Zhu, H., Chen, Y., Sung, W., McNamara, A. L., Tran, L. T., Burigo, L. N., et al. (2019). The microdosimetric extension in TOPAS: development and comparison with published data. Physics in Medicine and Biology, 64(14), 145004. [http://doi.org/10.1088/1361-6560/ab23a3](http://doi.org/10.1088/1361-6560/ab23a3)

---

## Installation.

> [!NOTE]
> The main difference in installing for Debian/Ubuntu and MacOS is the installation paths. 

> [!TIP]
> Users can install multiple extensions by either:
> - Copy all the Extension directories into a common global directory, or
> - Using the `\;` between directory paths:
>   `-DTOPAS_EXTENSIONS_DIR=/MyProject1Extensions/\;/MyProject2Extensions/`

### Debian

Follow [installation for Debian/Ubuntu](https://opentopas.readthedocs.io/en/latest/getting-started/Debian.html) procedures after and including **step 8.4**. Then:

    $ cd $HOME/Applications/

Clone the repository:

    $ git clone https://github.com/OpenTOPAS/OpenTOPAS-Microdosimetry.git

Return to the topas-build directory:

    $ cd $HOME/Applications/TOPAS/OpenTOPAS-build

Repeat `cmake` command by including the `TOPAS_EXTENSIONS_DIR` variable as follows (don't miss the `-D`):

    $ cmake ../OpenTOPAS -DCMAKE_INSTALL_PREFIX=../OpenTOPAS-install -DTOPAS_EXTENSIONS_DIR=$HOME/Applications/OpenTOPAS-Microdosimetry

Build:

    $ make -j8 install

### MacOS

Follow [installation for MacOS](https://opentopas.readthedocs.io/en/latest/getting-started/MacOS.html) procedures after and including **step 7.4**. Then:

    $ cd /Applications

Clone the repository:

    $ git clone https://github.com/OpenTOPAS/OpenTOPAS-Microdosimetry.git

Return to the topas-build directory:

    $ cd /Applications/TOPAS/OpenTOPAS-build

Repeat `cmake` command by including the `TOPAS_EXTENSIONS_DIR` variable as follows (don't miss the `-D`):

    $ cmake ../OpenTOPAS -DCMAKE_INSTALL_PREFIX=../OpenTOPAS-install -DTOPAS_EXTENSIONS_DIR=/Applications/OpenTOPAS-Microdosimetry

Build:

    $ make -j8 install
    
