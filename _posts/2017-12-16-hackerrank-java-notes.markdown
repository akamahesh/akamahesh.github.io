---
layout: post
title: Hackerrank - Java Notes
date: 2017-12-12 00:00:00 +0300
description: Java Notes # Add post description (optional)
img: how-to-start.jpg # Add image post (optional)
tags: [Java] # add tag
---


# Hackerrank - Java Notes  

> Java output formatting  

In each line of output there should be two columns:   
The first column contains the String and is **left justified** using exactly 15 characters.
The second column contains the integer, expressed in exactly **3 digits**; if the original input has less than three digits, you must pad your output's leading digits with zeroes.

```Java
System.out.printf("%-15s%03d%n", s1, x);
```
**Formatting**  

```Java
public class Root2 {
    public static void main(String[] args) {
        int i = 2;
        double r = Math.sqrt(i);

        System.out.format("The square root of %d is %f.%n", i, r);
    }
}  
```  
Conversions  
1. d formats an integer value as a decimal value.
2. f formats a floating point value as a decimal value.
3. n outputs a platform-specific line terminator.
4. x formats an integer as a hexadecimal value.
5. s formats any value as a string.
6. tB formats an integer as a locale-specific month name.
