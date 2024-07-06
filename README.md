# expo-bug

Good afternoon! I hope you can review and fix this issue. When building an android, an incorrect one is generated AndroidManifest.xml config. You can view it in the android/app/src/main folder. It is worth paying attention to the fact that there are two <data> attributes in one intentfilter and the latter overrides all the above options. This only happens on android. It would be great to split this into 2 intent-filters with different <data> attributes. To verify my statement, you can run the application on android and use the adb utility: "adb shell am start -W -a android.intent.action.VIEW -d"https://some.domain/profile/123 "". In my case, despite the verified domain
![Изображение](image.png)

