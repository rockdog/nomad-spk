# nomad-spk

This package is heavily based from the work done for [gogs-spk](https://github.com/alexandregz/gogs-spk)

[nomad](https://www.nomadproject.io/) (Service mesh) SPK package ([Synology PacKages](https://www.synology.com/en-us/dsm/app_packages))

Install nomad into a Synology NAS.

## Requirements

Only tested on x64 (DS916+) could work on ARM since a nomad binary exists.

## Usage

Change **Package Center -> Trust Level** to **Any Publisher** and import manually the package from **Manual install**.
Finally, install with nomad web installation.

## Configuration

You can store your configuration using a `conf.d` folder inside `1_create_package/nomad/`. If you don't want to ship your configurations with the package, you can use `/etc/nomad`.

## To use with another arch

Download the binary from https://www.nomadproject.io/downloads.html, replace the content from **1_create_package/nomad** directory and exec create_spk.sh:

```~/src/nomad-spk(master)$ rm -rf 1_create_package/nomad/ && unzip nomad_1.4.4_linux_amd64.zip && mv nomad ./1_create_package/```

```$ sh create_spk.sh```

