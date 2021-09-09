# Snodar Releases

## Manual Release

* To start, build the firmware. (generate .hex)

* When building, take note of the dis.h defines for software revision, and model.

> ~~To trigger automatic updating from the application, make sure that the version number in dis.h is greater than the last release.~~

> Versioning will now be based off of a build timestamp, compared against target hardware, triggered by changes in the production repo.
> firmware version should be changed between builds to give feedback on issues. Future implemtation could utilize a build-hash/tag id to guarantee unique identification of firmware versions on-device.

> Build Archiving: When builds are archived, unsupported, deprecated etc., we will discontinue attaching them as assets to the tagged release. Instead, their json will persist, but the last released version for that target will contain appropriate tags (ie, theoretical snodar 0p1 would include `'release': {deprecated:true, archive:'link-to-tagged-release', file:'same-release-name.zip'}`)

* Next, run the nordic script to create a firmware bundle.

> See secure dfu, w/ private key bundling


* Modify the releases.json to include an update for your release target.

Example:


```json
{
  "Snodar": {
    "1p0": 
    {
      "release":{
        "file":"snodar-firmwarebundle-release.zip",
        "time":1617229629,
        "version":"0.0.8"
      },
      "beta": {
        "file":"snodar-firmwarebundle-beta.zip",
        "time":1617229629,
        "version":"0.0.8"
      },
      "nightly": {
        "file":"snodar-firmwarebundle-nightly.zip",
        "time":1617229629,
        "version":"0.0.8"
      }
    }
  }
}

```

Release Item as an interface:

```typescript
  interface ReleaseItem {
    model: string,
    hw_rev: string,
    file: string,
    version: string,
    time: number, //unix timestamp
    notes?: string[] //Notes are optional. 
  }
```

* After the JSON has been modified, commit, and push the releases repository.

* Tag the release on github, and attach all firmware bundles (listed in the json) as assets. Attach the releases.json file as an asset as well.



## Automated Release Steps

1. Detect change on Production/Release Branch
1. Read Build Configuration
    - Get List of Builds
    - For Each Build, find Model and version (in dis.h)
1. Build each item in list
1. For each successfully built item, bundle with appropriate key. Name bundle uniquely. (ie, model-version.zip)
1. On successful bundle, create json object to represent bundle. 
    - `[model]:{[hw_rev]:{file:model-version.zip, version:version, time:timestamp}}`
1. Merge all successful bundle json objects into new object: `{model1, model2...}`
1. Write bundle json object to releases repository.
1. Commit + Push + Tag Release
1. Add release.json, and the respective bundles as assets to tagged release.
