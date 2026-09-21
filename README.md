# Capstone Candidate Workbook: Source, Audit, and Suitability Review

This repository contains the intake audit, safety sanitization, risk assessment, and capstone suitability evaluation for Assignment 3.2. The selected candidate artifact is a sanitized inventory reorder tool used in small business operations.

## Executive Summary
- **Domain:** Retail & Small Business Inventory Management
- **Primary Tool Function:** Tracks stock levels, calculates weekly usage demand, and generates automated replenishment alerts to prevent stockouts.
- **Suitability Score:** **20 / 20** (Strong Capstone Candidate)

## Capstone Documentation Index
1. [One Page Analysis](ONE_PAGE_ANALYSIS.md) — Comprehensive operational context, primary stakeholders, and business impacts.
2. [Workbook Intake Form](WORKBOOK_INTAKE_FORM.md) — Structural profile covering inputs, outputs, and process dependencies.
3. [Sanitization Checklist](SANITIZATION_CHECKLIST.md) — Safety and confidentiality verification protocol.
4. [Initial Risk & Defect Inventory](INITIAL_RISK_AND_DEFECT_INVENTORY.md) — Detailed audit identifying fragile formulas, missing validation, and hard-coded parameters.
5. [Capstone Suitability Checklist](CAPSTONE_SUITABILITY_CHECKLIST.md) — Formal 20-point scope and engineering evaluation.
6. [AI Usage Log](AI_LOG.md) — Disclosure of artificial intelligence assistance used during documentation.

## Core Operational Risks Identified
- **Hard-Coded Parameters:** Multipliers embedded directly in cell calculations rather than externalized parameters.
- **Inconsistent Formula Ranges:** Summary rows missing newly appended inventory items.
- **Missing Data Validation:** Absence of guards against negative stock entries or unhandled data types.

## Future Python Engineering Direction
The proposed Python refactoring will focus on implementing modular parameter configuration, strict input validation using `pytest`, and automated inventory threshold alert logic.