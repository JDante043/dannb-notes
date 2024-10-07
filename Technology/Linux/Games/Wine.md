[Wine](https://www.winehq.org/) is a compatibility layer that allows users to run Windows applications in Linux systems. A paid / commercial version of it also exists, called [CrossOver](https://www.codeweavers.com/crossover).

In gaming, there are usually 4 different versions of wine that's used:
- Normal Wine
- [Proton](https://github.com/ValveSoftware/Proton): A version of wine developed by Valve for use in steam.
- [Wine-GE](https://github.com/GloriousEggroll/wine-ge-custom): A version of wine developed by GoldenEggroll, usually preffered over wine.
- [Proton-GE](https://github.com/GloriousEggroll/proton-ge-custom): A version of proton developed by GoldenEggroll.

!!!Do note that running any version of Proton outside of steam is highly **not** recommended.
!!!

For uses outside of gaming, such as running a normal Windows application, normal wine is usually enough. 

Running an application will cause wine to create a `WINEPREFIX` in `~/.wine`. This will be your "C: drive". If a separate prefix is desired, you may manually change your `WINEPREFIX` to point to another location when starting your application, meaning that you will have to launch it from a terminal, or, you may install an application to manage individual prefixes, such as [Bottles](https://usebottles.com/).
