# iOSHelloWorld

In this tutorial, you will create a vector drawing app based on TouchVG. See [touchvg/Readme.txt](touchvg/Readme.txt) to copy files required to compile.

- Create a project with the `Single View Application` wizard.

- Add the libraries and header files of TouchVG to this project.

   - `cd' to the 'ios' directory of the [TouchVGTest](https://github.com/touchvg/TouchVGTest) project.
   - Type `./build.sh` or `./build.sh -arch arm64` to compile libraries outputed to the `ios/output` directory.
   - Add `TouchVG`, `TouchVGCore`, `libTouchVG.a` and `libTouchVGCore.a` to this project.
   - Change 'Library Search Paths' of the HelloWorld target from '.../iOSHelloWorld/touchvg' to the relative path 'touchvg'.

- Add `QuartzCore.framework` and `libc++.dylib` in 'Link Binary With Libraries' of the target.

   - Add libc++.dylib for ViewController.m or change ViewController.m to ViewController.mm to use Obj-C++ classes of TouchVG.

- Add a vector drawing view in ViewController.mm/.m:

   - Add `#import "GiViewHelper.h"` to use `helper = [GiViewHelper sharedInstance]`.
   - Add a drawing view in self.view via `[helper createGraphView:self.view.bounds :self.view];`.
   - Start the free-hand splines command via `helper.command = @"splines";`. The names of all commands will be printed in logging after the app runs.

<<<<<<< HEAD
- Enjoy the simple drawing app now!
=======
- Enjoy the simple drawing app now! You can fork this project and add drawing UI  reference to [ColorPad wizard](http://www.raywenderlich.com/18840/how-to-make-a-simple-drawing-app-with-uikit).
>>>>>>> ae4931e40fb8414ad2675b61fba2f143265f029e
