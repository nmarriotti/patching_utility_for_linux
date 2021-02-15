# Linux Patching Utility

This script creates a snapshot of files and/or entire directory structures and patches files that are specified in a manifest file. Patching is completed using the diff and patch commands.

## How to Use

Open _manifest.cfg_ and add each file or folder that you would like included in the patch to a new line.

### Build the Manifest

The manifest contains MD5 hashes, file paths for where the file/folder resides in the patch, and the destination where the file/folder is to be placed on the fileystem as well as the file attributes.

```
./patch build
```

### Patching

```
./patch
```
