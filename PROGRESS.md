# Progress

> Cross-session memory for this project. Updated by Claude Code.
> Recent entries at bottom. Older entries archived to PROGRESS_ARCHIVE.md.

## 2026-03-08

- **Removed**: Deprecated models from all 3 catalogs — Gemini (gemini-2.5-pro, gemini-2.0-flash, gemini-2.0-flash-lite), OpenAI (o3-mini, gpt-4.1), OpenRouter (12 models including claude-opus-4.5/4.1, sonnet-4.5/4.1, haiku-3.5, llama-3-70b, perplexity/sonar)
- **Fixed**: Updated 23 test files + conftest.py replacing all references to removed models with current equivalents (o3-mini→o4-mini, gpt-4.1→gpt-5, gemini-2.5-pro→gemini-3.1-pro, etc.)
- **Fixed**: Stale model references in docstrings (conversation_memory.py, dial.py, base_tool.py) and schema comments
- **Changed**: conftest.py DEFAULT_MODEL from gemini-2.5-flash to gemini-3-flash-preview; added restriction service cache reset to prevent cross-test pollution
- **Blocked**: `git push` — permission denied to BeehiveInnovations/zen-mcp-server.git (needs SSH or token auth)
- **Next**: Rename Gemini flash models (flash→3.0-flash, flash-lite→3.1-flash-lite per user request); fetch live OpenRouter model data via API; re-record 2 cassette-based integration tests

## 2026-03-15

- **Built**: Added gemini-3.1-flash-lite-preview to Gemini catalog with flash-lite/flashlite aliases
- **Changed**: Renamed flash friendly name to "Gemini 3.0 Flash", added 3.0-flash alias
- **Changed**: Upgraded OpenRouter pro from gemini-3-pro-preview → gemini-3.1-pro-preview (matches live API)
- **Changed**: Simplified OpenRouter catalog from 18 → 9 models (one best per provider). Added kimi-k2.5, glm-5, qwen3.5-397b. Removed all duplicate OpenAI/Gemini models available natively, mistral, deepseek-r1
- **Fixed**: Updated 24+ test files for simplified OpenRouter catalog
- **Decided**: Fork workflow — push to github.com/amiramir/pal-mcp-server (fork of BeehiveInnovations repo)
- **Next**: Re-record 2 cassette-based integration tests; consider adding gpt-5.4-pro to OpenAI native catalog
