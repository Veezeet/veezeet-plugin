# Veezeet

![Veezeet](assets/icon.png)

Veezeet is a trip planner. This plugin connects your assistant to your own Veezeet trips and teaches it how to use them. It covers seven jobs: plan a trip, vote on an option (a hotel, an activity, a date), check on a trip, bring the group in, import what is already booked, shape a day, and fix or undo a change.

## Use it

In Claude Code, install it with:

```
/plugin install veezeet --marketplace Veezeet/veezeet-plugin
```

In ChatGPT, add `https://api.veezeet.com/planner/mcp` as a custom MCP server, then import the plugin as a ZIP whose files sit at its root (it reads `.codex-plugin/plugin.json`).

Then connect Veezeet when your assistant asks and sign in with your Veezeet account. Then ask in your own words: "plan five days in Lisbon for two", "put three hotels to the group's vote", "what changed on our Japan trip?", "invite Sam to the trip as an editor". Setup and the list of tools are at https://veezeet.com/connector.

## What it does and does not do

The assistant works on your trips signed in as you. Everything it changes is attributed to it in the trip's history and can be undone. Veezeet does not book or pay for anything; a link it gives you opens a page on veezeet.com.

## Data

The plugin holds only instructions and the address of the Veezeet server, `https://api.veezeet.com/planner/mcp`. Your assistant sends the trip details you discuss to your Veezeet account through that server. The plugin stores nothing itself. Privacy policy: https://veezeet.com/privacy. Support: https://veezeet.com/support.

## Maintenance

`skills/plan-a-trip/references/planning-guide.md` is generated from the guide the Veezeet server returns from `get_planning_guide`. Do not edit it here.
