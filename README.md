# Introduction

[https://github.com/arundavidp/tictactoe/blob/d24a0da67150be19bb59e45a1234bda060cc874a/lib/main.dart#L38](https://github.com/arundavidp/tictactoe/blob/d24a0da67150be19bb59e45a1234bda060cc874a/lib/main.dart#L38)

It is the starting function of the app



\---



[https://github.com/arundavidp/tictactoe/blob/d24a0da67150be19bb59e45a1234bda060cc874a/lib/main.dart#L39-L50](https://github.com/arundavidp/tictactoe/blob/d24a0da67150be19bb59e45a1234bda060cc874a/lib/main.dart#L39-L50)

A FirebaseCrashlytics object is created as nullable object.\
If the app running platform is mobile (ios, android), and it is not run in a webview, then the crashlytics object declared is initialized in try catch block.\
In the try block, initially the Firebase itself is initialized after calling the ensureInitialized method on WidgetsFlutterBinding class.\
After Firebase is initialized then the FirebaseCrashlytics class instance is assigned to the variable crashlytics, thus it represents the FirebaseCrashlytics object to be used in the app.\
If any of the steps fail, the catch block is called, and the error message is printed.



\---



[https://github.com/arundavidp/tictactoe/blob/8366457f89e210892ee6da86379135094798503c/lib/main.dart#L52-L55](https://github.com/arundavidp/tictactoe/blob/8366457f89e210892ee6da86379135094798503c/lib/main.dart#L52-L55)

guardWithCrashlytics function is called passing the guardedMain function, and the nullable crashlytics object. The guardWithCrashlytics function is intended to log all errors caught while running the app in the Firebase Crashlytics service. This helps the developer to later check what errors occurred when users where using the app.
