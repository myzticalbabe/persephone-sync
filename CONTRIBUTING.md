# Contributing to Persephone Sync

## How to Contribute

### Reporting Issues
- Use the bug report template (.github/ISSUE_TEMPLATE/bug_report.yml)
- Include reproduction steps, expected vs actual behavior
- Specify Python version, OS, and persephone-sync version

### Pull Request Process
1. Fork the repository
2. Create a feature branch from `main`
3. Make your changes with tests
4. Ensure all tests pass: `python -m pytest -v`
5. Update CHANGELOG.md
6. Submit PR with description of changes

### Coding Conventions
- **Stdlib-first**: Prefer stdlib over external dependencies
- **Cross-platform**: Test on Windows, Linux, macOS
- **Docstrings**: All public methods must have docstrings with Args/Returns
- **Type hints**: Use type annotations for all public APIs

### Test Organization
```
tests/
  test_sync_*.py      # Sync functionality tests
  test_robocopy_*.py  # Robocopy tests
  test_rsync_*.py     # Rsync tests
  test_integrity_*.py # Integrity verification tests
```

### Running Tests
```bash
# Run all tests
python -m pytest tests/ -v

# Run with coverage
python -m pytest --cov=persephone_sync tests/ -v
```

### Pull Request Checklist
- [ ] Tests written and passing
- [ ] Docstrings added for public APIs
- [ ] Type hints added
- [ ] CHANGELOG.md updated
- [ ] No breaking changes without version bump
- [ ] Tested on Windows and Linux (WSL2)