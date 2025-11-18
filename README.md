# Demo Project
Project: demo_wordpress \
  Built by: AmyCN1 \
  Framework: WordPress CMS \
  Date: 11/18/2025

Deployment Platforms: \
Website, Mobile App, IoT, VoiceAssistants, Kiosks, eCommerce Platforms

# Project Overview & Architecture
  A scalable, modern Headless WordPress CMS solution built on the LAMP stack and hosted on AWS Lightsail (with easy upgrade path to EC2/RDS)
  
- Backend - LAMP Stack
  - thisBuild: Ubuntu 24.04 LTS, Apache 2, PHP 8.3, MariaDB 15.1 (LAMP stack)
  - Alternative: DebianOS, Nginx, PHP, MariaDB (LEMP stack)

- Frontend - Headless WordPress
  - thisBuild: Headless WordPress + React/Vue/Next.js (multi platforms depolyment PWAs)
  - Alternative: Traditional WordPress themes or Gutenberg/Full-Site Editing (Block Themes) 

  Current Frontend Content: Placeholder / Not included (available as custom development upon request)
  
- Serverend - Infrastructure & DevOps
  - Server: AWS Lightsail (easily upgradable to EC2)
  - DNS Management: AWS Route53
  - Load Balancing: Not currently implemented (available on request – supports multi-region & high-availability setups)
  - Containerization: Docker (available on request)
  - Orchestration: Amazon EKS (Kubernetes) (available on request)
  - Storage: Amazon S3 buckets (for media, backups, and static assets)

- Team Collaboration & Environments  \
    Fully separated Development and Production environments  \
    Git-based workflow support (can be integrated)  \
    CI/CD pipeline setup available on request

- User Authentication & Access Control  \
    Role-based access control (RBAC) using native WordPress user roles, custom user capabilities and permissions upon request  \
    Enterprise-ready authentication options:  \
    SSO (Single Sign-On) via SAML / OAuth 2.0  \
    Integration with AWS IAM, Azure AD, or on-premise Active Directory  \
    Granular user group policies for Internal Staff vs External Customers

AmyCN1's Notes: This architecture is fully scalable, secure, and ready for enterprise or high-traffic use cases. \

# To Do List: \
  Next build good practices with GitHub Action and Travis CI for code validation
