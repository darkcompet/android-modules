# Android Modules


## How this project was made

- Create new project with: package name `compet.bundle`, min api 21, Kotlin, empty activity.

- At android studio, create default product flavor.

	```bash
	# Create resource folders
	Right click on `app` folder and choose `New -> Folder -> Res Folder`.

	# Create flavor with package name as `compet.gpscompass`
	- Select `Build -> Edit Flavors -> Build Variants -> app`
	- Add flavor dimension `defaultDimension`
	- Add product flavor `defaultFlavor`, and fill with below info:
		- Application id: `compet.sampleapp`
		- Version code: 1
		- Version name: 1.0.0
		- Target SDK version: 31
		- Min SDK version: 21
	
	# At `src` folder, create new empty activity at `defaultFlavor` to tell android studio
	# generate `defaultFlavor` folder for us.
	- Right click to `app` -> Select `New -> Activity -> Empty Activity`
	```

- Add darkcompet support modules

	```bash
	# Init git
	git init

	# At android modules
	git submodule add https://github.com/darkcompet/android-module-animation.git
	git submodule add https://github.com/darkcompet/android-module-appcompat.git
	git submodule add https://github.com/darkcompet/android-module-boommenu.git
	git submodule add https://github.com/darkcompet/android-module-bottomsheet.git
	git submodule add https://github.com/darkcompet/android-module-compactview.git
	git submodule add https://github.com/darkcompet/android-module-compassview.git
	git submodule add https://github.com/darkcompet/android-module-constraintlayout.git
	git submodule add https://github.com/darkcompet/android-module-core.git
	git submodule add https://github.com/darkcompet/android-module-database.git
	git submodule add https://github.com/darkcompet/android-module-floatingbar.git
	git submodule add https://github.com/darkcompet/android-module-gesturedetector.git
	git submodule add https://github.com/darkcompet/android-module-googleauth.git
	git submodule add https://github.com/darkcompet/android-module-googlebilling.git
	git submodule add https://github.com/darkcompet/android-module-googlelocation.git
	git submodule add https://github.com/darkcompet/android-module-googlemap.git
	git submodule add https://github.com/darkcompet/android-module-http.git
	git submodule add https://github.com/darkcompet/android-module-imgproc.git
	git submodule add https://github.com/darkcompet/android-module-json.git
	git submodule add https://github.com/darkcompet/android-module-mvc.git
	git submodule add https://github.com/darkcompet/android-module-network.git
	git submodule add https://github.com/darkcompet/android-module-navigation.git
	git submodule add https://github.com/darkcompet/android-module-preferenceview.git
	git submodule add https://github.com/darkcompet/android-module-location.git
	git submodule add https://github.com/darkcompet/android-module-livedata.git
	git submodule add https://github.com/darkcompet/android-module-recyclerview.git
	git submodule add https://github.com/darkcompet/android-module-reflection.git
	git submodule add https://github.com/darkcompet/android-module-graphics.git
	git submodule add https://github.com/darkcompet/android-module-security.git
	git submodule add https://github.com/darkcompet/android-module-storage.git
	git submodule add https://github.com/darkcompet/android-module-showcaseview.git
	git submodule add https://github.com/darkcompet/android-module-stream.git
	git submodule add https://github.com/darkcompet/android-module-sensor.git
	git submodule add https://github.com/darkcompet/android-module-tooltip.git
	git submodule add https://github.com/darkcompet/android-module-topic.git
	git submodule add https://github.com/darkcompet/android-module-view.git

	# Import modules by add below lines to `settings.gradle` file
	include ':android-module-animation'
	include ':android-module-appcompat'
	include ':android-module-boommenu'
	include ':android-module-bottomsheet'
	include ':android-module-compactview'
	include ':android-module-compassview'
	include ':android-module-constraintlayout'
	include ':android-module-core'
	include ':android-module-database'
	include ':android-module-floatingbar'
	include ':android-module-gesturedetector'
	include ':android-module-googleauth'
	include ':android-module-googlebilling'
	include ':android-module-googlelocation'
	include ':android-module-googlemap'
	include ':android-module-http'
	include ':android-module-imgproc'
	include ':android-module-json'
	include ':android-module-mvc'
	include ':android-module-network'
	include ':android-module-navigation'
	include ':android-module-preferenceview'
	include ':android-module-location'
	include ':android-module-livedata'
	include ':android-module-recyclerview'
	include ':android-module-reflection'
	include ':android-module-graphics'
	include ':android-module-security'
	include ':android-module-storage'
	include ':android-module-showcaseview'
	include ':android-module-stream'
	include ':android-module-sensor'
	include ':android-module-tooltip'
	include ':android-module-topic'
	include ':android-module-view'

	# And at `app/build.gradle`, declare modules which project needs, for eg:
	implementation project(path: ':android-module-animation')
	implementation project(path: ':android-module-appcompat')
	implementation project(path: ':android-module-boommenu')
	implementation project(path: ':android-module-bottomsheet')
	implementation project(path: ':android-module-compactview')
	implementation project(path: ':android-module-compassview')
	implementation project(path: ':android-module-constraintlayout')
	implementation project(path: ':android-module-core')
	implementation project(path: ':android-module-database')
	implementation project(path: ':android-module-floatingbar')
	implementation project(path: ':android-module-gesturedetector')
	implementation project(path: ':android-module-googleauth')
	implementation project(path: ':android-module-googlebilling')
	implementation project(path: ':android-module-googlelocation')
	implementation project(path: ':android-module-googlemap')
	implementation project(path: ':android-module-http')
	implementation project(path: ':android-module-imgproc')
	implementation project(path: ':android-module-json')
	implementation project(path: ':android-module-mvc')
	implementation project(path: ':android-module-network')
	implementation project(path: ':android-module-navigation')
	implementation project(path: ':android-module-preferenceview')
	implementation project(path: ':android-module-location')
	implementation project(path: ':android-module-livedata')
	implementation project(path: ':android-module-recyclerview')
	implementation project(path: ':android-module-reflection')
	implementation project(path: ':android-module-graphics')
	implementation project(path: ':android-module-security')
	implementation project(path: ':android-module-storage')
	implementation project(path: ':android-module-showcaseview')
	implementation project(path: ':android-module-stream')
	implementation project(path: ':android-module-sensor')
	implementation project(path: ':android-module-tooltip')
	implementation project(path: ':android-module-topic')
	implementation project(path: ':android-module-view')
	```
