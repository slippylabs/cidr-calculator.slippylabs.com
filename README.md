# CIDR & Subnet Calculator

IPv4 and IPv6 subnet calculator — host ranges, masks, splitting a block into subnets, and aggregating a list of ranges. Runs entirely in your browser.

**Live:** <https://cidr-calculator.slippylabs.com/>

## What it does

- IPv4 and IPv6 subnetting — network and broadcast address, mask, wildcard, usable host range and count.
- Split a block into a given number of subnets, or into subnets big enough for a given host count.
- Check whether an address is contained in a prefix.
- Aggregate a messy list of ranges into the fewest CIDR blocks that cover it exactly.

## How it works

The aggregation is the part worth having: given an arbitrary list of ranges it merges the overlaps and then emits the minimal set of prefixes covering exactly that space and no more — the operation you actually need when writing a firewall rule or a route table, and the one that is miserable to do by hand.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/cidr-calculator.slippylabs.com.git
cd cidr-calculator.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
