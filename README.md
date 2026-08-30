# Awesome-SSL-Certificate-Lifecycle-Management

## Top SSL Certificate Lifecycle Management Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Certificate Discovery, Issuance, Renewal, Revocation, PKI Automation & Machine Identity*

**Last updated: August 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **SSL/TLS Certificate Lifecycle Management (CLM)**. These systems discover certificates, automate issuance and renewal (often via ACME), enforce policy, and prevent outages from expired certs across machines, apps, and infrastructure.



**Examples** include Keyfactor, Venafi, DigiCert Trust Lifecycle Manager, AppViewX, Sectigo Certificate Manager, Entrust PKI, KeyTalk, Smallstep, Certify The Web, and ZeroSSL (the category leaders).



**Open-source emphasis**: Certificate automation has excellent open tools. **cert-manager**, **step-ca**, **EJBCA**, and ACME clients provide production-grade issuance and renewal, especially for Kubernetes and internal PKI. This section is heavily expanded with these tools.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saashosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms

| Platform | Description | Starting Pricing | Free Tier / Free Trial Limits |
| :--- | :--- | :--- | :--- |
| **[Keyfactor](https://www.keyfactor.com/)** | Enterprise certificate lifecycle and PKI platform (includes EJBCA) — strong AD CS integration, discovery, and full-stack machine identity. | Starts at ~$75,000/year for enterprise platform; cloud marketplace instances via AWS/Azure private offers | 30-day free trial on AWS/Azure Marketplace for EJBCA Enterprise Cloud; open-source EJBCA Community Edition free forever |
| **[Venafi (CyberArk Machine Identity)](https://www.venafi.com/)** | Leading machine identity and certificate management platform for large enterprises — broad integrations and policy-driven CLM. | Starts at ~$150,000/year for enterprise contract; private offers on AWS Marketplace | 30-day free trial for TLS Protect Cloud (includes full domain certificate discovery scan & visibility) |
| **[DigiCert Trust Lifecycle Manager](https://www.digicert.com/)** | DigiCert’s unified CLM and digital trust platform — public and private certificate lifecycle with tight CA integration. | Essentials tier starts at ~$2,500/year (seat-based licensing across Essentials, Advanced, and Premium tiers) | 30-day free trial account available upon request (includes discovery & lifecycle evaluation) |
| **[AppViewX](https://www.appviewx.com/)** | Certificate and crypto automation platform with strong network device support, workflows, and crypto-agility features. | Starts at ~$15,000/year for AVX ONE CLM base deployment / AWS Marketplace private offers | 30-day free trial on AppViewX Cloud & AWS Marketplace; includes unlimited free public SSL discovery scan |
| **[Sectigo Certificate Manager](https://www.sectigo.com/)** | Certificate lifecycle management tied to a major public CA, with automation and CA-agnostic options. | SCM Pro starts at $10.75/month ($129/year) per domain; Wildcard tier at $48.25/month | 30-day free trial (includes discovery scan and up to 5 free 90-day DV certificates; no credit card required) |
| **[Entrust PKI / certificate management](https://www.entrust.com/)** | Enterprise PKI and certificate services for identity and machine trust. | Core PKIaaS bundles start at £6,000/year (~$7,800/year); individual certificates from $24/cert/year | 60-day free trial for Managed PKI upon request; free discovery tools |
| **[KeyTalk](https://www.keytalk.com/)** | Certificate and key management solutions focused on automated delivery and lifecycle. | CKMS platform licenses start at ~€2,500/year (~$2,700/year) based on managed seats/endpoints | 30-day Proof of Concept (PoC) / evaluation trial license with full technical consultation |
| **[Smallstep (Certificate Manager)](https://smallstep.com/)** | Modern certificate automation and private CA platform (commercial offerings built on open step-ca). | Hosted plans start at $3.00/host/month; custom enterprise bundles for advanced scale | Free forever tier for homelabs and small teams (free SaaS Certificate Manager with `step-ca` integration) or 14-day enterprise trial |
| **[Certify The Web](https://certifytheweb.com/)** | Windows-oriented certificate management and ACME automation for IIS and related workloads. | $59.00/year per server license (or $4.99/server/month on Microsoft Azure Marketplace) | Free forever Community Edition (manages up to 5 certificates per server install; community support) |
| **[ZeroSSL](https://zerossl.com/)** | Certificate authority and management tools with ACME support and free/paid certificate options. | Basic plan starts at $9.99/month ($119.88/year); Premium at $52.99/month | Free forever plan (3 90-day certificates via UI; unlimited 90-day certificates via ACME API) |



## Open-Source GitHub Projects

- **[cert-manager](https://github.com/cert-manager/cert-manager)**  

  Kubernetes-native certificate management — automatically provisions and renews TLS certificates from ACME (Let’s Encrypt), Vault, Venafi, and other issuers.



- **[step-ca (Smallstep)](https://github.com/smallstep/certificates)**  

  Open-source private certificate authority and ACME server for automated X.509 and SSH certificates — ideal for internal PKI and short-lived certs.



- **[EJBCA Community](https://www.ejbca.org/)**  

  Open-source enterprise PKI and certificate authority (also the core of Keyfactor’s stack) — full CA capabilities for private PKI.



- **[Let's Encrypt / Certbot and ACME clients](https://certbot.eff.org/)**  

  Free public certificates and the standard ACME protocol clients used everywhere for automated issuance and renewal.



- **[acme.sh and other ACME shell clients](https://github.com/acmesh-official/acme.sh)**  

  Lightweight, portable ACME clients for renewing certificates on diverse hosts without heavy dependencies.



- **[HashiCorp Vault PKI secrets engine](https://www.vaultproject.io/)**  

  Open-source secrets management with dynamic certificate issuance and short TTLs (self-hosted or HCP).



- **[OpenSSL and certificate tooling](https://www.openssl.org/)**  

  Foundational open libraries and CLI for creating, inspecting, and managing certificates and keys.



- **[Certificate discovery open scanners](https://github.com/)**  

  Tools that scan networks and inventories for expiring or misconfigured TLS certificates.



- **[Kubernetes and ingress ACME integrators](https://github.com/)**  

  Controllers and annotations that work with cert-manager for automatic HTTPS on ingresses.



- **[Policy and inventory open scripts](https://github.com/)**  

  Scripts that inventory certificates from load balancers, servers, and secret stores for compliance reporting.



### Additional Strong Open-Source Options

- Running **cert-manager** in every Kubernetes cluster for automatic TLS.

- Deploying **step-ca** as an internal ACME CA for private services and workloads.

- Using **EJBCA** when you need a full open private CA with richer RA and policy features.

- Standardizing on ACME everywhere possible so renewal is automated and CA-agnostic.

- Combining Vault PKI for dynamic, short-lived application certificates.

- Monitoring expiration with open discovery tools and alerting before outages.



**Frameworks for building custom systems**: Issue public certs via **ACME** (Certbot/acme.sh), manage Kubernetes with **cert-manager**, run internal PKI with **step-ca** or **EJBCA**, and store dynamic certs in **Vault**. This stack is fully open and widely production-proven. Commercial CLM platforms (Venafi, Keyfactor, DigiCert TLM, AppViewX, Sectigo, etc.) still lead for enterprise-wide discovery, multi-CA policy, AD CS depth, network device automation, and support for large heterogeneous estates.



## How to Contribute

1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.

- Certificate mismanagement causes outages and security incidents. Always test renewal and revocation procedures. Private CAs require careful root protection and operational discipline. Shorter public certificate lifetimes increase the need for reliable automation — monitor and alert on failures. Open tools must be kept updated and correctly configured.

- This list is not security or compliance advice.



---

**Made for platform, security, and SRE teams who refuse to let certificates expire in production.**

Let's keep TLS automated, short-lived where possible, and under continuous control.
