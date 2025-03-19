# Team Sunfish

> [!IMPORTANT]
> Currently development is paused.

> [!WARNING]
> Using lineageos-22.1-obsolete branch is not supported.
> Wait till i update the sources.

## Using local manifest 
Google made repo, an utility to manage huge repos that use nesting. 
Repo uses xml-like manifest file to specify clone path and git repository, 
remove (if included in other manifest file) and add repos.
In order to build android for a device, you must first clone a few things:

- Device tree
- Vendor tree
- Kernel tree
- Other hardware repos

But with repo manifest you can automate this process with writing a manifest,
which will include device specific stuff. You can write your own one or use our.
Out manifest is located at [team-sunfish/manifest](https://github.com/team-sunfish/manifest).
To use it you simply need to clone (or copy the manifest file from) this repo to 
```ANDROID_CLONE_DIRECTORY/.repo/local_manifests/```, after that rerun repo sync if
you are adding the manifest after syncing.
