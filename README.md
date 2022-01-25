# Dojo cupcake ColoGenerator

1. Create a class ColorGenerator.php
2. In this class, create a method : generateBackground(array $colors): string
$colors is an array containing the 3 colors (in hexadecimal format) for each cream layer of the showed cupcake
This method will return an hexadecimal color who is an average of the 3 cream colors.
Tips :
This is how hexadecimal colors work :
![alt text](https://github.com/jfm-wcs/dojo-cupcake-color-generator/blob/master/hexcode.gif?raw=true)

**With #3C00A6 we have**:

- 3C : Quantity of red  
- 00 : Quantity of green  
- A6 : Quantity of blue  
Hexadecimal is made of numbers 0 to 9 and letters A to F
We can transform hexadecimal to a number in php. With [hexdec](https://www.php.net/manual/en/function.hexdec.php) and reverse with [dechex](https://www.php.net/manual/en/function.dechex.php).

To calculate average color, calculate average of the 3 "red" parts, the 3 "green" parts and the 3 "blue" parts, then concatenate the 3 values to obtain the new color.

Make some tests:
```php
$this->assertEquals("#db8f30", ["#ff9300", "#942192", "#fffb00"]);
$this->assertEquals("#ab9131", ["#dd2727", "#25c154", "#ffcd1a"]);
$this->assertEquals("#acd207", ["#ff8400", "#07ff00", "#fff315"]);
```

3. In ColorGenerator, create a method invertColor to reverse an hexadecimal color. An inverted color will be 255 (the max value) minus the actual color, for red, green, and blue. The returned value should be also in hexadecimal format. (e.g the inverse color of #ffffff will be #000000.)


Make some tests:

```php
$this->assertEquals("#2470cf", "#db8f30");
$this->assertEquals("#546ece", "#ab9131");
$this->assertEquals("#532df8", "acd207");
```
