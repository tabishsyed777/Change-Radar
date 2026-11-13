# Change Radar

**A change-impact analysis tool that follows modeled dependencies to show which requirements, components, and interfaces may be affected.** Import a System Atlas model and turn a proposed change into a scoped, portable impact report.

## What it does

- Import a versioned `system-atlas` JSON export or explore the bundled sample map.
- Select the record that is changing and traverse its dependents by depth.
- See affected item type, owner, and description to guide review.
- Export the result as `change-radar-report` JSON for [Release Ledger](https://github.com/tabishsyed777/Release-Ledger).
- Keep the imported map in this browser for the next visit.

## Run it

Open `index.html` in a current browser. There is no build step, server, account, or external service. Use **Import system map** to load the JSON exported from [System Atlas](https://github.com/tabishsyed777/System-Atlas).

## How the analysis works

If item B lists item A as a dependency, changing A places B in scope. Change Radar walks those reverse dependency links and records the shortest discovered depth. Cycles are bounded by a visited set. The report includes the starting item, change summary, source timestamp, and impacted items.

## Scope

This is decision support over the records in the imported map. It does not inspect a repository, infer missing relationships, run tests, or certify that every affected area has been found. Keep the system model current and review the results with the relevant owners.

Released under the MIT License.
