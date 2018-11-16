---
layout: post
title:      "Require Pry"
date:       2018-11-16 18:55:16 +0000
permalink:  require_pry
---


When I first read about learning how to using `binding.pry` I was like "pshh" I'll never use this...

Boy, was I very wrong. Once I reached the hash and enumerable lessons,`binding.pry` became my best friend. It helps so much in debugging code your code and trying to uncover what each variable, array, hash or method is trying to do. Pretty much like how Hash with it's values and keys is a dictionary, `binding.pry` is a great tool to uncover what your calling and see if your code will actually work. Which is pretty cool so you don't have to make assumptions on what your code is trying to do. 

Whenever using binding.pry remember to put `require "pry"` at the top of your code page so that you can access the feature. If you want to learn more about it you can check out the official pry website [](http://pryrepl.org/). You can put `binding.pry` before code that you are trying to debug. It will actually freeze the code and you can make any modifications in the command line or in your code without it running everything through. 

My favorite use is calling `binding.pry` when I am working on Hash/Array Enumerables. So if you have something like this 

```
require "pry"

sandwich = ["pickles", "bread", "ketchup", "lettuce"]

sandwich.each do |item|
     binding.pry
    puts item
end

```

Once you press learn in the IDE terminal you can can see what `item` is just by typing it in the command line. If you want to have more fun you can even try typing in different bits of codes to see if your code will return true or false. All in all it's a great tool that has unexpectedly helped me more than I thought it would. Also if you have the learn IDE console downloaded on your computer then you don't need to go through all the steps to download PRY!



