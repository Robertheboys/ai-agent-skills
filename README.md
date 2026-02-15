# 🧠 AI Agent Skills Collection

> **37 production-ready skills** for AI coding assistants — covering marketing, CRO, SEO, automation, video, design, and more.

These skills are modular instruction sets that extend the capabilities of AI agents (Claude, Gemini, etc.) running in coding environments like Cursor, Windsurf, or VS Code. Think of them as "expert knowledge packs" — each one turns your AI assistant into a specialist.

---

## 📦 What Are Skills?

Skills are folders containing a `SKILL.md` file (with YAML frontmatter + detailed instructions) and optional supporting files like references, templates, and scripts. When an AI agent encounters a task matching a skill's description, it loads the instructions and acts as a domain expert.

**In simple terms:** it's like giving your AI assistant a manual on exactly how to be an expert in a specific area.

```
skills/
├── copywriting/
│   └── SKILL.md          ← Main instruction file
├── seo-audit/
│   ├── SKILL.md
│   └── references/       ← Supporting resources
│       ├── ai-writing-detection.md
│       └── aeo-geo-patterns.md
└── ...
```

---

## 🚀 Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/YOURUSERNAME/ai-agent-skills.git
```

### 2. Copy skills to your project

Copy the skills you need into your project's `.agents/skills/` directory (or `.claude/skills/` depending on your setup):

```bash
# Copy all skills
cp -r ai-agent-skills/* your-project/.agents/skills/

# Or copy individual skills
cp -r ai-agent-skills/copywriting your-project/.agents/skills/
cp -r ai-agent-skills/seo-audit your-project/.agents/skills/
```

### 3. Use them!

Your AI agent will automatically detect and use the relevant skill when you ask related questions. For example:

- *"Write copy for my landing page"* → triggers `copywriting`
- *"Audit the SEO of my site"* → triggers `seo-audit`
- *"Create an A/B test for this"* → triggers `ab-test-setup`

---

## 📋 Skills Catalog

### 🎯 Marketing & Growth

| Skill | Description |
|-------|-------------|
| **[copywriting](./copywriting/)** | Write or improve marketing copy for any page — homepage, landing, pricing, features |
| **[copy-editing](./copy-editing/)** | Systematic editing of existing marketing copy through multiple focused passes |
| **[content-strategy](./content-strategy/)** | Plan content strategy, decide topics, build topic clusters |
| **[social-content](./social-content/)** | Create and optimize social media content for LinkedIn, Twitter/X, Instagram, TikTok |
| **[email-sequence](./email-sequence/)** | Create drip campaigns, nurture sequences, onboarding emails, lifecycle emails |
| **[launch-strategy](./launch-strategy/)** | Plan product launches, feature announcements, go-to-market strategies |
| **[marketing-ideas](./marketing-ideas/)** | 139 proven marketing approaches organized by category |
| **[marketing-psychology](./marketing-psychology/)** | 70+ mental models and psychological principles for marketing |
| **[paid-ads](./paid-ads/)** | Campaign strategy for Google Ads, Meta, LinkedIn, Twitter/X |
| **[referral-program](./referral-program/)** | Design and optimize referral & affiliate programs |
| **[competitor-alternatives](./competitor-alternatives/)** | Create comparison and alternative pages for SEO & sales |
| **[product-marketing-context](./product-marketing-context/)** | Create a shared context document that other marketing skills reference |
| **[free-tool-strategy](./free-tool-strategy/)** | Plan and build free tools for lead generation and SEO |

### 📈 Conversion Rate Optimization (CRO)

| Skill | Description |
|-------|-------------|
| **[page-cro](./page-cro/)** | Optimize any marketing page for conversions — homepage, landing, pricing |
| **[signup-flow-cro](./signup-flow-cro/)** | Reduce friction and boost signup/registration completion rates |
| **[onboarding-cro](./onboarding-cro/)** | Optimize post-signup onboarding, user activation, time-to-value |
| **[form-cro](./form-cro/)** | Optimize lead capture, contact, demo request, and checkout forms |
| **[popup-cro](./popup-cro/)** | Create and optimize popups, modals, slide-ins, exit intents |
| **[paywall-upgrade-cro](./paywall-upgrade-cro/)** | Optimize in-app paywalls, upgrade screens, upsell modals |
| **[ab-test-setup](./ab-test-setup/)** | Plan, design, and implement A/B tests and experiments |
| **[pricing-strategy](./pricing-strategy/)** | Pricing decisions, tier structure, packaging, freemium strategy |

### 🔍 SEO & Technical

| Skill | Description |
|-------|-------------|
| **[seo-audit](./seo-audit/)** | Full SEO audits — technical, on-page, content quality, E-E-A-T |
| **[schema-markup](./schema-markup/)** | Implement JSON-LD structured data for rich results |
| **[programmatic-seo](./programmatic-seo/)** | Create SEO pages at scale using templates and data |
| **[analytics-tracking](./analytics-tracking/)** | Set up GA4, GTM, conversion tracking, event tracking, UTM parameters |

### 🤖 Automation & AI

| Skill | Description |
|-------|-------------|
| **[n8n-builder](./n8n-builder/)** | Generate complete n8n workflow JSON files |
| **[n8n-node-configuration](./n8n-node-configuration/)** | Node configuration guidance with property dependencies |
| **[n8n-workflow-patterns](./n8n-workflow-patterns/)** | Proven architectural patterns from real n8n workflows |
| **[prompt-engineering-patterns](./prompt-engineering-patterns/)** | Advanced prompt engineering for production LLM systems |

### 🎨 Visual & Video

| Skill | Description |
|-------|-------------|
| **[ai-image-generation](./ai-image-generation/)** | Generate images with FLUX, Gemini, Grok, Seedream via inference.sh |
| **[ai-marketing-videos](./ai-marketing-videos/)** | Create marketing videos with Veo, Seedance, Wan, Kokoro voiceover |
| **[baoyu-cover-image](./baoyu-cover-image/)** | Generate article cover images with 5 design dimensions |
| **[remotion-best-practices](./remotion-best-practices/)** | Best practices for Remotion — video creation in React |
| **[web-design-guidelines](./web-design-guidelines/)** | Review UI code for Web Interface Guidelines compliance |

### 🧩 Utility & Discovery

| Skill | Description |
|-------|-------------|
| **[brainstorming](./brainstorming/)** | Creative exploration before any implementation work |
| **[business-analyst](./business-analyst/)** | Product discovery, stakeholder interviews, requirements analysis |
| **[find-skills](./find-skills/)** | Discover and install new agent skills from the community |

---

## 🔗 How Skills Connect

Many skills reference each other. For example:

```
copywriting ←→ copy-editing        (write → review)
seo-audit ←→ schema-markup         (diagnose → implement)
signup-flow-cro → onboarding-cro   (signup → activation)
page-cro ←→ ab-test-setup          (optimize → test)
launch-strategy → email-sequence   (launch → nurture)
content-strategy → social-content  (plan → distribute)
```

The `product-marketing-context` skill creates a shared context document (`.claude/product-marketing-context.md`) that most marketing skills automatically check before asking questions. **Set this up first** to avoid repeating information.

---

## 📁 Directory Structure

Each skill follows this structure:

```
skill-name/
├── SKILL.md              # Required: Main instructions with YAML frontmatter
├── references/           # Optional: Supporting documents, examples
│   └── *.md
├── rules/                # Optional: Detailed rules (e.g., Remotion)
│   └── *.md
├── scripts/              # Optional: Helper scripts
└── examples/             # Optional: Reference implementations
```

### SKILL.md Format

```yaml
---
name: skill-name
version: 1.0.0
description: "When to use this skill. Trigger phrases: 'keyword1,' 'keyword2,' etc."
---

# Skill Title

Instructions, frameworks, checklists, and examples...
```

---

## 🛠 Creating Your Own Skills

1. Create a new folder: `skills/my-new-skill/`
2. Add a `SKILL.md` file with YAML frontmatter
3. Write clear instructions with:
   - **When to use** the skill
   - **Initial assessment** questions
   - **Frameworks and checklists**
   - **Output format** expectations
   - **Related skills** references
4. Add `references/` folder for supporting docs if needed
5. Submit a PR!

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

- **Add new skills** — Follow the structure above
- **Improve existing skills** — Fix errors, add examples, expand coverage
- **Add references** — Supporting documents for existing skills
- **Report issues** — Missing triggers, unclear instructions, etc.

### Guidelines

- Keep skills focused on one domain
- Write clear trigger descriptions in the YAML frontmatter
- Include practical examples and checklists
- Reference related skills when appropriate
- Test with your AI agent before submitting

---

## 📄 License

MIT License — Use freely in your projects, modify as needed, share with others.

---

## ⭐ Star this repo if you find it useful!

These skills represent hundreds of hours of marketing, SEO, CRO, and automation expertise distilled into AI-consumable instructions. If they help you, consider starring the repo and sharing it with others.

---

*Built with ❤️ by [BitsBlaze](https://github.com/YOURUSERNAME) — Making AI agents smarter, one skill at a time.*
