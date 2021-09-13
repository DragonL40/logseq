-
  > Consider again a situation in which we have a single resource and a set of $n$ requests to use the resource for an interval of time. Assume that the resource is available starting at time $s$. In contrast to the previous problem, however, each request is now more flexible. Instead of a start time and finish time, the request i has a deadline $d_i$, and it requires a contiguous time interval of length $t_i$, but it is willing to be scheduled at any time before the deadline. Each accepted request must be assigned an interval of time of length $t_i$, and different requests must be assigned non-overlapping intervals.
- Beginning at our overall start time $s$, we will assign each request $i$ an interval of time of length $t_i$; let us denote this interval by $[s(i), f(i)]$, with $f(i) = s(i) + t_i$.
- A request $i$ is _late_ if $f(i) > d_i$, and the _lateness_ of such a request $i$ is defined to be $l_i = f(i)-d_i$.
- **The goal is to schedule all requests, using non-overlapping intervals, so as to minimize the _maximum lateness_**
-
- What is the greedy criteria?
  collapsed:: true
	- Earliest Deadline First, $d_1 \le \dots \le d_n$
- The Algorithm
  collapsed:: true
	- Order the jobs in order of their deadlines
	- Assume for simplicity of notation that $d_1 \le \dots \le d_n$
	- Initially, $f = s$
	- Consider the jobs $i = 1, \dots, n$ in this order
		- Assign job $i$ to the time interval from $s(i) = f$ to $f(i) = f + t_i$
		- Let $f = f +t_i$
	- End
	- Return the set of scheduled intervals $[s(i), f(i)]$ for $i = 1, \dots, n$
- _T_
-
-