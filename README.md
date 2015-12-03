# LCTabBarController
A amazing and highly customized tabBarController! You could almost customize 100% of the properties with LCTabBarController! 😍 ✨

![LCTabBarController](https://github.com/LeoiOS/LCTabBarController/blob/master/demo01.png)

````
In me the tiger sniffs the rose.

心有猛虎，细嗅蔷薇。
````

**[中文介绍](https://github.com/LeoiOS/LCTabBarController/blob/master/README_zh-CN.md)**



## Introduction

* Highly decoupled!
> Each control is a independent class! `-->` means "own":
>
> LCTabBarBadge --> LCTabBarItem --> LCTabBar --> LCTabBarController

* Simple integration!
> Integration takes only one step: Just replace the `UITabBarController` word in your `AppDelegate.m` with `LCTabBarController` to complete the integration!

* Non-Pollution!
> `LCTabBarController` has all the functions of `UITabBarController`, and NO any intrusion behavior!
>
> So, even if your project is complete, you could integrated at any time! You could also change back to `UITabBarController`! (But I 200% believe you won't do it!)

* Highly customized!
> You can freely set the following properties, you can also choose to modify the code directly!
>
> 1. tabBar title color
>
> 2. tabbar title font
>
> 3. tabbar image ratio
>
> 4. tabbar badge frame
>
> 5. tabbar badge font
>
> 6. ...

* If you feel good, please give me a star, thank you very much! ⭐️
> I will keep update with new Issue, if you want to know my progress at any time, please click on the `watch` button in the upper right corner!



## Installation

LCTabBarController is available on [CocoaPods](https://cocoapods.org/). Just add the following to your project Podfile:

pod "LCTabBarController"    # Podfile



## Non-CocoaPods Installation

Just drag the LCTabBarController folder into your project.



## Usage

* Inside your `AppDelegate.m`:
````objc
// Import header file
#import "LCTabBarController.h"

// 1. If you have already started the project, even if it's already done.
UITabBarController *tabBarC = [[UITabBarController alloc] init];
->
LCTabBarController *tabBarC = [[LCTabBarController alloc] init];

// 2. If you're just starting to write a new project
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    
    self.window = [[UIWindow alloc] initWithFrame:[UIScreen mainScreen].bounds];
    
    [self.window makeKeyAndVisible];
    
    // 示例代码
    HomeVC *vc1 = [[HomeVC alloc] init];
    vc1.view.backgroundColor = [UIColor whiteColor];
    vc1.tabBarItem.badgeValue = @"23";
    vc1.title = @"Home";
    vc1.tabBarItem.image = [UIImage imageNamed:@"tabbar_home"];
    vc1.tabBarItem.selectedImage = [UIImage imageNamed:@"tabbar_home_selected"];
    
    UIViewController *vc2 = [[UIViewController alloc] init];
    vc2.view.backgroundColor = [UIColor cyanColor];
    vc2.tabBarItem.badgeValue = @"1";
    vc2.title = @"Message";
    vc2.tabBarItem.image = [UIImage imageNamed:@"tabbar_message_center"];
    vc2.tabBarItem.selectedImage = [UIImage imageNamed:@"tabbar_message_center_selected"];
    
    UIViewController *vc3 = [[UIViewController alloc] init];
    vc3.view.backgroundColor = [UIColor redColor];
    vc3.title = @"Discover";
    vc3.tabBarItem.image = [UIImage imageNamed:@"tabbar_discover"];
    vc3.tabBarItem.selectedImage = [UIImage imageNamed:@"tabbar_discover_selected"];
    
    UIViewController *vc4 = [[UIViewController alloc] init];
    vc4.view.backgroundColor = [UIColor yellowColor];
    vc4.tabBarItem.badgeValue = @"99+";
    vc4.title = @"Profile";
    vc4.tabBarItem.image = [UIImage imageNamed:@"tabbar_profile"];
    vc4.tabBarItem.selectedImage = [UIImage imageNamed:@"tabbar_profile_selected"];
    
    
    UINavigationController *navC1 = [[UINavigationController alloc] initWithRootViewController:vc1];
    UINavigationController *navC2 = [[UINavigationController alloc] initWithRootViewController:vc2];
    UINavigationController *navC3 = [[UINavigationController alloc] initWithRootViewController:vc3];
    UINavigationController *navC4 = [[UINavigationController alloc] initWithRootViewController:vc4];
    
    
    
    /**************************************** Key Code ****************************************/

    LCTabBarController *tabBarC = [[LCTabBarController alloc] init];

    tabBarC.viewControllers = @[navC1, navC2, navC3, navC4];

    self.window.rootViewController = tabBarC;

    /******************************************************************************************/
    
    
    
    return YES;
}
````

* Done!

* You can change the following properties in `LCTabBarCONST.h/.m`, other more attributes can be directly read code changes!
````objc
#define LC_TABBAR_ITEM_TITLE_COLOR      // tabBar 标题字体颜色
#define LC_TABBAR_ITEM_TITLE_COLOR_HL   // tabBar 标题字体颜色 (高亮)

const CGFloat LCTabBarItemImageRatio     = 0.70f;   // tabBar 图片所占比例
const CGFloat LCTabBarItemTitleFontSize  = 10.0f;   // tabBar 标题字体大小
const CGFloat LCTabBarBadgeTitleFontSize = 11.0f;   // tabBar badge 字体大小
````



## Example

![LCTabBarController](https://github.com/LeoiOS/LCTabBarController/blob/master/demo01.png)
---
![LCTabBarController](https://github.com/LeoiOS/LCTabBarController/blob/master/demo02.png)
---
![LCTabBarController](https://github.com/LeoiOS/LCTabBarController/blob/master/demo03.png)
---
![LCTabBarController](https://github.com/LeoiOS/LCTabBarController/blob/master/demo04.png)



## Support

If you have any questions, please commit a [Issues](https://github.com/LeoiOS/LCTabBarController/issues/new)! Thx!
Email: liucsuper@gmail.com & leoios@sina.com
Blog: http://www.leodong.com



## License

[MIT License](http://opensource.org/licenses/MIT)



