# android_MediaProvider
## clone android MediaProvider source code and modify its branch marshmallow-release
git clone https://android.googlesource.com/platform/packages/providers/MediaProvider

## branch marshmallow-release
https://github.com/scofieldhsu/android_MediaProvider/tree/marshmallow-release

## why modified
* originally you can only issue an adb command to trigger Android media scan if you update some file in external storage by 'adb shell am broadcast -a android.intent.action.MEDIA_SCANNER_SCAN_FILE -d file:///storage/emulated/0/xxx.JPEG' and the command must specify scheme and file path (the command is too long, easy to type wrong and when if there are many files ...)
* now you can just issue an adb command to trigger Android media scan for external storage by command 'adb shell am broadcast -a android.intent.action.MEDIA_SCANNER_SCAN_DIR' (the command is very simple)
