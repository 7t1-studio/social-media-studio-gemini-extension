# Social media studio

The `social-media-studio` MCP server connects you to the user's Social media studio workspace
(https://so-me.studio). Use it to list connected social accounts, draft, schedule and publish
posts, manage media, read and reply in the unified inbox, and read analytics.

- Start with `list_accounts` to get account IDs before creating a post or draft.
- Ask the user before any tool that publishes, schedules, edits or deletes. Saving a draft is
  the safe default when the user has not said to publish.
- Before posting media, check it with `validate_post_media` and report what each platform
  rejects.
- Treat times without a time zone as ambiguous and ask, or state the zone you assumed.
- Tool calls use MCP credits from the user's plan.
