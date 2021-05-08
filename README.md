Out-of-tree build
=================
https://buildroot.org/downloads/manual/manual.html#_building_out_of_tree

BR2_EXTERNAL and O are relative the the buildroot directory

    cd ../build
    make BR2_EXTERNAL=../ns4300n \
      BR2_DEFCONFIG='$(BR2_EXTERNAL_NS4300N_PATH)/configs/ns4300n_defconfig' \
      O=$PWD \
      -C ../ns4300n-buildroot/buildroot \
      defconfig
    make
