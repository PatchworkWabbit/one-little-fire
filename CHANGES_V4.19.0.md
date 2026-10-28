# V4.19.0 (copy of V4.15/4.16 line; your originals untouched). Memory file: zero_theorem_v419_energy_memory.json - start fresh.

Everything below replaces a number or an order that was typed into the code with something the
engine counts or saves itself. Nothing is dropped; deferred work is kept and revisited.

## From V4.16.0 (already sent)
- Zi rotations are read by slot type (3 of 4 rotations never ran before).
- Observed repeated addition becomes one saved operation that later multiplies cite.

## V4.17.0 - why nothing passed 4 expressions
1. Feedback peers: a new record was only added/multiplied with records 0,1,2 (`[:3]`).
   Still included (the first counted records), PLUS the record's direct parents and every record in its i chain.
2. Pair lane budget was a typed 4 per launch. Now max(4, how many counter states exist).
3. The main queue stopped for the whole launch after one look found only finished jobs, so ~1 task
   ran per launch instead of 64. It now keeps walking the saved order (capped at 8x the work budget).

## V4.18.0 - 00404 slots (the optional-slot machine)
1. Template: the reservation was the literal '00404' (11 slots, once per path). It is now taken from
   each counter value as its digit string (digits 0-9, any length, no cap): '00404', then '0','1','2',... 
   one reservation per template per path.
2. New step `optional_insert`: put a placed operation and value at any point INSIDE an expression
   (between its numbers), not only around the whole thing.
3. Slot contents: besides complex numbers, operations and roles, whatever algebra (symbolic archive),
   calculus and energy slots have EMERGED by then can be placed in a slot. They are held as retained
   records with status 'unresolved' (no numeric reading is supplied), and keep mixing.
   Operations are now offered first and every content is offered to every blank before the next content.
4. The slot lane's work per launch was a typed 5. Now max(5, counter states x lanes, number of slot nodes).
   It also keeps walking its saved order after an empty look.

## V4.19.0 - fair selection that does not starve late jobs
The selector walked (job, visit) pairs diagonally. Reaching job N cost about N squared steps, so
later jobs were never reached (only 34 core jobs ever ran in 20 launches). It now alternates:
a FRESH walk offers every never-attempted job once in saved order; a REVISIT walk keeps the original
diagonal over deferred jobs. The replay check was rewritten to match and still rejects skipped jobs.

## Test results (fresh archive, replay PASS every launch, no crashes)
- Old V4.16.0, 20 launches: biggest expression 4 units; 34 core jobs ever ran.
- V4.19.0, 10 launches: 8-unit expressions appear; slot machine reserved templates '00404','0','1';
  80 operations placed. No value placed, no combine or insert yet (they come later in the order).
- Launch time grows (about 110 s at launch 10 on my server); memory file ~ see size on your phone.

## Still open
- Unit slots from the 4s (the 1111s) are not yet turned into zero functions.
- Division, P (predecessor) as an operation, observer record.
- Values reached so far are small; this build only proves the machine is moving.
