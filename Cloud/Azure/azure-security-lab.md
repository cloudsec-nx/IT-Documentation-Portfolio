# 🔐 Project: Azure Security Monitoring Lab

> **Type:** Persoonlijk leerproject — Cloud & Security
> **Status:** 🔄 In uitvoering
> **Aanmaakdatum:** 03-05-2026
> **Laatst bijgewerkt:** 03-05-2026

---

## 📋 Voorblad

| Veld | Info |
|---|---|
| **Projectnaam** | Azure Security Monitoring Lab |
| **Type** | Homelab / Cloud Lab |
| **Omgeving** | Microsoft Azure + Lokaal |
| **Auteur** | cloudsec-nx |
| **Status** | 🔄 Fase 1 — In uitvoering |

---

## 🎯 Doel

Een persoonlijke Azure-omgeving opzetten met security monitoring en alerting om praktijkervaring op te doen met Microsoft Defender for Cloud en Microsoft Sentinel. Het project groeit iteratief van een eenvoudige opzet naar een volwassen security monitoring oplossing.

---

## 🗺️ Projectfasen

```
Fase 1          Fase 2              Fase 3
────────────────────────────────────────────
Azure VM    →   Microsoft       →   Zero Trust
+ Defender      Sentinel            + Kubernetes
for Cloud       (SIEM)              + Automatisering
```

---

## 📦 Fase 1 — Azure VM & Defender for Cloud

### Doel
Een Azure VM opzetten, beveiligen met Microsoft Defender for Cloud en basis security alerts configureren.

### Benodigdheden
- Azure account (gratis tier of Pay-as-you-go)
- Azure CLI of Azure Portal toegang
- Basiskennis Azure VNet & NSG

### Architectuur
```
Internet
    │
    ▼
Azure VNet
    │
    ├── NSG (Network Security Group)
    │       └── Inbound rules: RDP/SSH beperkt
    │
    └── Virtual Machine (Windows Server / Ubuntu)
            └── Microsoft Defender for Cloud
                    └── Security alerts & aanbevelingen
```

### Stappen

#### Stap 1 — Resource Group aanmaken
- [ ] Resource Group aanmaken: `rg-security-lab`
- [ ] Regio kiezen: `West Europe`

#### Stap 2 — Netwerk opzetten
- [ ] Virtual Network aanmaken: `vnet-security-lab`
- [ ] Subnet aanmaken: `subnet-lab` (10.0.1.0/24)
- [ ] NSG aanmaken en koppelen
- [ ] NSG regels instellen:
  - RDP (3389) of SSH (22) alleen vanaf eigen IP
  - Alle andere inbound verkeer blokkeren

#### Stap 3 — Virtual Machine aanmaken
- [ ] VM aanmaken (Ubuntu 24.04 of Windows Server 2022)
- [ ] VM grootte: `B1s` (goedkoopste optie)
- [ ] Koppelen aan `vnet-security-lab`
- [ ] Public IP instellen
- [ ] VM verbinden via SSH of RDP

#### Stap 4 — Microsoft Defender for Cloud inschakelen
- [ ] Ga naar Microsoft Defender for Cloud in Azure Portal
- [ ] Defender for Servers inschakelen op de VM
- [ ] Secure Score bekijken
- [ ] Aanbevelingen doorlopen

#### Stap 5 — Security alerts configureren
- [ ] Alert rule aanmaken voor verdachte inlogpogingen
- [ ] Email notificatie instellen
- [ ] Test alert triggeren

### Verwacht resultaat
- Werkende Azure VM met beveiligd netwerk
- Defender for Cloud actief met security score
- Minimaal 1 werkende security alert

---

## 📦 Fase 2 — Microsoft Sentinel (SIEM)

> ⏳ Start na voltooiing Fase 1

### Doel
Microsoft Sentinel toevoegen als SIEM-oplossing voor gecentraliseerde log analyse en geavanceerde alerting.

### Stappen (globaal)
- [ ] Log Analytics Workspace aanmaken
- [ ] Microsoft Sentinel inschakelen
- [ ] Data connectors koppelen (VM, Defender)
- [ ] Analytics rules configureren
- [ ] Dashboard instellen

---

## 📦 Fase 3 — Zero Trust & Automatisering

> ⏳ Start na voltooiing Fase 2

### Doel
Zero Trust principes toepassen en repetitieve taken automatiseren.

### Stappen (globaal)
- [ ] Conditional Access policies koppelen
- [ ] Kubernetes cluster toevoegen
- [ ] Automatisering via Azure scripts
- [ ] Incident response playbooks

---

## 💰 Kosten inschatting

| Resource | Geschatte kosten |
|---|---|
| Azure VM B1s | ~€8-10 per maand |
| Public IP | ~€3 per maand |
| Defender for Cloud (gratis tier) | €0 |
| Microsoft Sentinel | Per GB ingested data |
| **Totaal Fase 1** | **~€10-15 per maand** |

> 💡 **Tip:** Zet de VM uit als je er niet mee werkt — dan betaal je alleen voor opslag.

---

## 📝 Bevindingen & Learnings

> Noteer hier wat je leert tijdens het project.

| Datum | Bevinding | Categorie |
|---|---|---|
| | | |

---

## ⚠️ Problemen & Oplossingen

| Probleem | Oorzaak | Oplossing |
|---|---|---|
| | | |

---

## 🔗 Referenties

- 📖 Microsoft Defender for Cloud docs: https://learn.microsoft.com/nl-nl/azure/defender-for-cloud
- 📖 Microsoft Sentinel docs: https://learn.microsoft.com/nl-nl/azure/sentinel
- 📖 Azure VM quickstart: https://learn.microsoft.com/nl-nl/azure/virtual-machines

---

*Laatst bijgewerkt: mei 2026*
