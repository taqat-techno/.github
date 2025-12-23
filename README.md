# TaqaTechno

**Odoo ERP Solutions & Custom Development**

---

## About Us

TaqaTechno is a technology company specializing in Odoo ERP implementations, customizations, and enterprise solutions. We deliver high-quality software solutions across multiple Odoo versions (14-19) for clients in various industries including property management, disaster relief, e-commerce, and more.

- **Website**: [taqatechno.com](https://www.taqatechno.com/)
- **Email**: info@taqatechno.com
- **Location**: Saudi Arabia

---

## Our Repositories

| Repository | Description |
|------------|-------------|
| `relief_center` | Disaster relief management with MapTiler integration |
| `multi-theming-17` | Multi-website theming for Odoo 17 |
| `taqat-prop` | Property management solutions |
| `plugins` | Shared plugins and utilities |
| `rc-demo` | Demo and testing repository |
| `pearlpixels` | Web design projects |

---

## Development Guidelines

### 1. Branch Protection

| Branch | Rule |
|--------|------|
| `main` | Protected - Requires Team Leader approval |
| `staging` | Protected - Requires team coordination |
| `feature/*` | Your working branch |

**Workflow:**
```
feature/your-task  →  staging  →  main
       ↑                ↑          ↑
   You work here    Team review   TL approval
```

### 2. IDE Standard

**Required**: PyCharm or JetBrains IDE

Why? Unified code formatting prevents merge conflicts.

### 3. Definition of Done

Before marking any task complete:

- [ ] Tested as **Public User**
- [ ] Tested as **Portal User**
- [ ] Tested as **Admin User**
- [ ] Content matches approved design (AR & EN)
- [ ] UI/UX matches approved mockups

### 4. Odoo Code Standards

```
DO                                  DON'T
─────────────────────────────────────────────────────
Use security rules                  Use sudo() everywhere
Theme = website logic               Mix theme & module logic
Module = database logic
XML + publicWidget in themes        Heavy Python in themes
XPath (before/after/inside)         Replace entire views
Odoo translation functions          Hardcoded AR/EN text
```

### 5. Website Development

- All sections must work with **Odoo Website Editor**
- Use **Odoo native components** when possible
- Test in both **edit mode** and **published mode**

### 6. File Structure

```
module_name/
├── __manifest__.py      # Required metadata
├── __init__.py
├── README.md            # Required for custom models
├── controllers/
├── models/
├── views/
├── data/
├── security/
├── i18n/
└── static/
    └── src/
        ├── js/          # No inline scripts
        └── scss/        # No inline styles, no plain CSS
```

### 7. Manifest Requirements

Every module must include:

```python
{
    'name': 'Module Name',
    'version': '17.0.1.0.0',
    'author': 'TaqaTechno',
    'website': 'https://www.taqatechno.com/',
    'support': 'info@taqatechno.com',
    'contributors': [
        'Developer Name <email@taqatechno.com>',
    ],
    # ... rest of manifest
}
```

### 8. Documentation

Every custom model needs a `README.md` with:

- **Purpose**: What does this module do?
- **Models**: List of custom models
- **Workflow**: How does it work?
- **Dependencies**: Required modules

---

## Quick Reference

### Naming Conventions

| Type | Convention | Example |
|------|------------|---------|
| Module | `snake_case` | `relief_center` |
| Model | `dot.notation` | `disaster.location` |
| Field | `snake_case` | `partner_id` |
| XML ID | `module_model_description` | `relief_center_disaster_form` |

### Git Commit Format

```
<type>: <short description>

Types: feat, fix, docs, style, refactor, test
```

**Examples:**
```bash
feat: add disaster location map view
fix: resolve partner validation error
docs: update README with API endpoints
```

### Branch Naming

```
feature/<task-id>-<description>
bugfix/<task-id>-<description>
hotfix/<task-id>-<description>
```

**Examples:**
```
feature/123-add-map-integration
bugfix/456-fix-login-redirect
```

---

## Team

| Role | Responsibility |
|------|----------------|
| **Team Leader** | Approves merges to `main` |
| **Senior Developer** | Reviews PRs, mentors team |
| **Developer** | Feature development, testing |
| **QA** | Testing, bug reporting |

---

## Contact

For questions or support:

- **Technical Issues**: Create an issue in the relevant repository
- **General Inquiries**: info@taqatechno.com

---

*TaqaTechno - Building Better Solutions*