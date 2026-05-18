# Product Overview: ReguCheck

## 1. What is ReguCheck?

**ReguCheck** is a simple compliance screening tool. It allows users to paste raw regulatory text (such as tax bulletins, policy announcements, or legal updates), select an applicable category, and immediately see if the text contains predefined high-priority compliance keywords.

## 2. Core Functional Logic

The application evaluates text using a direct keyword-matching system.

### 2.1 Keyword Library

The system monitors three specific categories, each associated with its own set of critical terms:

#### Corporate Tax
- `nexus`
- `withholding`
- `deadline`
- `audit`

#### Labor & Employment
- `overtime`
- `minimum wage`
- `termination`
- `exempt`

#### Environmental Compliance
- `emissions`
- `disposal`
- `permit`
- `hazardous`

### 2.2 Audit Rules

#### Case-Insensitivity
The matching system checks for terms regardless of capitalization (e.g., "NEXUS" and "nexus" are treated the same).

#### Unique Matches Only
The engine looks for unique terms. Multiple occurrences of the exact same word are only counted once.

#### Severity Evaluation
- **0 terms matched**: Low Severity
- **1 to 2 unique terms matched**: Medium Severity
- **3 or more unique terms matched**: High Severity

## 3. Basic System Workflow

The tool operates on a simple, sequential cycle:

```
┌─────────────────────────────────────────┐
│  Input Text & Category Selection        │
└──────────────────┬──────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────┐
│  Scan Text for Category-Specific        │
│  Keywords                                │
└──────────────────┬──────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────┐
│  Calculate Severity Rating              │
│  (Low/Medium/High)                      │
└──────────────────┬──────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────┐
│  Display Flagged Keywords &             │
│  Dynamic Action Directive               │
└─────────────────────────────────────────┘
```

---

**Version**: 1.0  
**Last Updated**: 2026-05-18
