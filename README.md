# KQL Detections

Microsoft Sentinel detection and hunting queries focused on threat detection, adversary tradecraft, and ATT&CK-aligned analytics.

## Purpose

This repository contains KQL detections developed for:

* Threat Detection
* Threat Hunting
* Detection Engineering
* Security Operations
* ATT&CK Coverage Mapping

The goal is to provide high-fidelity analytics suitable for Microsoft Sentinel environments.

---

## Detection Coverage

| Detection | File | ATT&CK Technique | Tactic |
|------------|------|------------------|--------|
| LSASS Memory Access | detections/lsass_memory_access.kql | T1003.001 | Credential Access |
| Defender Tampering | detections/defender_tampering.kql | T1562.001 | Defense Evasion |
| Shadow Copy Deletion | detections/shadow_copy_deletion.kql | T1490 | Impact |

---

## Technologies

* Microsoft Sentinel
* Kusto Query Language (KQL)
* Sysmon
* Windows Event Logs
* MITRE ATT&CK

---

## Repository Structure

```text
detections/
hunts/
investigations/
```

---

## Disclaimer

These detections are created for research, lab validation, and portfolio purposes.
