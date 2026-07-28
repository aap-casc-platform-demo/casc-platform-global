# casc-platform-global

Platform AAP desired-state configuration

## Usage

Place YAML files in the `base/` directory using the appropriate resource type
subdirectory (e.g., `base/projects/`, `base/templates/`). Environment-specific
overrides go in `<env>/` directories (e.g., `dev/`, `prd/`).

The CasC dispatcher will automatically pick up and apply these configurations
to AAP when the CI/CD pipeline triggers.

### Example

```yaml
---
platform:
  - name: example-resource
    description: Replace with your actual configuration
```

## CI/CD Pipeline

This repository includes a thin CI/CD caller that triggers the platform's
shared CasC pipeline on push and pull request events. The pipeline validates
YAML files and triggers the dispatcher Job Template in AAP.

## Part of the AAP Multi-Tenant CasC Framework

This repository is managed by the **aap-casc-platform-demo** platform team as part
of the AAP Multi-Tenant CasC Framework. See the
[aap-casc-engine](../aap-casc-engine) repository
for full documentation.
