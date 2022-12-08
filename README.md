# Introduction

[https://github.com/arundavidp/tictactoe/blob/3bde9313ef29d3d11c83c1332fbd339c72f65694/lib/main.dart#L38](https://github.com/arundavidp/tictactoe/blob/3bde9313ef29d3d11c83c1332fbd339c72f65694/lib/main.dart#L38)

It is the starting function of the app

***

[https://github.com/arundavidp/tictactoe/blob/3bde9313ef29d3d11c83c1332fbd339c72f65694/lib/main.dart#L39-L50](https://github.com/arundavidp/tictactoe/blob/3bde9313ef29d3d11c83c1332fbd339c72f65694/lib/main.dart#L39-L50)

A FirebaseCrashlytics object is created as nullable object.\
If the app running platform is mobile (ios, android), and it is not run in a webview, then the crashlytics object declared is initialized in try catch block.\
In the try block, initially the Firebase itself is initialized after calling the ensureInitialized method on WidgetsFlutterBinding class.\
After Firebase is initialized then the FirebaseCrashlytics class instance is assigned to the variable crashlytics, thus it represents the FirebaseCrashlytics object to be used in the app.\
If any of the steps fail, the catch block is called, and the error message is printed.

***

[https://github.com/arundavidp/tictactoe/blob/3bde9313ef29d3d11c83c1332fbd339c72f65694/lib/main.dart#L52-L55](https://github.com/arundavidp/tictactoe/blob/3bde9313ef29d3d11c83c1332fbd339c72f65694/lib/main.dart#L52-L55)

guardWithCrashlytics function is called passing the guardedMain function, and the nullable crashlytics object. The guardWithCrashlytics function is intended to log all errors caught while running the app in the Firebase Crashlytics service. This helps the developer to later check what errors occurred when users where using the app.

The typical main function in flutter apps (which calls the runApp function) is guardedMain here, and it is passed to guardWithCrashlytics function as a callback.

The guardWithCrashlytics function will call the guardedMain function from its body.



GoRouter is used to define the root widget to render on startup, and the widgets for different paths which are accessed with context.go() method.

[https://github.com/arundavidp/tictactoe/blob/c7daf196de48fc06c11bcb1dceb976a7f4a07157/concepts/gorouter.md#L1-L5](https://github.com/arundavidp/tictactoe/blob/c7daf196de48fc06c11bcb1dceb976a7f4a07157/concepts/gorouter.md?plain=1#L1-L5)

GoRouter concept file
