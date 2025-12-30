# Changelog

All notable changes to this project are documented in this file.

Format: [Keep a Changelog](https://keepachangelog.com/)
Versioning: [Semantic Versioning](https://semver.org/)

## [Unreleased]

### Planned
- Additional specialized agents
- Extended skill library
- Automated testing integration

## [1.1.0] - 2025-12-30

### Added
- **8th Agent**: `prompt-security-agent` for injection defense and safety
- **5 New Skills**: `agent-design`, `fine-tuning`, `multi-modal`, `prompt-injection`, `safety-guardrails`
- **Production-grade upgrades** for all agents:
  - Input/Output schemas (type-safe)
  - Error handling patterns with fallback strategies
  - Token optimization configurations
  - Troubleshooting sections with debug checklists
  - Research references for each technique
- **Comprehensive skill content**:
  - Parameter schemas with validation
  - Core patterns with concrete examples
  - Integration points between skills
  - Troubleshooting tables

### Changed
- Upgraded all 8 agents to production-grade standards
- Expanded all 12 skills with comprehensive documentation
- Fixed Agent 08 metadata (added domain, skills, triggers)
- Updated agent naming consistency (removed numeric prefixes in names)
- Improved skill bonding references

### Fixed
- Agent 08 missing `domain`, `skills`, and `triggers` fields
- Inconsistent agent references in skill bondings
- README agent/skill counts (7→8 agents, 7→12 skills)

## [1.0.0] - 2025-12-29

### Added
- Initial release
- SASMP v1.3.0 compliance
- EQHM enabled for all agents
- Golden Format skills (7 full structure)
- Basic skill definitions (5 minimal)
- 1 command: `/prompt-review`
- Protective LICENSE

---

**Maintained by:** Dr. Umit Kacar & Muhsin Elcicek
