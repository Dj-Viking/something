# Learning Swift

---

* 3/3/2022
  - trying to learn how to code swift. Ran into some compatibility issues with a example swiftui project had to use `objectVersion: 52` set in the project.pbxproj file, which apparently enumerates to xcode version 11.3.1 which is what is installed on my catalina machine.
  - the project starts, but I cannot choose a simulator for it for some reason, could be a compatibility issue there also
  - Started a brand new project to see if I can get a build. and it works, while streaming the simulator took a few minutes to start. which seems to be normal from what I have seen. 

  - My idea is to try and port over the map project that Crystal Knight worked on for the ios devs meetup. to get it to build on my machine. I am currently hesitant to upgrade my machine to big sur to run xcode 12+ because of possible backwards compatibility issues with ableton live and other software that I frequently use. 
  - And then eventually try to build an application that is a clone of touchOSC just to see if I can build it myself and learn how that works. 

---

* 3/5/2022
  - Figured out what the issue was trying to build the example project. I needed to install xcode version 12.4 to at least compile the version of swift code inside the project. (Which the Swift compiler version seems to be 5 in xcode 12.4)
  - Even so, some of the styles I had to use an invoked struct (at least i think that is what it is called) for .tabViewStyle(PageTabViewStyle()) like so. Because doing `.tabViewStyle(.page)` is most likely not available for the version of swift that I have. some docs have the latter example and other docs have the former example. The former example works for my situation at the moment.
  - Also some of the SF icons were not available to me like globe.americas for some reason, probably another version issue, even after downloading the SF Icons dmg and installing them, still not available, just chose different icons that were available to me. Not having the icons resulted in runtime errors
  - Also upon installing the correct Xcode version I had to go to xcodeproj file and change the iOS deployment targets to let the compiler know what hardware the compiler is targeting and so the simulator can simulate this hardware.  
  - <a href="https://swiftontap.com/" rel="noopener noreferrer">SwiftUI docs that helped me with the .page and .stack style issues</a>
