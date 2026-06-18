# Sovereign Family OS

The sovereign model keeps raw sensitive data in family-controlled systems whenever possible. The portal may store metadata, preferences, connector state, generated summaries, and audit events, but should avoid full raw document, photo, finance, password, medical, and legal datasets by default.

Deployment modes:

- Local Sovereign Node: Docker Compose, local network, VPN/Tailscale, self-hosted services.
- Hybrid Sovereign: Vercel portal, Supabase metadata, self-hosted raw data, scoped MCP gateway.
- Hosted Convenience: SaaS-like access with limited sensitive storage and clear export paths.

