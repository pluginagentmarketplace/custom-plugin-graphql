# Installation Guide

## Developer Roadmap Plugin for Claude Code

### Prerequisites

- Claude Code CLI installed
- Git (optional, for cloning)

### Installation Methods

#### Method 1: From Directory (Local Development)

```bash
# Navigate to plugin directory
cd /path/to/custom-plugin-graphql

# Load in Claude Code
# Use command in Claude Code:
# load from ./custom-plugin-graphql
```

Or use from absolute path:
```bash
load from /home/user/custom-plugin-graphql
```

#### Method 2: Single Command

```bash
# Copy and paste into Claude Code:
claude-plugin add /home/user/custom-plugin-graphql
```

#### Method 3: From GitHub (When Published to Marketplace)

```bash
claude-plugin add github:pluginagentmarketplace/custom-plugin-graphql
```

### Verify Installation

After installation, verify with:

```
/browse-agent
```

You should see all 7 agents listed.

### Quick Test

1. Type `/learn` - Should show role selection
2. Type `/roadmap backend` - Should show backend roadmap
3. Type `/assess` - Should start assessment

## Configuration

The plugin is ready to use out of the box. Optional configuration:

### Enable/Disable Hooks

Edit `hooks/hooks.json` to enable/disable analytics and progress tracking:

```json
{
  "settings": {
    "auto_progress_tracking": true,
    "achievement_badges": true,
    "learning_recommendations": true,
    "analytics_enabled": true
  }
}
```

### Customize for Your Needs

- **Edit agents**: Modify `agents/*.md` files
- **Add skills**: Create new skill files in `skills/[topic]/SKILL.md`
- **Add commands**: Create markdown files in `commands/` directory
- **Customize roadmaps**: Edit agent descriptions and capabilities

## Troubleshooting

### Plugin not loading

1. Verify file structure:
   ```bash
   ls -la .claude-plugin/plugin.json
   ```

2. Check paths in plugin.json are correct

3. Verify markdown files exist:
   ```bash
   ls agents/
   ls commands/
   ls skills/*/SKILL.md
   ```

### Commands not showing up

1. Verify command files in `commands/` directory
2. Check `plugin.json` has command references
3. Restart Claude Code

### Skills not accessible

1. Verify skill files are at `skills/{name}/SKILL.md`
2. Check SKILL.md has proper frontmatter:
   ```markdown
   ---
   name: skill-id
   description: Description here
   ---
   ```

## System Requirements

- **RAM**: 512 MB minimum
- **Disk**: 50 MB for plugin files
- **Claude Code**: Latest version recommended

## Performance

The plugin is lightweight and should load instantly:
- Plugin.json: ~2 KB
- Agents: ~50 KB total
- Skills: ~150 KB total
- Commands: ~30 KB total

## Security & Privacy

- Plugin runs locally, no external calls
- No data collection without your consent
- All hooks can be disabled in hooks.json
- Learning progress stored locally only

## Getting Help

1. **For setup issues**: Check this file
2. **For learning questions**: Use `/browse-agent` to find relevant agent
3. **For specific topics**: Ask the specialized agent
4. **For general info**: Use `/roadmap [role]`

## Updates

To update the plugin:

```bash
cd /path/to/custom-plugin-graphql
git pull origin main
```

Or re-add the plugin:
```bash
claude-plugin add /home/user/custom-plugin-graphql
```

## Next Steps

After installation:

1. Run `/learn` to start learning
2. Select your target role
3. Choose your current level
4. Follow the personalized learning path
5. Use agents for questions
6. Track your progress

---

**Happy Learning! 🚀**
