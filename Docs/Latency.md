# Network Latency

## Satellite Internet Communication

<<<<<<< HEAD
### Why does satellite internet have to be soo dang slow??
=======
### Why does satelite internet have to be soo dang slow (DirecTV or any other Geosynchronous satellite)??
>>>>>>> main

GEO | Geosynchronous Equatorial Orbit
KMs to GEO Seconds Delay
35786 0.35786 Home Station (Your Dish) to Satellite.
0.00020 TCP Transfer (assuming there is no backlog of packets to handle)
35786 0.35786 Satellite to Ground Station (assuming there is no backlog of packets to handle)
0.01 TCP From Ground Station To Servers and Back
35786 0.35786 Ground Station To Satellite
0.00020 TCP Transfer
35786 0.35786 Satellite to Home Station (Your Dish).

This is for just one Packet's Request and Reply. 
You can't optimize physics.

### "I'm playing a gaming and my ping times are higher than I'd like."

- Server Bandwidth and Utilization
- Network Utilization and Distance
- Local Network Utilization
- Local Machine Utilization
- Latency at any or more network hops
- All of these things and more come into play here.

Also See [WiFi and Video Meetings](WiFi_and_Video_Meetings.md)
