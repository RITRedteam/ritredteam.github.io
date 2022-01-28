# RITSEC Redteam Wiki

RITSEC Redteam is a group of students and alumni write and use custom tooling to attack competition infrastructure. This provides a challenging learning environment for blue teams.

This is our wiki. Here we will document all of our publicly released tools.

## Contributing Your Tool's Documentation

> Note: please be sure to strictly follow the metadata instructions in order to ensure your tool properly shows up in the sidebar

### Identify your category

First, identify which category your tool falls into:

```
/windows
/linux
/networking
/cross-platform
```

### Make a folder for your tool

Create a folder within your given category for your tool. (ex. for a windows tool named `Bingus` you would create the `/windows/bingus/` directory)

> Note: please use hyphens in place of spaces in folder/file names

### Add your tool's home page

Go ahead and add an `index.md` file inside your tool folder and then use this template to add your page metadata and a brief description of your tool.

So the `/windows/bingus/index.md` would look like:

```
---
layout: default
title: Bingus
parent: Windows
has_children: true
---

# Bingus

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

### Add additional pages for your tool

For additional pages, there is just one slight modification to the home page metadata we need to make. Again using the `Bingus` example, here would be the installation page (`/windows/bingus/installation.md`):

```
---
layout: default
title: Installation
parent: Bingus
grand_parent: Windows
nav_order: 1
---

# Installation

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

> Note: if the `nav_order` field is omitted, the pages will just be sorted alphabetically

Now you are free to add other pages to your tool folder as needed. The table of contents on the home page is auto-generated so no need to worry about generating that (auto generates links to all of the pages in your directory).
