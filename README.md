# Everything an MBA learns

An interactive 3D prerequisite map of the MBA core curriculum — every concept a dot, every link a prerequisite. Inspired by [Marble's map of primary school](https://withmarble.com/curriculum/).

**136 concepts · 180 prerequisite links · 8 disciplines**

Data & Decisions · Economics · Accounting · Finance · Marketing · Operations · Strategy · Leadership & Organizations

## Use it

Open `index.html` in a browser — it's a single self-contained file with no dependencies and no build step.

- **Drag** to spin · **right-drag** to pan · **scroll** to zoom · **double-click** to reset
- **Tap any dot** to see everything you must master before it: the full prerequisite chain lights up, with "Builds directly on" and "Unlocks next" panels for navigating the graph
- **Click a discipline chip** to toggle it on or off
- **Search** for any concept by name

## The data

The curriculum graph lives in the `CONCEPTS` array at the top of the script in `index.html`. Each entry is:

```js
['wacc', 'Cost of capital (WACC)', 3, ['capm', 'bonds']]
// [id, name, disciplineIndex, [prerequisite ids]]
```

The graph is a validated DAG — no cycles, no dangling references — with 16 root concepts that have no prerequisites. Prerequisites cross discipline boundaries where the pedagogy does: pricing strategy builds on elasticity (economics) and break-even analysis (accounting); firm valuation by DCF builds on NPV, WACC, and the statement of cash flows.

Edit the array to re-sequence the curriculum or add your own concepts; the layout, counts, and interactions all derive from it at load time.

## License

Concept data is released under the [Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/), matching the license Marble uses for its curriculum data. Code is MIT.
