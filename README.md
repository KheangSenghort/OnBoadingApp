# OnBoadingApp
A iOS onboarding component to add easily on your project.

![[Watch Demo](https://www.youtube.com/watch?v=DqP-kihCRco)](https://img.youtube.com/vi/DqP-kihCRco/0.jpg)

# Requirements
`OS X 10.15.5+`
`Xcode 11.5 or above`

# Usage
Drag and drop ***Introductions and Common*** folder on your app.
For this example, ensure 3 pngs exist (provided in the example repo) in the project's asset catalog, in this case 1.png, 2.png and 3.png

Use the following code in your AppDelegate.swift or similar.

```
  func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
               let isFirst = UserDefaults.standard.bool(forKey:"FirstTimecome" )
               if  !isFirst
               {
                   UserDefaults.standard.set(true, forKey: "FirstTimecome")
                   let mGetStartedVC = GetStartedVC(nibName: "GetStartedVC", bundle: nil)
                   let navigationController = UINavigationController(rootViewController: mGetStartedVC)
                   self.window!.rootViewController = navigationController
               }
        
        guard let _ = (scene as? UIWindowScene) else { return }
    }
```

# License
This software is Open Source under the MIT license, see LICENSE for details.
