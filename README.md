# DevOps Repository

This repository contains Kubernetes deployment configurations for all services.

## How It Works

The deployment files in this repository are **automatically synchronized** from individual project repositories. When changes are pushed to the `main` or `staging` branches of individual repos, a CI/CD pipeline automatically commits the updated `k8s/` configurations to this DevOps repository.

This ensures that:

- Deployment configurations stay in sync with their respective codebases
- Developers can manage k8s configs alongside their application code
- Changes are versioned and traceable back to their source

## Do NOT Modify Directly

The following directories are auto-generated and will be **overwritten** by CI/CD pipelines:

- `ExsysBackend/`
- `ExsysFrontend/`
- `GaslightBackend/`
- `GaslightCodeRunner-Evaluation/`
- `GaslightCodeRunner-Tournament/`
- `GaslightFrontend/`
- `GroupSchedulerBackend/`
- `GroupSchedulerFrontend/`
- `LifeTrackerBackend/`
- `LifeTrackerFrontend/`

**To modify these configurations**, edit the `k8s/` folder in the respective project repository.

## Can Be Modified Directly

The following directories are managed directly in this repository:

- `Redis/` - Shared Redis deployment configuration

These are shared infrastructure components not tied to a specific application repository.
