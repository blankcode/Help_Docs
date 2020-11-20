# WIFI and audio/video meetings really don't mix

## My meetings are dropping or have a bad "jittery" connection.

Meetings aren't like other traffic, they are live data and UDP rather than TCP. That means there is no preloading of data available and if a packet is missed either going up or coming in, it's just lost forever.

The constant 2-way connection that's needed for meetings will normally saturate most access points. This is true unless both the AP and device (laptop/tablet/phone) are MU-MIMO enabled.

## Possible Fixes:

- Ethernet, get that sucker wired.
- A new router that supports AND has a good implementation of MU-MIMO. This will be better but, I don't know if it would be perfect.
- If cost is a problem and getting a wired connection to your meeting device is out of the question, you could get a cheap N router and get it as close as you can to your device. Set it up in AP only mode and now, that AP is your Meeting device's dedicated AP. Allow only your meeting device to connect to this AP, NO others.
- let's say you, your spouse and your 5 kids all need to bne on meetings for work and school.

  - If you want to layout the money for each person to have their own AP, I'd go with a set 0f 5Ghz APs/Routers in AP Mode.
    - 5Ghz has MANY more channels and overlapping is far less of an issue.
  - You COULD use multiple/many 2.4Ghz access points, just use a pattern and try not to overlap the channels.

    - Channels 1, 6 and, 11 are the only ones that do not overlap with another.

## Channel Overlap

    ([1] 2 3) (4 5 [6] 7 8) (9 10 [11] 12 13) 14

- 14 is not used in the US.

### Here's a good pattern:

     1 6 11
    6 11 1 6
     1 6 11

### God help you if you need one this big...

     1 6 11 1 6 11 1 6 11
    6 11 1 6 11 1 6 11 1
     1 6 11 1 6 11 1 6 11
    6 11 1 6 11 1 6 11 1
     1 6 11 1 6 11 1 6 11
    6 11 1 6 11 1 6 11 1
     1 6 11 1 6 11 1 6 11
