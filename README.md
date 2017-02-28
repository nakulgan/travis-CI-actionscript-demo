# Travis-CI ActionScript Demo

[![Build Status](https://travis-ci.org/nakulgan/travis-CI-actionscript-demo.svg?branch=flexmojos4.0)](https://travis-ci.org/nakulgan/travis-CI-actionscript-demo)

A simple demo that demonstrates a way to unit test [ActionScript](http://en.wikipedia.org/wiki/ActionScript) applications with [Travis CI](http://travis-ci.org)

## About
The demo utilizes OSX Travis worker.  A specified [Flash Player](http://www.adobe.com/products/flashplayer.html) will be downloaded from the Adobe website at runtime. All build dependencies (flex sdk, flex unit, etc) will be resolved by [Maven](http://maven.apache.org/) and the [flex-mojos](http://code.google.com/p/flex-mojos/) plug-in.

## Example Details

### Flex-Mojos 4.0
  * needs Maven 3.2 or 3.5
  * needed to compile FlexSDK 4.5
  * used FlexUnit 4.0
  * needs a Flash Player work around
  * aided by this Adobe tutorial - [Part 1](http://www.adobe.com/devnet/flex/articles/flex-maven-flexmojos-pt1.html), [Part 2](http://www.adobe.com/devnet/flex/articles/flex-maven-flexmojos-pt2.html)

:blue_book: See _travis.ci_ and _pom.xml_ files for setup details.

## Local Usage
To run this script locally you will need a Mac, the OSX version should ideally match the [Travis OSX build environment](http://docs.travis-ci.com/user/osx-ci-environment).

Clone the GitHub repo. Pull the Tags, and checkout the example you want.

Get Maven (if you don't have it already).

```
brew install maven
```

Download a _Debug Flash Player_ via **getFpFromArchive** script from the [list of Adobe Archives](http://helpx.adobe.com/flash-player/kb/archived-flash-player-versions.html).  
(This 
player is only used when running Maven and will not alter your computers setup.)

```
sh getFpFromArchive 'http://download.macromedia.com/pub/flashplayer/installers/archive/fp_11.7.700.225_archive.zip'
```

Run Maven **test**.  
(the _flashplayer_ environemnt variable is set which is used in the _pom.xml_ file.

```
mvn test -DflashPlayer.command=Flash\ Player\ Debugger.app/Contents/MacOS/Flash\ Player\ Debugger
```

## Resources

 * [Flex-Mojos (Pre-Apache Flex)](http://code.google.com/p/flex-mojos/)
 * [Flex-Mojos Introduction](https://github.com/justinjmoses/flexmojos-introduction)

## Authors

 * Manfred Endres
 * Hays Clark
 
