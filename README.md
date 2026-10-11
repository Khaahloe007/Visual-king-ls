# Visual-king-ls
Visual King LS - Real-time defense system that logs REAL internet attacks (not simulation), auto-blocks malicious IPs via threat intelligence, stores all events in persistent KV database, provides live PWR, attack stats, and two-way communication between cloud and phone terminal.
# Visual King LS

**Real-world defense system. Not a simulation.**

### What it is
Visual King LS is a live security system built from a phone in Soweto using only Termux, GitHub and Cloudflare. It does not generate fake attacks. It lives on the real internet at `workers.dev` and waits for real bots, scanners and hackers to find it — and it logs everything.

It was built after testing 2,367 logs and 116 lessons with 100% immunity in simulation. Now it is moved to the real world.

### What it does
1. **Logs REAL attacks:** Every time a bot from anywhere in the world visits your link, it records IP, path, payload, country, and time into persistent storage (Cloudflare KV). It keeps 7 days of history.
2. **Checks threat intelligence:** Every IP is checked against AbuseIPDB (1000 free checks per day). If abuse score is >75, it is marked malicious.
3. **Auto-blocks:** Bad IPs are blocked instantly and shown a block page. Good users pass through.
4. **Shows live stats:**
   - `/stats` - total attacks, blocked count, top attacking countries, top targeted paths
   - `/logs` - last 50 real attacks
   - `/pwr` - real Power calculation from live traffic, not fake 100%
5. **Two-way communication:** 
   - `/talk?msg=...` - you can send a message from Termux to the cloud, and the cloud can reply. Your phone becomes a command center.
6. **Never sleeps:** Built on Cloudflare Workers (100k requests/day free). No server to pay, no laptop needed, runs 24/7.

### Purpose
Most security demos show fake percentages: "35 signals, 6x 100%". No municipality, school or spaza shop can use that.

Visual King LS proves with real evidence:
- Who is attacking you RIGHT NOW
- Where they come from
- What they are trying to hack
- And blocks them automatically

It is built for municipalities, SAPS, schools, small businesses, and personal phones — anyone who wants to see their real threat level, not a simulation.

It costs R0, needs no credit card, and runs 100% from a phone.

### Tech Stack
Cloudflare Workers + KV + AbuseIPDB + GitHub + Termux

### Quick Test
