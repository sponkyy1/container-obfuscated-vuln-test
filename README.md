# 🧪 Obfuscated Vulnerability Testing in Container Scanners

This repository contains a set of experiments to evaluate the limitations of signature-based vulnerability scanners (Trivy, Grype) in detecting obfuscated vulnerabilities.

## 🔍 Objectives

- Test how scanners behave when vulnerable components are:
  - Renamed
  - Moved to non-standard paths
  - Packed into archives
  - Stripped of debug info

- Compare results with runtime tracing via eBPF (Tracee)

## 📁 Structure

- `Dockerfiles/`: Test containers with different obfuscation scenarios
- `scans/`: Trivy and Grype outputs
- `tracee/`: Runtime syscall logs for detecting executions missed by scanners
- `.github/workflows/scan.yml`: GitHub Actions pipeline to automate scans

## 📖 Article

See [`article.md`](./article.md) for the full paper draft (in progress).