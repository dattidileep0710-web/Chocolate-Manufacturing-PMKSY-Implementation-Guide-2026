# Contributing Guidelines

## Welcome

Thank you for contributing to the Chocolate Manufacturing PMKSY Implementation Guide 2026. This guide establishes the standards and processes for contributions.

## Governance

All contributions are governed by:
- [AGENTS.md](AGENTS.md) — AI agent operating manual
- [CLAUDE.md](CLAUDE.md) — Claude-specific instructions
- [DOCUMENT_CONTROL.md](DOCUMENT_CONTROL.md) — Document lifecycle
- [VERIFICATION_MATRIX.md](VERIFICATION_MATRIX.md) — Quality requirements
- [STYLE_GUIDE.md](STYLE_GUIDE.md) — Formatting standards

## How to Contribute

### For Human Contributors

1. **Read the Governance Documents**
   Start with AGENTS.md and CLAUDE.md to understand the workflow.

2. **Identify Work**
   - Check [ROADMAP.md](ROADMAP.md) for planned documents
   - Check [OPEN_QUESTIONS.md](OPEN_QUESTIONS.md) for research needs
   - Check [KNOWN_GAPS.md](KNOWN_GAPS.md) for known limitations

3. **Claim Work**
   - Open a GitHub Issue describing the contribution
   - Wait for assignment/approval from Program Manager
   - Create feature branch: `feature/DOC_ID-description`

4. **Create/Modify Document**
   - Follow the Iteration Cycle (AGENTS.md)
   - Use the front matter template (STYLE_GUIDE.md)
   - Write content aligned with PMKSY-First Principle

5. **Self-Verify**
   - Run all 7 verification categories (VERIFICATION_MATRIX.md)
   - Complete verification checklist
   - Attach to PR

6. **Submit PR**
   - Target `develop` branch
   - Include verification checklist
   - Reference related issues

7. **Review & Merge**
   - Minimum 2 reviewer approvals
   - Approver sign-off
   - Squash merge to `develop`

### For AI Agents

Follow the exact workflow in AGENTS.md and CLAUDE.md:
- One document per iteration
- READ → PLAN → CREATE → VERIFY → UPDATE → REPORT → WAIT
- Explicit human approval required between iterations

## Contribution Types

### New Content Documents
- Follow roadmap sequence
- Must include: front matter, citations, cross-references, verification
- Target: APPROVED status

### Corrections/Updates
- PATCH version for fixes
- MINOR version for additions
- MAJOR version for structural changes (requires ACR)

### Research/Clarification
- Add to OPEN_QUESTIONS.md
- Document findings with sources
- Update affected documents when resolved

### Gap Mitigation
- Address items in KNOWN_GAPS.md
- Document workarounds and progress
- Close when resolved

## Quality Standards

Every contribution must:
- [ ] Pass all 7 verification categories
- [ ] Follow STYLE_GUIDE.md
- [ ] Include complete front matter
- [ ] Cite official sources for PMKSY claims
- [ ] Maintain cross-reference integrity
- [ ] Update 00_MASTER_INDEX.md and CHANGELOG.md

## Code of Conduct

### Principles
- **Accuracy First**: Verify before contributing
- **Source Everything**: No unsourced claims about PMKSY
- **Respect Process**: Follow the iteration cycle
- **Collaborate Transparently**: Use issues and PRs for discussion

### Unacceptable
- Bypassing verification
- Adding content without citations
- Modifying governance documents without ACR
- Direct pushes to `main` or `develop`
- Multi-document iterations

## Recognition

Contributors acknowledged in:
- CHANGELOG.md (per contribution)
- CONTACTS.md (active contributors)
- Release notes (major versions)

## Getting Help

- **Process Questions**: Open GitHub Issue with "process" label
- **Content Questions**: Tag domain expert in issue
- **Technical Issues**: Check VERIFICATION_MATRIX.md first
- **Urgent**: Contact Program Manager (see CONTACTS.md)

## License

By contributing, you agree that your contributions will be licensed under the repository license (see LICENSE).