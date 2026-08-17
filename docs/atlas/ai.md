# Atlas AI

Atlas Community includes an optional AI panel that helps you explore and reason
about your landscape in plain language. It is **off until you turn it on**, and
it runs against an AI provider key that **you** supply and that stays inside
your own Atlas instance.

This page documents the two things the in-product help links to: setting the
panel up, and using the chat.

- [Atlas AI setup](#atlas-ai-setup)
- [Atlas AI chat](#atlas-ai-chat)

## Atlas AI setup

**Atlas AI setup** is the one-time step that enables the AI panel for your Atlas
Community instance. Until you complete it, the panel stays disabled and Atlas
makes no calls to any AI provider.

### Consent

Setup begins with an explicit consent step. Nothing is sent to an AI provider
before you accept it. The consent step tells you, in plain terms:

- that enabling AI means asset and landscape context can be sent to the AI
  provider you configure, so it can answer your questions;
- that the feature is optional and can be turned off again;
- that you — not VEV — choose and control the provider and its key.

You must accept consent before a key can be saved or a chat can run.

### Bring your own key (BYOK)

Atlas Community uses a **bring-your-own-key** model: you configure your own AI
provider and paste in your own API key. There is no shared, VEV-hosted model
behind the panel. Setup walks you through:

1. choosing a supported AI provider;
2. entering the API key for that provider;
3. saving the configuration to enable the panel.

### Why the key stays in your own Atlas instance

The provider key is stored **in your own Atlas instance** and used only from
there to call the provider you chose. It is not sent to VEV, and it is not
shared with any other tenant or a central service. This matters because:

- **you keep control** — the credential lives in the deployment you operate, and
  you can rotate or remove it at any time;
- **self-hosting stays self-contained** — a self-hosted Atlas does not depend on
  a VEV-run AI backend to make the panel work;
- **billing is yours** — usage runs against your provider account under your own
  terms, not through VEV.

To turn the feature off, remove the key; the panel returns to its disabled
state.

## Atlas AI chat

**Atlas AI chat** is the conversational panel you use once setup is complete. You
ask questions about your landscape in natural language and get answers you can
act on, with links back to the relevant assets.

### Grounded in your landscape

The chat is **grounded in your own tenant's landscape**. When you ask a
question, Atlas selects the relevant assets and relationships from *your*
catalogue and gives the model that context, so answers reflect what is actually
in your instance rather than generic knowledge. Responses can reference the
specific assets they drew on, so you can follow up in the catalogue.

Because the chat runs on the provider and key you configured in
[Atlas AI setup](#atlas-ai-setup), the same control applies: the context needed
to answer is sent only to the provider you chose, from your own Atlas instance.

### What you can do with it

- Ask what exists in your landscape and how parts relate.
- Get a starting point for an area you are unfamiliar with, with links into the
  catalogue.
- Keep the panel closed or the feature disabled whenever you do not want it —
  it is always optional.
