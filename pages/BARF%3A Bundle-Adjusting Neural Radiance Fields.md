title:: BARF: Bundle-Adjusting Neural Radiance Fields
alias:: BARF

- A hard prerequisite of [[NeRF]] and other view synthesis methods is accurate camera poses of the given images, which is typically obtained through auxiliary off-the-shelf algorithms.
- ## Major Contributions
	- Establish a theoretical connection between classical image alignment to joint registration and reconstruction with [[NeRF]].
	- Show that susceptibility to noise from positional encoding affects the basin of attraction for registration, and we present a simple strategy for coarse-to-fine registration on coordinate-based scene representations.
	- Our proposed [[BARF]] can successfully recover scene representations from imperfect camera poses, allowing for applications such as view synthesis and localization of video sequences from unknown poses.
-
-