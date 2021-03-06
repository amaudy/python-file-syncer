# File Syncer

Python program which synchronizes files from a local directory to one of the
storage providers supported by [Libcloud](http://libcloud.apache.org/).

## Features

* Synchronize files from a local directory to one of the supported providers
  * User can specify a list of filename patterns which should be excluded
  * User can specify to delete files in the container that do not exist locally
* Restore files from the remote server to a local directory

## Usage

```shell
file-syncer --help
```

### Synchronizing files from a local directory to a remote server

```shell
file-syncer --username=<api username> --key=<api key or password> \
            --provider=<libcloud provider constant - e.g. CLOUDFILES_US> \
            --container-name=<target container name>  \
            --directory=<path to directory used to synchronize> \
            --delete
```

### Restoring files from the remote server to a local directory

```shell
file-syncer --username=<api username> --key=<api key or password> \
            --restore \
            --provider=<libcloud provider constant - e.g. CLOUDFILES_US> \
            --container-name=<remote container name>  \
            --directory=<path to directory where the files will be restored to>
```

## License

This library is distributed under the [Apache 2.0 license](http://www.apache.org/licenses/LICENSE-2.0.html).
