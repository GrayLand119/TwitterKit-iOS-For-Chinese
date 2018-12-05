**Twitter will be discontinuing support for Twitter Kit on October 31, 2018. [Read the blog post here](https://blog.twitter.com/developer/en_us/topics/tools/2018/discontinuing-support-for-twitter-kit-sdk.html).**

# Twitter Kit for iOS

This branch resloved the issue "Failed to connect to ton.twimg.com port 443: Connection" with Chinese user. 

# CocoaPod

```ruby
    pod 'TwitterCore', :podspec => 'https://raw.githubusercontent.com/GrayLand119/twitter-kit-ios/master/TwitterCore/TwitterCore.podspec'
    pod 'TwitterKit', :podspec => 'https://raw.githubusercontent.com/GrayLand119/twitter-kit-ios/master/TwitterKit/TwitterKit.podspec'
```

# Carthage

To install Twitter Kit for iOS using Carthage, add the following lines to your Cartfile. For more information about how to set up Carthage and your Cartfile, see[here](https://github.com/Carthage/Carthage).

```ruby
binary "https://raw.githubusercontent.com/GrayLand119/twitter-kit-ios/master/TwitterCore.json"
binary "https://raw.githubusercontent.com/GrayLand119/twitter-kit-ios/master/TwitterKit.json"
```

After running`carthage update`, add`TwitterKit.framework`and`TwitterShareExtensionUI.framework`to the`Linked Frameworks and Binaries`section under General of your App target. In addition to that, make sure that when you are adding the copy-frameworks run script for Carthage that you add the following input paths:

$(SRCROOT)/Carthage/Build/iOS/TwitterCore.framework
$(SRCROOT)/Carthage/Build/iOS/TwitterKit.framework

Optional:
$(SRCROOT)/Carthage/Build/iOS/TwitterShareExtensionUI.framework

Make sure that the run script phase is after your Link Binaries with Libraries phase to prevent issues with properly archiving your iOS application.

## License

Copyright 2017 Twitter, Inc.
Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0
