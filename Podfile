use_frameworks!
platform :ios, '12'
target 'TestApp' do
    pod 'FMDB'
    pod 'iCarousel'
    pod 'FBSDKCoreKit'
    pod 'FRHyperLabel', '~> 1.0.4'
    pod 'MBProgressHUD', '~> 1.2.0'
    pod 'Reachability', '~> 3.2'
    pod 'IQKeyboardManager'
    pod 'AFNetworking', '~> 4.0'
    pod 'SVPullToRefresh'
    pod 'HCSStarRatingView'
    pod 'SDWebImage'
    pod 'Somo'
    pod 'Firebase/Performance', '7.7'
    pod 'Firebase/RemoteConfig'
    pod 'Firebase/Analytics'
    pod 'Firebase/Messaging'
    pod 'Firebase/Crashlytics'
    pod 'GoogleMaps'
    pod 'GoogleAnalytics'
    pod 'FLAnimatedImage'
    pod 'SpreadsheetView'
    pod 'Charts', '~> 3.6'
    pod 'DZNEmptyDataSet'
    pod 'Eureka'
    pod 'PanModal'

# Keep Freestar up to date with the latest released versions here:
# https://github.com/freestarcapital/SDK_documentation_iOS/wiki/FreeStar-Ads-Mediation-Swift-iOS

    pod 'FreestarAds', '~> 3.6'
    pod 'FreestarAds-AppLovin', '~> 3.2'
    pod 'FreestarAds-Googleadmob', '~> 2.2'
    pod 'FreestarAds-Unity', '~> 4.1'
    pod 'FreestarAds-Vungle', '~> 3.1'
    pod 'FreestarAds-Amazon', '~> 2.1'
    pod 'FreestarAds-Google', '~> 3.0'
    pod 'FreestarAds-GAM', '~> 1.0'
    pod 'FreestarAds-Facebook', '~> 3.1'
    pod 'FreestarAds-Nimbus', '~> 1.0'
    target 'TestAppTests' do
      inherit! :search_paths
      # Pods for testing
    end
end
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      # some pods set 8.0 deployment target but Xcode 12 requires 9
      config.build_settings.delete 'IPHONEOS_DEPLOYMENT_TARGET'
      # some pods set conflicting values for this (looking at you, Vungle)
      config.build_settings['EXCLUDED_ARCHS[sdk=iphonesimulator*]'] = "arm64"
      # No longer used as of Xcode 12 - not sure this works ...
      config.build_settings.delete 'VALID_ARCHS'
    end
  end
end
