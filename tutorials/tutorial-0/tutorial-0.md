# Tutorial 0: Intro to UIKit

Please leave feedback by creating a GitHub issue or by posting on Piazza.

Watch [this](https://www.youtube.com/watch?v=bZNAFkkUeKs&ab_channel=Devslopes) video for a basic demonstration of how to build an app like this and [this](https://www.youtube.com/watch?v=JX2DLrT_FC4&ab_channel=JerryYe) video for some intro theory. Remember -- Stack Overflow and Google are strongly encouraged as well. If you can't get this tutorial working after 30 minutes, quit. You will be graded on submitting something, not whether it's working or not. At the very least, spend a few minutes playing around with XCode.  

<img src="https://github.com/jerry1ye10/cis-195-f20/blob/master/tutorials/tutorial-0/assets/pic1.png" width="300" height="500"/> <img src="https://github.com/jerry1ye10/cis-195-f20/blob/master/tutorials/tutorial-0/assets/pic2.png" width="300" height="500"/>




## Step 0: Create a new project
* Open Xcode
* Select "new project" from the start screen, or use File > New > Project in the menu bar
* Select "Single View Application"
* Name the project "app0_lastname_firstname"
* Make sure you select storyboard as the User Interface 
## Step 1: Build the storyboard 
* Go to the storyboard
* Drag a `UIButton` and a `UILabel` into your view
## Step 2: Add the logic
* Connect both your button and your label to your designated view controller 
* Make your button change the `text` of the label whenever it's clicked. To change the text of the button run something like this: `button.setTitle("Turn Blue", for:.normal)`
* For extra credit change the color of the `UILabel` to reflect the color of the word at the time

# Part 2: UIView Lifecycle methods
No submission is required for this part of the tutorial. Be prepared to discuss it in class. 
## View Controller Life Cycle

![](/tutorials/tutorial-1/assets/fig1.png?raw=true)

Any non-trivial iPhone app will have multiple screens. Those screens may appear and disappear many times while the app is running. It's important to "hook in" to this life cycle, and perform specific actions at specific times.

For example: when the view loads, we may want to make an API request. When the view appears, we may want to play an animation to welcome the user.

In general, you'll use the "Life Cycle" methods heavily to control your app.

Read: [Understand the View Controller Lifecycle](https://developer.apple.com/library/content/referencelibrary/GettingStarted/DevelopiOSAppsSwift/WorkWithViewControllers.html). Stop at “Add a Meal Photo.”

Watch from 00:00 to 10:00: [Stanford - View Controller Life Cycle](https://www.youtube.com/watch?v=tLsPoVDXDG8&list=PLPA-ayBrweUzGFmkT_W65z64MoGnKRZMq&index=10)

*Optional reading: Similarly, apps have a life cycle too. Certain events happen to every app: app gets opened, app finished loading, app exited etc. [This article](https://medium.com/@neroxiao/ios-app-life-cycle-ec1b31cee9dc) describes the possible states your app can flow through. Don't worry if you don't understand everything on these diagrams - they're quite dense.*

![](/tutorials/tutorial-1/assets/fig2.png?raw=true)

You should understand the following:
* Apps have a predicted life cycle, governed by the different methods inside `AppDelegate`.
* View Controllers have a predicted life cycle, governed by the different life cycle methods in that view controller. Why is this important? You will want to make certain things happen in your app that will be require the view to be loaded, the view to actually appear (make sure you understand the distinction), disappear etc. **Having a firm grasp of this life cycle will make you write less buggy code, and make debugging much easier.**
* The life cycle methods provide predictable structure that stems directly from the way the iPhone loads and renders applications. These methods were provided to give iOS apps a way to react to "hook into" milestones in the life of the program.

### Do the following
* Open Xcode and create a new Single View Application. Name it whatever you like.
* Open `ViewController.swift` and examine the methods that were automatically included in the file.
* Add the missing lifecycle methods (not yet included) to `ViewController.swift` and place a **breakpoint** and a **print statement** with the function signature inside of each one (e.g. `print(“viewDidLoad()”)`). Breakpoints can be placed by clicking the code line number where you want the program to pause. More information [here](https://medium.com/yay-its-erica/xcode-debugging-with-breakpoints-for-beginners-5b0d0a39d711).
* Run your app in a simulator, continue between the breakpoints and examine the console output.
* Record the order in which the life cycle methods were called.
* Think about the differences between each of the differing life cycle methods. Give an example of when you might use each one. (HINT: check out [this link](https://www.codementor.io/hemantkumar434/view-controller-lifecycle-ios-applications-7oyju9lp6) if you’re having trouble, which explains these methods in layman's terms.)
* Again, be prepared to discuss in class.

---
