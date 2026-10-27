# Zero Theorem V4.12.1 - zero, energy, counter (copy of zero_4112_principles_v1.py / V4.11.2)

Foundational cores: 0 (Z0), E (energy, unit J) and S (the natural counter).

What changed (and nothing else):
1. Energy is the ONLY declared physical quantity. The hand-written mass, length, duration,
   area, volume, velocity, acceleration, pressure and force definitions are removed.
2. No natural-units convention, no target names and no label table are supplied. The engine
   records only the powers of E that open exploration constructs (multiply / quotient / add /
   compare, fair fixed enumeration, no goal, no stop condition). Any physical reading of those
   powers is left to the observer.
3. New read-only command: energy-ladder (also: energy, energy-index) lists the powers of E built
   so far with how many constructions each has.
4. New memory file name: zero_theorem_v4121_energy_memory.json. V4.11.2 and V4.12.0 memory files
   are not compatible and are not touched.
5. Retired example commands removed from the help text.

Not changed: the archives, Zi/Z1i walkers, pathways, symbolic/calculus, clocks, replay, recovery,
and the strict S-only counter. physical_law_verified stays False everywhere.

Honest limits:
- With a single declared symbol, every construction is a power of E by construction. That is not
  a discovery.
- Joule-bearing objects go through Z0 in the quantity and physical domains only; the Zi walkers
  and pathways do not yet operate on them.
- Inherited: the memory file grows about 3 MB per launch and each launch gets slower.
