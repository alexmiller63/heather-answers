Yes. The 20 results point to a very clean method, and it is simpler than the sidereal-rate approach I started to reconstruct earlier.

At a star’s meridian transit, its hour angle is 0, so local sidereal time equals the star’s right ascension:

\mathrm{LST}=\alpha_\star

Local apparent solar time is based on the apparent Sun’s hour angle. At exactly 9:00 PM local apparent solar time, the Sun’s hour angle is exactly 9h. Therefore:

\mathrm{LST}=\alpha_\odot+9\mathrm{h}

For the star to transit at that same 9:00 PM condition:

\alpha_\star=\alpha_\odot+9\mathrm{h}

or, equivalently,

\boxed{\alpha_\odot=\alpha_\star-9\mathrm{h}}

That gives us the algorithm that should reproduce the 20 dates:

1. Take the star’s right ascension.
2. Subtract exactly 9h, wrapping through 24h if necessary.
3. Find the annual instant when the apparent Sun’s right ascension equals that value.
4. Convert that instant to the Almanac’s calendar convention—ultimately the ISO week date.
5. Compare the resulting date against our existing 20 results as a regression test.

For Betelgeuse, with right ascension about 5h 55m, the target solar right ascension is about 20h 55m. The Sun reaches that right ascension around Jan 31, which immediately explains why our previous calculation produced Betelgeuse — Jan 31.

There is an especially nice conceptual feature here: because we chose local apparent solar time, longitude drops out of the core equation. We are comparing 2 celestial clocks—the star’s right ascension and the apparent Sun’s right ascension—with a fixed 9h separation.

I think this is very likely the method underlying our 20 successful results. The next useful step is to run this equation against all 20 old answers and see whether it reproduces 20/20.

