DRAM - Dynamic Random Access Memory 
. DRAM Capacitor charge leaks over time, so the memory controller needs to refresh each row periodically to restore charge. 
- active each row every N ms
- Typical N = 64ms

Downsides of refresh
	-- energy consumption: Refreshing consumes energy
	-- performance degradation: DRAM rank/bank unavailable while refreshed. 
	--- QOS (quality of service) / predictability impact: (Long) pause times during refresh
	-- refresh rate limits DRAM capacity scaling. - More cells to refresh. Causes longer pauses during those 64ms periods. 

How can we solve these problems?

Critical thinking: Do we need to refresh all rows every 64 ms? 

No. Technically. Some cells can last for much longer without being refreshed - the reason we fresh every 64ms (typically) is because manufacturing is not perfect, and we have to account for small variations in each cells performance.
A DRAM cell is made of a capacitor and an access transistor. Some cells are 'more leaky' then others. 

How could we take advantage of this profile? 

#### Most DRAM rows can be refreshed much less often without losing data 

CITE - `Raidr: Retiention-Aware Intelligent DRAM Refresh` ISCA 2012

The key idea of RAIDR: Refresh weak rows more frequently, all other rows less frequently. 