# IAdea Debain SDK

## Installing Repo

- See https://source.android.com/setup/build/downloading#installing-repo

```
$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$ chmod a+x ~/bin/repo
```

## Initializing a Repo client

```
$ mkdir WORKING_DIRECTORY
$ cd WORKING_DIRECTORY
```

```
$ repo init -u https://github.com/iadea/iadea-linux-manifests -b master -m lionking_release.xml
```

## Downloading the source tree

```
$ repo sync
```

## Build the code

- Build individual images

```
$ make boot-image
$ make system-image
$ make oem-image
```

- Build production image

```
$ ln -s BASE_IMAGE lionking-base-image
$ make prod-image
```
