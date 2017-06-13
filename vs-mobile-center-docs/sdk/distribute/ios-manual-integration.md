---
title: Mobile Center Distribute for iOS
description: Using in-app updates in Mobile Center Distribute
keywords: sdk, distribute
author: elamalani
ms.author: emalani
ms.date: 06/08/2017
ms.topic: article
ms.assetid: f91fcd0b-d5e6-4c74-89a8-f71c2ee57566
ms.service: mobile-center
ms.custom: sdk
ms.tgt_pltfrm: ios
---

# Mobile Center Distribute – In-app updates

> [!div class="op_single_selector"]
> * [Android](android.md)
> * [iOS](ios.md)
> * [Xamarin](xamarin.md)

If you don't want to use Cocoapods, you can integrate the modules by copying the binaries into your project. Follow the steps below:

1. Download the [Mobile Center iOS SDK](https://github.com/Microsoft/MobileCenter-SDK-iOS/releases) frameworks provided as a zip file.

2. Unzip the file and you will see a folder called `MobileCenter-SDK-iOS` that contains different frameworks for each Mobile Center service. The framework called `MobileCenter` is required in the project as it contains code that is shared between the different modules.

3. [Optional] Create a subdirectory for 3rd-party-libraries.
    * As a best practice, 3rd-party libraries usually reside inside a subdirectory (it is often called **Vendor**), so if you don't have your project organized with a subdirectory for libraries, create a **Vendor** subdirectory now.
    * Create a group called **Vendor** inside your Xcode project to mimic your file structure on disk.

4. Open Finder and copy the unzipped `MobileCenter-SDK-iOS` folder into your project's folder at the location where you want it to reside.

5. Add the SDK framework to the project in Xcode:
    * Make sure the Project Navigator is visible (⌘+1).
    * Now drag and drop `MobileCenter.framework`, `MobileCenterDistribute.framework` and `MobileCenterDistributeResources.bundle` from the Finder (the ones inside the **Vendor** folder) into Xcode's Project Navigator. Note that `MobileCenter.framework` is required to start the SDK, make sure it is added to your project, otherwise the other modules will not work and your project will not compile successfully.
    * A dialog will appear, make sure your app target is checked. Then click **Finish**.