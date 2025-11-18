# Copilot Instructions for demo_wordpress

## Project Architecture

This is a **documentation repository** for a Headless WordPress CMS project. The actual WordPress installation lives on AWS Lightsail servers, NOT in this Git repo.

**Key Architecture Points:**
- **Backend**: LAMP stack (Ubuntu 24.04 LTS, Apache 2, PHP 8.3, MariaDB 15.1) on AWS Lightsail
- **Frontend**: Headless architecture - WordPress backend exposes REST/GraphQL APIs for decoupled frontends
- **Environments**: Separate Dev and Prod AWS Lightsail instances
- **Infrastructure**: AWS Route 53 (DNS), S3 (media/backups), potential Docker/EKS setup

## What's NOT in This Repo

- No WordPress core files (`wp-admin/`, `wp-includes/`, `wp-content/`)
- No PHP code, themes, or plugins
- No `wp-config.php` or database credentials
- No `composer.json`, `package.json`, or build scripts
- Actual WordPress instances are deployed directly on AWS Lightsail servers

## What IS in This Repo

- `README.md`: Comprehensive architecture documentation
- `.history/`: VS Code Local History plugin snapshots of README changes

## Development Workflow

### Documentation Updates
- All changes focus on updating `README.md` with architecture details
- Use markdown formatting with line breaks (`\`) as established in existing content
- Maintain consistent structure: Project metadata → Architecture → Infrastructure → Team/Auth

### Deployment & Infrastructure
- **SSH Access Required**: All WordPress changes happen via SSH to AWS Lightsail instances
- **Environments**: Dev and Prod are completely separate Lightsail instances
- **No CI/CD**: Git-based workflows and CI/CD are "available on request" but not currently implemented
- **S3 Integration**: Media and backups stored in S3 buckets (external to WordPress filesystem)

### Headless WordPress Patterns
When extending this project with frontends:
- Use WordPress REST API (`/wp-json/wp/v2/`) or WPGraphQL for data fetching
- Recommended stack: React/Next.js/Vue for mobile apps or PWAs
- Authentication via JWT tokens for headless API access
- Current frontend is placeholder - custom development needed

## Common Tasks

### Update Architecture Documentation
Edit `README.md` to reflect infrastructure changes, new AWS services, or deployment updates. Follow the existing markdown style with trailing backslashes.

### Plan Frontend Integration
Reference the "Frontend - Headless WordPress" section in `README.md` for technology recommendations. Frontend repos would be separate from this documentation repo.

### Scale Infrastructure
Document upgrades in `README.md`:
- Lightsail → EC2 migration paths
- Load balancing configurations (currently not implemented)
- Docker containerization plans
- EKS orchestration setups

## Project-Specific Conventions

- **Line Break Style**: Use `\` at end of lines for consistent README formatting
- **Availability Markers**: Features marked "available on request" indicate future/optional capabilities
- **Environment Separation**: Always distinguish between Dev and Prod when discussing deployments
- **AWS-Centric**: All infrastructure decisions reference AWS services (Lightsail, Route 53, S3, IAM, EKS)

## Authentication & Access Control

- WordPress RBAC using native user roles (Editor, Author, Contributor, etc.)
- Enterprise SSO via SAML/OAuth 2.0 (configurable but not in this repo)
- Integrations: AWS IAM, Azure AD, or on-premise Active Directory
- Separate policies for Internal Staff vs External Customers

## Key Files

- `README.md`: Single source of truth for project architecture and deployment strategy
- `.history/README_*.md`: Historical snapshots tracking documentation evolution
