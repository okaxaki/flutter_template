This repository stores the output of `flutter create` for each Flutter version.

Every time the Flutter SDK version is updated, the following commands are run on the macOS:

```bash
rm -rf project
flutter create project
```

The results are then committed to the main branch.
Each commit is tagged with the corresponding Flutter SDK version number.

#### Note:
In `project/ios/Runner.xcodeproj/project.pbxproj`,`DEVELOPMENT_TEAM` setting lines are excluded from commits.

`DEVELOPMENT_TEAM` lines are automatically generated by `flutter create` based on 
the signing cerfificates in the Keychain on the macOS. If you attempt to do the same thing as this repository,
please be careful not to accidentally commit the `DEVELOPMENT_TEAM` lines.
