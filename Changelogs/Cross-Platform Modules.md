---
nav-title: Cross-Platform Modules Changelog
title: Cross-Platform Modules
description: NativeScript Cross-Platform Modules Changelog
position: 1
---

Cross Platform Modules Changelog
==============================

##1.2.1 (2015, August 18)

Fixed
=========

- [(#575)](https://github.com/NativeScript/NativeScript/issues/575) Application crashes in Android when there is an ActionBar on the first page.

- [(#576)](https://github.com/NativeScript/NativeScript/issues/576) app.css now applied when there is page-specific css.

##1.2.0 (2015, July 24)

New
=========

- [(#393)](https://github.com/NativeScript/NativeScript/issues/393) Create application.android instance immediately and move all android-specific events to application.android.

- [(#391)](https://github.com/NativeScript/NativeScript/issues/391) Implement cancellable back button pressed for Android.

- [(#304)](https://github.com/NativeScript/NativeScript/issues/304) Expose additional properties of NavBar/ActionBar

- [(#294)](https://github.com/NativeScript/NativeScript/issues/294) Add an optional fullscreen parameter to Page.showModal method.

- [(#263)](https://github.com/NativeScript/NativeScript/issues/263) Provide per page option for manipulating NavigationBar

- [(#191)](https://github.com/NativeScript/NativeScript/issues/191) Extend the set of support CSS properties in {N}

Fixed
=========

- [(#423)](https://github.com/NativeScript/NativeScript/issues/423) Showing a modal page from another modal page results in error on iOS.

- [(#422)](https://github.com/NativeScript/NativeScript/issues/422) Login dialog - iOS7: loginResult.userName returns password as a value instead of username

- [(#421)](https://github.com/NativeScript/NativeScript/issues/421) Page.showModal seems completely broken in IOS

- [(#406)](https://github.com/NativeScript/NativeScript/issues/406) Prompt dialog - iOS7: okButton returns result equal to false, cancelButton returns result equal to true

- [(#405)](https://github.com/NativeScript/NativeScript/pull/405) FPS module will now correctly count frames while scrolling in iOS

- [(#395)](https://github.com/NativeScript/NativeScript/issues/395) dialogs.action() causes app to crash on iPad

- [(#372)](https://github.com/NativeScript/NativeScript/issues/372) Simple location app doesn't perform until real gps apps are also running

- [(#368)](https://github.com/NativeScript/NativeScript/issues/368) [Screen Builder] Model is not updated when an observable object property is used in two text fields

- [(#343)](https://github.com/NativeScript/NativeScript/issues/343) Not returning a view on the view parameter of the creatingView event handler of the placeholder crash the application

- [(#322)](https://github.com/NativeScript/NativeScript/issues/322) Creating an Observable by passing a JSON object in the constructor does not define the respective properties on the Observable object instance.

- [(#285)](https://github.com/NativeScript/NativeScript/issues/285) `visibility` property inconsistent with CSS

- [(#270)](https://github.com/NativeScript/NativeScript/issues/270) BackgroundImage property does not respect the CornerRadius when set to Border.

- [(#261)](https://github.com/NativeScript/NativeScript/issues/261) WebView crash when navigating back

### Breaking changes
-  [(#304)](https://github.com/NativeScript/NativeScript/issues/304) ActionBar/NavigationBar is now defined using the `page.actionBar` instead of `page.optionsMenu`. [See an example...](../ApiReference/ui/action-bar/HOW-TO.md)

### Known issues
-  ```tns debug ios``` command is not working. The workaround is to use ```tns debug ios --framework-path "__path to the iOS runtime__"```. A fix for this is coming in 1.2.1 which will be released in the week of July, 27th.

##1.1.0 (2015, June 10)

### New
- [(#280)](https://github.com/NativeScript/NativeScript/issues/280) Change NativeActivity Pbase class in order to be compatible with Android runtime

- [(#244)](https://github.com/NativeScript/NativeScript/issues/244) Expose application level events as real events. [See an example...](https://github.com/NativeScript/NativeScript/blob/master/apps/tests/app/app.ts)

- [(#233)](https://github.com/NativeScript/NativeScript/issues/233) Application module event handlers are lacking in parameters. [See an example...](https://github.com/NativeScript/NativeScript/blob/master/apps/tests/app/app.ts)

- [(#221)](https://github.com/NativeScript/NativeScript/pull/221) view parent exposed in itemLoading event

- [(#214)](https://github.com/NativeScript/NativeScript/pull/214) Repeater component added. [Read more...](https://github.com/NativeScript/docs/blob/master/layouts.md#repeating-layout-children)

- [(#207)](https://github.com/NativeScript/NativeScript/pull/207) Optimizations

- [(#199)](https://github.com/NativeScript/NativeScript/issues/199) TabView.selectedIndexChanged event

- [(#184)](https://github.com/NativeScript/NativeScript/issues/184) Hint property for TextView

- [(#176)](https://github.com/NativeScript/NativeScript/issues/176) Implement navigatingTo, navigatedTo, navigatingFrom and navigatedFrom events on Page

### Fixed
- [(#267)](https://github.com/NativeScript/NativeScript/issues/267) SegmentedBar CSS color not applied correctly when items are bound

- [(#257)](https://github.com/NativeScript/NativeScript/pull/257) Fix some crashes for ListView's iOS UITableView

- [(#242)](https://github.com/NativeScript/NativeScript/issues/242) Cannot attach gesture observer for more than one gesture (Android).

- [(#234)](https://github.com/NativeScript/NativeScript/issues/234) DatePicker and TimePicker property bindings do not work in Android 5.x

- [(#228)](https://github.com/NativeScript/NativeScript/issues/228) ListPicker for Android shows text after bound to an empty array.

- [(#222)](https://github.com/NativeScript/NativeScript/issues/222) ListPicker showing number of items in list (Ticket938420)

- [(#196)](https://github.com/NativeScript/NativeScript/issues/196) Layout is incorrect after device rotation in iOS when there is navbar

- [(#193)](https://github.com/NativeScript/NativeScript/issues/193) Layout is broken when there is optionsMenu on the first page in iOS

- [(#189)](https://github.com/NativeScript/NativeScript/issues/189) Changing `bindingContext` affects UI elements that has a binding to `bindingContext`.

- [(#188)](https://github.com/NativeScript/NativeScript/issues/188) Remaining item when cleared page options menu in ios.

- [(#187)](https://github.com/NativeScript/NativeScript/issues/187) Custom source for UI element binding fails.

- [(#186)](https://github.com/NativeScript/NativeScript/issues/186) Using object get property syntax for binding expressions

- [(#175)](https://github.com/NativeScript/NativeScript/issues/175) Implement weak-event pattern on ListView (when bound to observable)


### Breaking changes
-  [(#242)](https://github.com/NativeScript/NativeScript/issues/242) View and GesturesObserver classes have some breaking changes related to gesture operations


##1.0.0 (2015, April 29)

### New
* New options for camera module. Added a resizing options along with keep-aspect-ratio options. More information about how to use it can be found at the dedicated camera help article.
* First-file search order changed. Now package.json is searched first, then index.js and bootstrap.js is being searched last.

### Fixed
* Taking a full size picture in Android with NativeScript camera module.
* Pages no more freeze on cancelling back-navigation via swipe gesture
* Items having verticalAlignment set to center now have correct layout bounds
* Camera for ios no more throws a Null pointer error
* iOS dialog OK button now appears last

### Breaking changes
* `image-cache` now stores native image instances, i.e. `android.graphics.Bitmap` or `UIImage`. 
* `Image.src` property is now of type `any` and can accept either a string containing an image url or a native image instance.
* Gesture related enum values changed to start with a small letter in order to be consistent with all other enums within NativeScript. For example "gesturesModule.GestureType.Tap" should be used like "gesturesModule.GestureType.tap".
* `knownEvents` modules within all UI controls are removed and replaced with a static string values. In that case all possible events will be visible through the inheritance tree. These static strings have an `Event` suffix. At every place where `viewModule.knownEvents.loaded` is used should be changed to `viewModule.View.loadedEvent` or `pageModule.Page.loadedEvent`. This change is relevant to code-behind only (xml declaration will not be affected).

##0.10.0 (2015, April 17)

### Fixed

### New

* In addition to binding converters introduced in version 0.42 static (global) place for most common converters is added. This place is named `application.resources`. More information how to use it can be found in the special help topic regarding `Data binding`.

* Using plain objects (numbers, strings also an entire object) as binding context via `$value`. More information can be found at the dedicated `Data binding` help topic.

### Breaking Changes

  * Image: `url` property renamed to `src`
  * Image: `source` property renamed to `imageSource`
  * TabView: `TabEntry` renamed to `TabViewItem`
  * Module `local-settings` changed to `application-settings`.Only the name of the module is changed (API remains the same), hence the `require` statements must be updated, i.e. `require("local-settings")` should be changed to `require("application-settings")`.

