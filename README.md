# Svelte 5 Development Skill for Claude Code

A comprehensive skill for [Claude Code](https://claude.com/claude-code) that provides expert guidance on Svelte 5 and SvelteKit development. This skill replaces the need for the Svelte MCP server, saving ~3.3k tokens per request while providing all the essential knowledge you need.

## Why Use This Skill?

- **Token Efficient**: Loads on-demand only when working with Svelte code, vs MCP tools loaded on every request
- **Comprehensive Coverage**: All essential Svelte 5 runes, patterns, and SvelteKit features
- **Best Practices Built-in**: Covers common pitfalls and when to use which approach
- **Real-World Patterns**: Includes SSE, remote functions, form actions, and more
- **Type-Safe**: Covers TypeScript patterns and `$types` usage

## What's Covered

### Svelte 5 Runes
- **$state** - Reactive state with deep reactivity
- **$derived** - Computed values (replaces reactive `$:`)
- **$effect** - Side effects and lifecycle
- **$props** - Component props with TypeScript
- **$bindable** - Two-way binding

### Common Patterns & Pitfalls
- When to use `$derived` vs `$effect`
- Navigation with remote functions (using `goto()`)
- Async operations and form initialization
- Component composition with snippets
- Proper prop handling and mutation rules

### SvelteKit Features
- File-based routing and dynamic routes
- Loading data (universal vs server load functions)
- Form actions and progressive enhancement
- Real-time updates with Server-Sent Events
- Environment variables (public vs private)

### Best Practices
- Effect vs derived decision-making
- Server vs client load functions
- When to use `$bindable` vs callbacks
- Reactive state management patterns

## Installation

### Option 1: Direct Copy (Recommended)

1. Create the skill directory:
```bash
mkdir -p .claude/skills/svelte5-development
```

2. Download the skill file:
```bash
curl -o .claude/skills/svelte5-development/SKILL.md \
  https://raw.githubusercontent.com/splinesreticulating/claude-svelte5-skill/main/SKILL.md
```

3. (Optional) Disable the Svelte MCP server to save tokens:
```bash
# In Claude Code
/mcp
# Then disable the 'svelte' server
```

### Option 2: Git Clone

```bash
# Clone into your project's .claude/skills directory
cd your-project
git clone https://github.com/splinesreticulating/claude-svelte5-skill \
  .claude/skills/svelte5-development
```

## Usage

Once installed, Claude Code will automatically use this skill when you're working with Svelte files or discussing Svelte/SvelteKit topics. You can also explicitly invoke it:

```bash
/svelte5-development
```

### Example Interactions

**Ask about runes:**
> "When should I use $derived vs $effect?"

**Get component help:**
> "How do I create a form with progressive enhancement in SvelteKit?"

**Navigation patterns:**
> "My links aren't working with remote functions enabled"

**Real-time features:**
> "How do I implement Server-Sent Events in SvelteKit?"

## Token Savings

By using this skill instead of the Svelte MCP server:
- **MCP Server**: ~3.3k tokens loaded on every request
- **This Skill**: ~0 tokens until needed, then only loads relevant guidance
- **Savings**: Significant reduction in token usage for non-Svelte work

## When to Re-enable MCP Server

This skill covers 95% of common Svelte 5 and SvelteKit development needs. You might want to temporarily re-enable the Svelte MCP server for:
- Very specific API documentation lookups
- Advanced adapter configurations
- Complex hook implementations
- Migration guides for legacy code

## Compatibility

- **Svelte**: 5.x (covers up to 5.42 features)
- **SvelteKit**: 2.x (includes 2.16+ features like `PageProps`)
- **Claude Code**: All versions with skill support

## Updates

Svelte 5 is actively evolving. This skill was last updated: **November 2025**

Notable recent features covered:
- Svelte 5.25: Direct override of `$derived` values
- Svelte 5.36: Experimental `await` support
- Svelte 5.42: `fork()` API for preloading
- SvelteKit 2.16: `PageProps` and `LayoutProps` types

## Contributing

Found a pattern that should be included? Have a suggestion? Please open an issue or PR!

## Credits

Created by extracting and organizing content from the official [Svelte documentation](https://svelte.dev/docs) and [SvelteKit documentation](https://svelte.dev/docs/kit).

## License

MIT License - See [LICENSE](LICENSE) for details.

## Related Skills

- [Frontend Design](https://github.com/anthropics/claude-code/tree/main/plugins/frontend-design) - Create distinctive, production-grade UIs

---

**Note**: This is a community-created skill for Claude Code. It is not officially maintained by the Svelte or Anthropic teams.
