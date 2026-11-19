# Social media studio for Gemini CLI

A [Gemini CLI](https://github.com/google-gemini/gemini-cli) extension that connects Gemini to
[Social media studio](https://so-me.studio), so you can schedule and publish posts on 18 social
platforms, manage drafts and media, reply from the unified inbox and check analytics from your
terminal.

It adds Social media studio's hosted MCP server (`https://api.so-me.studio/mcp`, Streamable HTTP)
and a short context file that tells Gemini how to use it safely.

## Install

```bash
gemini extensions install https://github.com/7t1-studio/social-media-studio-gemini-extension
```

Then start Gemini CLI and sign in:

```text
/mcp auth social-media-studio
```

Your browser opens Social media studio's sign-in and consent page (OAuth 2.1 with PKCE). After you
approve, run `/mcp` to see the server and its tools.

### Use an API key instead

If you prefer an API key (`sk_live_...`, created in **Settings → API** at
https://app.so-me.studio/settings?tab=api), add the server to `~/.gemini/settings.json` yourself;
a server defined there takes precedence over the extension's:

```json
{
  "mcpServers": {
    "social-media-studio": {
      "httpUrl": "https://api.so-me.studio/mcp",
      "headers": { "X-API-Key": "sk_live_your_key" }
    }
  }
}
```

## What you need

- A Social media studio account on a paid plan (Lite, Creator, Standard, Advanced or Lifetime).
  Paid plans start with a 7-day trial. Tool calls use MCP credits from the plan.
- Social accounts connected in Social media studio.

## Example prompts

- "List my connected social accounts."
- "Schedule this for my LinkedIn Page on Monday at 9:00 Dhaka time: …"
- "Turn this blog post into a five-part X thread and schedule it for tomorrow at 15:00 UTC."
- "Check whether this video works as a TikTok and an Instagram Reel before I post it."
- "Save it as a draft for my X account instead of posting."
- "How did my Instagram account do over the last 30 days?"

## Platforms

X, LinkedIn (profiles and Pages), Instagram, Facebook, TikTok, YouTube, Threads, Pinterest,
Bluesky, Mastodon, Reddit, Google Business Profile, WordPress, Dev.to, Dribbble, Discord and Slack.

## Links

- Docs: https://docs.so-me.studio/mcp/overview
- Gemini CLI setup guide: https://docs.so-me.studio/mcp/gemini-cli
- Privacy: https://so-me.studio/privacy-policy
- Terms: https://so-me.studio/terms-and-conditions
- Support: support@so-me.studio

## License

MIT. See [LICENSE](LICENSE).
