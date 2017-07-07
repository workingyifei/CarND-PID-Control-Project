cte or cross track error is the distance to the center of the road or where we want to be.

p error is basically cte. P or proportional is proportional to p error. higher p error makes the system unstable so car may drift away from road easily (big oscillation), lower p error tends to make the system unresponsive so car may not turn.

i error is the accumulation of all cte's. I or integral is proportional to i error. i error overcomes any biases in the system such as misaligned wheel or tires. since we are using simulator, i error is set to very small

d error is the difference between current and previous cte. D or derivative is proportional to d error. d error counter-steer cte or the p error to mitigate or dampen the oscillation. It's useful when car is in a sharp turn where P and I may not be able to bring the vehicle back in time.

I tuned P, I and D manually starting with P and D. With P = 0.3, the car drift heavily and after decreasing to 0.1 it seems to be stable. Then tune D and increase little by little bo compensate or decrease the oscillation till optimal. I've found out with P=0.2, I=0.004 and D=3.0, the car runs best in the simulator.