# Security Policy

## Scope

The LLM Research Wiki is a template made of plain markdown files and folders. It has **no backend, no database, no embeddings, no executable code, and no network services**. The operational logic lives in `CLAUDE.md`, which is read by [Claude Code](https://claude.ai/code) at runtime on your own machine.

Because of this, the usual software attack surface is very small. The realistic concerns are:

- **Prompt content in `CLAUDE.md` or page templates** that could cause an LLM agent to behave in unintended ways (for example, instructions that lead it to modify or delete `raw/` source files, which it should never do).
- **Secrets accidentally committed** into the template (none should ever be — this repo holds no credentials).

## Reporting a vulnerability

If you find an issue that fits the above — or anything else you believe is a security concern in the template — please report it privately rather than opening a public issue:

- Use GitHub's **[private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability)** ("Report a vulnerability" under the Security tab), or
- Email **paulo.deassis@orpheusinstituut.be**

Please include what you found, how to reproduce it, and the impact you have in mind. I'll acknowledge within a reasonable time and credit you in any fix unless you'd prefer otherwise.

## A note for forkers

Your own working wiki will contain your sources and notes. Treat your fork's `raw/` and `wiki/` folders with the same care you'd give any private research material — review what you commit before making a fork public.
