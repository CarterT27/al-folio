---
layout: post
title: My Keyboard-Centric MacOS Workflow
date: 2024-08-24 8:00:00
description: using open-source tools to navigate at lightspeed
tags: productivity
categories: misc
featured: true
---

# Introduction

As a student studying Data Science, I do a lot of programming. Sometimes this leads to me being on my computer for very long periods -- whether I'm checking emails, programming, watching lecture recordings, or just browsing the internet. I dislike constantly switching from my keyboard to my mouse or mousepad and then back to my keyboard, so I started looking for ways to reduce the wasted time spent using my mouse.

The least efficient approach is one that uses the mouse the most frequently, and I constantly see people taking 1-2 seconds just to switch between windows.

# Hiding the Dock

Instead of using the touchpad to select a new application from the dock to open, I rarely use the dock when I'm on my computer. Hiding the dock by right clicking it and choosing `Turn Hiding On` frees up a lot of screen real estate. Now, whenever you are not actively using the dock, it slides away from view.

# Basic Navigation

Why not just get rid of the dock entirely? When opening apps, it is much quicker to type `<command> + <space>` to open Spotlight, and then you can type in the first few letters of the application that you are trying to open and select it with `<enter>`. This approach allows you to open any app on your Mac mouse-free. 

Now that we can open apps without the mouse, how do we switch between them without using the dock? Well, spotlight lets you do that the same way as opening the app, but there are quicker ways. One approach would be to hold `<command>` and press `<tab>` to switch between opened apps. When you release `<command>`, the selected window will be focused. However, this approach can still take many keyboard entries to select the correct window, especially when you have many apps opened.

# Enter [AeroSpace](https://github.com/nikitabobko/AeroSpace).

AeroSpace is a window manager, similar to i3 for Linux users. It allows you to switch between windows (apps) in very few keypresses, as well as move them around your screen without clicking and dragging them with your mouse.

To install AeroSpace you must already have [Homebrew](https://brew.sh/) installed, which I highly recommend for not just programmers, but anyone looking to easily install applications on Mac. You can find installation instructions on the [homepage](https://brew.sh/), and it's as simple as pasting a command into your terminal and pressing `<enter>`.

Once you have installed Homebrew, you can install AeroSpace with the command `brew install --cask nikitabobko/tap/aerospace`. This will set up everything you need to start navigating your computer at lightspeed. 

# AeroSpace Basics

AeroSpace replicates the MissionControl functionality in MacOS, with the added benefit of being able to switch between workspaces, move windows between workspaces, move windows around the screen, change which window is focused, and more, all from your keyboard.


## What is a Workspace?

Workspaces are basically separate screens that you can switch between. For example, I generally like to keep most of my applications/windows maximized in their own screens. I'll have my terminal in the first workspace, my browser in another workspace, and my task manager in the third workspace. Once you run AeroSpace, it will automatically maximize any open windows and tile them, which means that if you have multiple windows open in a workspace they will each occupy separate parts of the screen.

## Keybinds

With the default configuration, AeroSpace keybinds are centered around the `<option>` key. I find this works for me, as my other keybinds use the `<command>` and `<control>` keys.  

You can switch between workspaces with `<option> + <key>`, where `<key>` is the workspace you want to switch to. In my workflow, `<option> + 1` opens my terminal workspace, and `<option> + 2` opens my firefox workspace. There are workspaces for every number and letter on your keyboard, so don't worry about running out of space.  

To move windows between workspaces, it is a similar command: `<option> + <shift> + <key>`, where `<key>` is the workspace you want to move the currently focused window to. When I am writing code in the terminal and want to see a live preview in my browser at the same time, I switch to my firefox workspace with `<option> + 2` and move firefox to the 1st workspace with `<option> + <shift> + 1`. Then, in my 1st workspace, the left half of the screen is comprised of my terminal, while the right half has my browser.  

If I want to switch the focus between my terminal and browser in the same workspace, I can use vim keybindings to move my focus around the current workspace's windows, so `<option> + h` will go left, `<option> + j` will go down, `<option> + k` will go up, and `<option> + l` will go right.  

If I am connected to an external monitor, I can move the current workspace to the other monitor by typing `<option> + <shift> + <tab>`. Then, I can switch my focus between monitors by switching between workspaces normally, but now one of the workspaces will be located at the other monitor. For example, I will have most of my workspaces on my main monitor, and then I will move my Task Manager workspace to the actual laptop screen by switching to it with `<option> + 3` and moving it with `<option> + <shift> + <tab>`. Then, I can simultaneously switch between my tasks on my laptop screen and my code and browser on my external monitor.  

# AeroSpace vs. Alternatives

Now that we know how to use AeroSpace, why even use it in the first place? AeroSpace allows switching between windows very quickly and the keybinds work well with my workflow and are easy to remember. I previously used [yabai](https://github.com/koekeishiya/yabai), which requires disabling `System Integrity Protection` to run, needs a separate application to control keybinds, and didn't feel as seamless when switching between workspaces. It felt laggy and like a workaround for a tiling window manager in Mac, instead of AeroSpace feeling like it could be integrated into the Apple ecosystem without anyone noticing. The basic MissionControl that MacOS provides is good, but it's a little harder to switch between workspaces quickly and the functionality isn't as seamless as the snappy tiling that AeroSpace offers. 

# Conclusion

I hope that this blog helped you become more productive on your computer. Stay tuned for more productivity tips and posts about technology!
