# New Relic Video Agent for iOS & tvOS


The New Relic Video Agent for iOS & tvOS contains multiple modules necessary to instrument video players and send data to New Relic.

## Modules

There are two modules available:

### NewRelicVideoCore

Contains all the base classes necessary to create trackers and send data to New Relic. It depends on the New Relic Agent.

### NRAVPlayerTracker

The video tracker for AVPlayer player. It depends on NewRelicVideoCore.

## Build & Setup

### Install automatically using Cocoapods

Add the following lines to your Podfile:

```
  pod 'NewRelicVideoCore', :git => 'https://github.com/newrelic/video-agent-iOS'
  pod 'NRAVPlayerTracker', :git => 'https://github.com/newrelic/video-agent-iOS'
```

### Install manually

First install the [New Relic iOS Agent](https://docs.newrelic.com/docs/mobile-monitoring/new-relic-mobile-ios/installation/ios-manual-installation).

1. Clone this repo.
2. Open each one of the .xcodeproj files with Xcode.
3. Select the appropiate scheme.
4. Build (cmd+B).
5. Include the generated .framework in your project.

## Documentation

To generate source code documentation, you can use [appledoc](https://github.com/tomaz/appledoc) as follows:

```bash
appledoc --project-name NewRelicVideoAgent --project-company "New Relic Inc." --company-id com.newrelic --create-html --no-create-docset --output ./docs NewRelicVideoCore/NewRelicVideoCore/**/*.h
```

And then open `docs/html/index.html` with your prefered browser.

You can also read the [tutorial](tutorial.md).

## Examples

The `Examples` folder contains all the usage examples.
