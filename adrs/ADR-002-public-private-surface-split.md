# ADR-002: Separate public discovery from the private family system

Status: accepted

Date: 2026-07-12

## Context

A public founder story, a private family archive, and a reusable hosted product have different threat models. `noindex` is not authorization. A hidden URL is not a private portal. A family subdomain does not create tenant isolation by itself.

## Decision

Use three surfaces with one portable protocol:

1. Public discovery: `frankx.ai/family` and `frankx.ai/family-intelligence-system` contain only public-safe copy, examples, and downloads.
2. Private pilot: an authenticated German-first Family Intelligence OS deployment for the Riemer-Gorte family. Its final hostname requires DNS and identity review.
3. Reusable product: the `family-intelligence-os` Vercel/self-host template. Each family is a tenant with explicit circles, row-level authorization, scoped encryption, audit, and export.

## Non-negotiables

- Living people are private by default.
- Children are never publicly searchable or used as public demo data.
- A public archive receives redacted, publication-approved artifacts; it never mirrors the private database.
- Authorization is rechecked in server components, route handlers, server actions, workers, and MCP handlers. Next.js proxy is only traffic routing.
- Public repositories contain code, doctrine, schemas, anonymized fixtures, and templates—not family records.

## Consequences

The existing `/familie` route may remain a public-safe archive index, but it is not the private family portal and must not imply that `robots: noindex` makes living-person content private.
