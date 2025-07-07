# Image-ToolBox

## Introduction
**Image Processing Toolbox** is an Android library that provides utilities to perform on images such as resizing
and processing

## Basic Usage
Resize an image:

```kotlin
// change image size 
val bitmap: Bitmap = IPOXResizer(bitmap)
                        .resize(0.5F)
                        .bitmap
imgView.setImageBitmap(bitmap)
```

## Advanced Usage

```kotlin
// change image ratio (ICAO)
val bitmap: Bitmap = IPOXResizer(bitmap)
                        .changeRatio()
                        .resizeByWidth(140)
                        .bitmap
imgView.setImageBitmap(bitmap)
```

```kotlin
// change image ratio (Custom) = height / width
val bitmap: Bitmap = IPOXResizer(bitmap)
                        .changeRatio(2F)
                        .resizeByHeight(180)
                        .bitmap
imgView.setImageBitmap(bitmap)
```

```kotlin
val bitmap: Bitmap = IPOXTransform(resized)
                        .grayscale()
                        .bitmap
```

## Set up
Add dependency to your `build.gradle`:
```groovy
implementation("fr.sabry.ipox:ipox:1.1.1")
```
