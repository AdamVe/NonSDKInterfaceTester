# Non-SDK interfaces tester

This is an empty Android application project used for examination of non-SDK interfaces with the _veridex_ tool.

## Usage
1. Install [veridex](https://developer.android.com/guide/app-compatibility/restrictions-non-sdk-interfaces#test-veridex-tool)
2. Clone this repo
3. Add dependencies to library you want to examine into `app/build.gradle` dependencies section
4. build a debug apk with `./gradlew assembleDebug`
5. run _veridex_ with `./appcompat.sh --imprecise --dex-file=app-debug.apk`

## Example output
Without any dependencies:
```shell
➜  veridex-mac ./appcompat.sh --imprecise --dex-file=app-debug.apk
NOTE: appcompat.sh is still under development. It can report
API uses that do not execute at runtime, and reflection uses
that do not exist. It can also miss on reflection uses.
0 hidden API(s) used: 0 linked against, 0 through reflection
        0 in unsupported
        0 in blocked
        0 in max-target-o
        0 in max-target-p
        0 in max-target-q
        0 in max-target-r
```
