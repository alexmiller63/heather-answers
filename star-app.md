So far, the working 2026 Almanack has a surprisingly substantial astronomical core. In ISO2026.md we have the purpose and ISO-year framework, the tropical zodiac layer calculated from our own solar-longitude equations, and the 100-object layer with 50 stars and 50 Messier objects. Each object has a calculated 2026 best-visibility date, the stars have Bayer designations, and the reader-facing classification uses declination band first and astronomical season second: for example, Northern Summer. Arctic and Antarctic objects retain their best-visibility dates but do not receive seasons. We have also prepared the complete set of 50 major lunar phases for ISO 2026—New Moon/conjunction, First Quarter, Full Moon, and Last Quarter—with our calculated times checked against USNO. The ISO-year coverage is 2025-12-29 through 2027-01-03.

Around that, we have already established several book-wide conventions: zodiac and planetary symbols to reduce clutter, first-use expansion such as ♈ (Aries) 1, astronomical rather than month-based seasons, the 5 declination bands based on approximately ±23.5° and ±66.5°, and the distinction between globally calculable events and location-dependent predictions such as crescent visibility.

As for an app: the basic Star Almanack app would not be terribly difficult. Most of the intellectual work is actually what we are doing now—defining precisely what the numbers mean. Once those rules are stable, software can execute them repeatedly.

A useful progression would be:

* Version 1: date → ISO week date, zodiac day, lunar phase information, and the stars/Messier objects that are well placed around that date.
* Version 2: use the phone’s location to show what is actually above the horizon, altitude/direction, rise/transit/set information, and observer-specific finding instructions.
* Version 3: location-dependent calculations such as predicted crescent visibility, planetary visibility, conjunctions, twilight conditions, and perhaps interactive star charts.

The biggest engineering challenge is not displaying the calendar. It is making the astronomical engine rigorous enough that we know exactly which coordinate systems, epochs, apparent corrections, time scales, atmospheric assumptions, and visibility criteria are being used. But we are already documenting those decisions instead of burying them in code, which makes the eventual app much easier to build correctly.

And the crescent problem illustrates why the app becomes significantly more powerful than the printed Almanack. The book cannot know where its reader is standing. The app can. Once it knows latitude, longitude, elevation, date, and local sunset, it can answer questions the book deliberately cannot.

So I would characterize it as moderate software work, not a massive research project. The difficult conceptual foundation is already being built into Star Almanack itself.

