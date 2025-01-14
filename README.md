![](https://raw.githubusercontent.com/LuckPerms/branding/master/banner/banner.png "Banner")
# LuckPerms
[![Build Status](https://ci.lucko.me/job/LuckPerms/badge/icon)](https://ci.lucko.me/job/LuckPerms/)
[![javadoc](https://javadoc.io/badge2/net.luckperms/api/javadoc.svg)](https://javadoc.io/doc/net.luckperms/api)
[![Maven Central](https://img.shields.io/maven-metadata/v/https/repo1.maven.org/maven2/net/luckperms/api/maven-metadata.xml.svg?label=maven%20central&colorB=brightgreen)](https://search.maven.org/artifact/net.luckperms/api)
[![Discord](https://img.shields.io/discord/241667244927483904.svg?label=discord&logo=discord)](https://discord.gg/luckperms)

LuckPerms is a permissions plugin for Minecraft servers. It allows server admins to control what features players can use by creating groups and assigning permissions.

You can find LuckPerms's latest downloads, wiki & other valuable links on the project homepage at [luckperms.net](https://luckperms.net/).

It is:

* **fast** - written with performance and scalability in mind.
* **reliable** - trusted by thousands of server admins and the largest of server networks.
* **easy to use** - setup permissions using commands, directly in config files, or the web editor.
* **flexible** - supports various data storage options and works on many different server types.
* **extensive** - many customization options and settings that can be changed to suit your server.
* **free** - available for download and use at no cost and permissively licensed to remain free forever.

For more information, see the wiki article on [Why LuckPerms?](https://luckperms.net/wiki/Why-LuckPerms)

## Building
LuckPerms uses Gradle to handle dependencies & building.

#### Requirements
* Java 17 JDK or newer
* Git

#### Compiling from source
```sh
git clone https://github.com/LuckPerms/LuckPerms.git
cd LuckPerms/
./gradlew build
```

You can find the output jars in the `loader/build/libs` or `build/libs` directories.

## Tests
Some automated tests run during each build.

* Unit tests are defined in [`common/src/test`](https://github.com/LuckPerms/LuckPerms/tree/master/common/src/test)
* Integration tests are defined in [`standalone/src/test`](https://github.com/LuckPerms/LuckPerms/tree/master/standalone/src/test).

## Contributing
#### Pull Requests
If you make any changes or improvements to the plugin that would benefit others, please consider making a pull request to merge your changes into the upstream project. (especially if your changes are bug fixes!)

LuckPerms loosely follows the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html). Try to copy the style of code found in the class you're editing. 

#### Project Layout
The project is split up into a few separate modules.

* **API** - The public, semantically versioned API used by other plugins wishing to integrate with and retrieve data from LuckPerms. This module (for the most part) does not contain any implementation itself and is provided by the plugin.
* **Common** - The standard module contains most code implementing the respective LuckPerms plugins. This abstract module reduces duplicated code throughout the project.
* **Bukkit, BungeeCord, Fabric, Forge, Nukkit, Sponge & Velocity** - Each uses the standard module to implement plugins on the respective server platforms.

## License
LuckPerms is licensed under the permissive MIT license. Please see [`LICENSE.txt`](https://github.com/LuckPerms/LuckPerms/blob/master/LICENSE.txt) for more information.
