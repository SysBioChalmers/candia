Bootstrap: docker
From: continuumio/miniconda3

%files
	paradias_env.yaml
    
%post
    mkdir -p /cephyr
    mkdir -p /local
    mkdir -p /apps
    mkdir -p /usr/share/lmod/lmod
    mkdir -p /var/hasplm
    mkdir -p /var/opt/thinlinc
    mkdir -p /usr/lib64
    touch /usr/lib64/libdlfaker.so
    touch /usr/lib64/libvglfaker.so
    touch /usr/bin/nvidia-smi

	/opt/conda/bin/conda update conda    # https://github.com/conda/conda/issues/9681
    /opt/conda/bin/conda env update --name base --file paradias_env.yaml --prune
	

%runscript
    exec "$@"
