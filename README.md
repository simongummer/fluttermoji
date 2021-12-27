

//TEST

# fluttermoji  <img src="https://user-images.githubusercontent.com/37346450/103101129-1b9a2100-463c-11eb-8a94-b6fbe44bf00f.png" align="right" height="150" />
![Pub Version](https://img.shields.io/pub/v/fluttermoji) [![Generic badge](https://img.shields.io/badge/demo-LIVE-green.svg)](https://psk907.github.io/fluttermoji/) [![GitHub stars](https://img.shields.io/github/stars/psk907/fluttermoji?style=social)](https://github.com/psk907/fluttermoji/stargazers) [![GitHub stars](https://img.shields.io/badge/DM-me-blue?style=flat&logo=telegram)](https://t.me/psk907)

A light-weight and highly customizable SVG graphic set for Flutter, which provides a Customizer Widget, CircleAvatar and other utility functions.

This package provides you two easy-to-use widgets -

| Name | Description | Screenshot | 
|--------|----------|---------- |
|FluttermojiCircleAvatar | Use your fluttermoji anywhere in your Flutter app with a simple customizable widget. Supports material dark theme too.| ![1608830483994](https://user-images.githubusercontent.com/37346450/103071632-009ec100-45ea-11eb-97c4-96c9ec67e204.gif)
|FluttermojiCustomizer | A complete personalization suit that offers previews of each individual component and a modern UI with material light and dark theme support.|![1608827561239](https://user-images.githubusercontent.com/37346450/103100686-c0ffc580-4639-11eb-9fc9-9fe5c0bf7dcc.jpg)

Use the given utility functions to send and receive Fluttermoji data from your server/DB efficiently.

| Function Prototype | Description | 
|------------------|---------------|
|String decodeFluttermojifromString(String encodedData)| Decode your string containing the attributes to a SVG and render it by enclosing this string with a SvgPicture.string() | 
| Future\<Map> encodeMySVGtoMap() | Retrieve the local user's fluttermoji attributes from local storage and encodes them to a Map of attributes and returns a Future, you have to await on function call. |
|Future\<String> encodeMySVGtoString() | Retrieve the local user's fluttermoji attributes from local storage and encodes them to a String containing a map of attributes and returns a Future, you have to await on function call. | 
| Future<List<bool>> clearFluttermoji() | Erase fluttermoji String and Map from local storage |
	
SVG Assets used are derived from [getavataaars.com](https://getavataaars.com/) .

## Screenshots
###  Example app
<a href="https://psk907.github.io/fluttermoji" >Try out the demo on your browser now</a>
<br />
<br />
<img src="https://user-images.githubusercontent.com/37346450/103443014-fd0dd880-4c80-11eb-8955-309bfb66fb4c.jpg" height ="400" />
<img src="https://user-images.githubusercontent.com/37346450/103443015-fed79c00-4c80-11eb-8219-5edab76c9f0f.jpg" height="400" />
<img src="https://user-images.githubusercontent.com/37346450/103443018-01d28c80-4c81-11eb-8336-ebc19de61220.jpg" height="400" />

**Use them in your games or social media apps**

<a href="https://play.google.com/store/apps/details?id=com.statefullyfidgeting.tugofwar" ><img src="https://user-images.githubusercontent.com/37346450/103443017-00a15f80-4c81-11eb-8223-3404a35079aa.jpg" height="400" /></a>

## Usage Instructions
1. Depend on it by importing your package in the ```pubspec.yaml```  file.
	```yaml
	dependencies:
          fluttermoji: latest_version
	```
2. Add the following import to your .dart file
	```dart
	import 'package:fluttermoji/fluttermoji.dart';
	```
3. Add the FluttermojiCircleAvatar widget to display your Fluttermoji where needed.
	```dart
	FluttermojiCircleAvatar();
	```
4. To allow your users to personalize their Fluttermoji, add the following widget and pair it with the above one in your page.
	```dart
	FluttermojiCustomizer();
	```

That's all it takes, simple right ? The two widgets communicate with each other and update in real-time throughout your widget tree.

##  Usage Guidelines
The package offers a ton of features in the simplest way possible, however there are some points worth noting.

- FluttermojiCircleAvatar would render an avatar with the default set of options until customized and saved by the user.
- FluttermojiCustomizer updates the preview in real-time however changes must be saved by tapping the Save icon built into the widget itself.
- Use the `canvaskit` renderer when building for web, the default `html` renderer will not work with SVGs.
- The fluttermoji's attributes are saved to local app/browser storage. Clearing app/browser data would mean clearing these attributes as well.
- FluttermojiCustomizer uses a Scaffold whose height is set to _0.4*screen height_ by default, if you do not pass a value to the ```scaffoldHeight``` property make sure to place the widget properly.
- If you plan on using FluttermojiCustomizer in Landscape mode, manually pass in the desired width for the widget in the ```scaffoldWidth``` property.

## Attributions

- SVG assets from [Fang-Pen Lin](getAvataars.com)'s  [GitHub repository](https://github.com/fangpenlin/avataaars-generator)
- Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a>
- Animated [GIF](https://user-images.githubusercontent.com/37346450/103071632-009ec100-45ea-11eb-97c4-96c9ec67e204.gif) designed by [Reesha Shenoy](https://github.com/reeshaa) 

## Community
If you find any issues or have some feedback, please raise the same on the GitHub repo or contact me directly.
Share your creative implementation of Fluttermoji with me and I might feature them on this page.
Do leave a thumbs up if you liked it.


**Happy Fluttering ; )**
