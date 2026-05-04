# guillemroca — Claude Code Plugin Marketplace

A curated marketplace of Claude Code plugins maintained by [Guillem Roca](https://github.com/GuillemRoca).

## Install the marketplace

```bash
claude plugin marketplace add GuillemRoca/claude-plugins
```

## Available plugins

| Plugin | Description |
|--------|-------------|
| [`agent-skills-android`](https://github.com/GuillemRoca/agent-skills-android) | Production-grade Android engineering skills for AI coding agents |

## Install a plugin

```bash
claude plugin install agent-skills-android@guillemroca
```

To update later (use the fully qualified `plugin@marketplace` form):

```bash
claude plugin update agent-skills-android@guillemroca
```

> **Update fails with an SSH / "Permission denied (publickey)" error?** The marketplace clones repos via SSH. If you don't have SSH keys set up on GitHub, either [add your SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) or use the full HTTPS URL to force HTTPS cloning:
> ```bash
> /plugin marketplace add https://github.com/GuillemRoca/claude-plugins.git
> /plugin install agent-skills-android@guillemroca
> ```

## Adding a new plugin

1. Publish the plugin in its own GitHub repo with `.claude-plugin/plugin.json` at the root.
2. Append an entry to `.claude-plugin/marketplace.json` here:
   ```json
   {
     "name": "my-new-plugin",
     "description": "...",
     "source": { "source": "github", "repo": "GuillemRoca/my-new-plugin" }
   }
   ```
   The plugin's own `plugin.json` declares the version — omitting it here lets updates propagate automatically.
3. Push.

## License

MIT
