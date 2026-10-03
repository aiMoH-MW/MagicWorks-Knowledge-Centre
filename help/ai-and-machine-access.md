---
description: "Machine-readable access to the MagicWorks Knowledge & Resource Centre for AI tools, agents and retrieval systems."
---

# AI and machine-readable access

The MagicWorks Knowledge & Resource Centre is designed for both human readers and machine retrieval.

After publication, approved public knowledge is available through GitBook's machine-readable formats in addition to the normal web interface.

## LLM discovery

At the custom knowledge-domain root:

* `/llms.txt` provides an AI-oriented map of the published knowledge.
* `/llms-full.txt` provides the published site content in a consolidated text-friendly form.
* Individual published pages can also be requested in Markdown by adding `.md` to the page URL.

## MCP access

The read-only published-docs MCP endpoint is:

`https://knowledge.magicworksitsolutions.com/~gitbook/mcp`

This endpoint is intended for AI tools and agents that support the Model Context Protocol and need to search or retrieve the latest published MagicWorks knowledge.

## Scope

Machine-readable access includes only content intentionally published through this knowledge centre.

It does not make repository-only governance files, credentials, confidential client material or internal operating documents public.

## Source-of-truth principle

The GitHub repository is the maintained source for the public knowledge content, and Git Sync carries approved updates into GitBook.

The main MagicWorks website remains the canonical commercial destination for services and enquiries.
