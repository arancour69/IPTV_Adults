# Project Structure

This document describes the organization of the IPTV_Adults repository.

## 📁 Directory Structure

```
IPTV_Adults/
├── .github/                           # GitHub configuration
│   ├── ISSUE_TEMPLATE/                # Issue templates
│   │   ├── bug_report.md              # Bug report template
│   │   ├── feature_request.md         # Feature request template
│   │   └── question.md                # Question/help template
│   ├── workflows/                     # GitHub Actions workflows
│   │   ├── validate-playlists.yml     # Validate M3U8 format
│   │   ├── generate-stats.yml         # Generate repository statistics
│   │   ├── check-links.yml            # Check documentation links
│   │   ├── update-readme.yml          # Update README with stats
│   │   └── welcome.yml                # Welcome new contributors
│   ├── pull_request_template.md       # PR template
│   ├── link-check-config.json         # Link checker config
│   └── workflows/
│
├── playlists/                         # M3U8 playlist files
│   ├── AdultsHD_1                     # Playlist 1
│   ├── AdultsHD_2                     # Playlist 2
│   ├── AdultsHD_3                     # Playlist 3
│   ├── AdultsHD_4                     # Playlist 4
│   ├── AdultsHD_5                     # Playlist 5
│   └── README.md                      # Playlists directory guide
│
├── docs/                              # Documentation
│   └── README.md                      # Docs directory guide
│
├── README.md                          # Main project documentation
├── SUPPORT.md                         # FAQ and troubleshooting
├── CONTRIBUTING.md                    # Contribution guidelines
├── CHANGELOG.md                       # Version history
├── LICENSE                            # Project license
├── .markdownlintrc                    # Markdown linting rules
├── .github/                           # GitHub configuration (see above)
│
└── [Archived Playlists]/             # Legacy files (optional)
    ├── AdultsHD_1-old                 # Backup of older versions
    └── AdultsHD_2-old
```

## 📋 File Organization Guide

### Root Level Files
- **README.md** - Main documentation entry point
- **SUPPORT.md** - FAQ, troubleshooting, and support resources
- **CONTRIBUTING.md** - Guidelines for contributors
- **CHANGELOG.md** - Version history and updates
- **LICENSE** - Project license (CC0 1.0 Universal)

### `.github/` Directory
- **ISSUE_TEMPLATE/** - Templates for issues:
  - `bug_report.md` - For broken streams
  - `feature_request.md` - For stream suggestions
  - `question.md` - For general help
- **workflows/** - GitHub Actions automation:
  - `validate-playlists.yml` - Validates M3U8 format
  - `generate-stats.yml` - Generates repository statistics
  - `check-links.yml` - Checks documentation links
  - `update-readme.yml` - Updates README with stats
  - `welcome.yml` - Welcomes new contributors
- **pull_request_template.md** - Template for pull requests
- **link-check-config.json** - Configuration for link checker

### `playlists/` Directory
- Contains all M3U8 playlist files
- Each file is a complete playlist with multiple streams
- README.md provides usage instructions
- Files are organized by quality and type

### `docs/` Directory
- Additional documentation
- Configuration guides
- Links to all documentation resources

## 🔄 File Flow

```
Issue/PR Created
    ↓
GitHub Action Triggered
    ↓
Template Applied
    ↓
Validation Run
    ↓
Stats Generated
    ↓
Comment Posted
    ↓
Welcome Message Sent
    ↓
README Updated (if needed)
```

## 🎯 Best Practices

### When Adding Playlists
1. Place M3U8 files in `playlists/` directory
2. Follow M3U8 format standards
3. Use descriptive filenames
4. Update `playlists/README.md` if needed
5. Changes trigger automatic validation

### When Updating Documentation
1. Edit files in root directory or `docs/`
2. Follow Markdown standards
3. Update cross-references
4. Link checker will validate URLs
5. README stats auto-update

### When Contributing Code
1. Follow issue/PR templates
2. Make focused, single-purpose changes
3. Include clear commit messages
4. Pass all automated checks
5. Respond to review comments

## 🤖 Automated Processes

### GitHub Actions Workflows

**Validate Playlists** (`validate-playlists.yml`)
- Runs on playlist file changes
- Checks M3U8 format
- Validates stream URLs
- Posts status comments

**Generate Statistics** (`generate-stats.yml`)
- Runs weekly and on playlist changes
- Counts total channels
- Calculates file sizes
- Generates stats.json

**Check Links** (`check-links.yml`)
- Runs on documentation changes
- Validates all markdown links
- Checks for broken URLs
- Runs markdown linting

**Update README** (`update-readme.yml`)
- Triggered by stats generation
- Updates statistics sections
- Auto-commits changes
- Keeps README current

**Welcome Contributors** (`welcome.yml`)
- Runs on new issues/PRs
- Posts welcome message
- Provides helpful links
- Encourages participation

## 📖 Documentation Flow

```
User Visits Repo
    ↓
Sees Main README
    ↓
Finds Links to:
├─ SUPPORT.md (FAQ)
├─ CONTRIBUTING.md (How to Help)
├─ CHANGELOG.md (What's New)
├─ playlists/README.md (Playlist Info)
└─ docs/README.md (Config)
```

## 🔐 Access & Permissions

- **Public read access** - Everyone can view
- **Clone/Download** - Everyone can clone
- **Issues/Discussions** - Everyone can participate
- **Pull Requests** - Everyone can contribute
- **Merging** - Maintainers only

## 🔄 Version Control

- **Main Branch** - Stable, production-ready
- **Feature Branches** - For new features
- **Bug Fixes** - Direct to main (if minor)
- **Major Changes** - Via pull requests

## 📊 Statistics Tracking

Generated statistics include:
- Number of playlists
- Total file size
- Number of channels
- Last update timestamp
- Per-playlist breakdown

Stats are stored in `stats.json` and displayed in README.

## 🎓 Learning Resources

New to GitHub? Check these:
- [GitHub Guides](https://guides.github.com/)
- [How to Fork](https://guides.github.com/activities/forking/)
- [Create Pull Requests](https://docs.github.com/en/pull-requests)
- [M3U8 Format](https://en.wikipedia.org/wiki/M3U)
- [IPTV Standards](https://www.iptv-org.github.io/)

---

**Questions?** Check [SUPPORT.md](../SUPPORT.md) or open an [issue](../../issues)

**Want to help?** See [CONTRIBUTING.md](../CONTRIBUTING.md)
