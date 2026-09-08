# Changelog

## v0.28.9-rel.0

### Changes

- Update Flannel to 0.28.9 and its CNI installer to 1.9.1-flannel3.
- Remove obsolete PodSecurityPolicy resources and Windows manifests/tasks.
- Modernize installation and health probes while retaining VXLAN/host-gw and the existing kube-system namespace.
- Require Ansible core 2.21 and Linux.
- Replace legacy CI tooling with pinned actions, uv-managed Python 3.14.7 and locked dependencies.
- Add pre-commit YAML/file checks, ansible-lint, actionlint, zizmor.

### Upgrade notes

This is a breaking modernization of the previous release. Review custom variables
and templates before upgrading. Existing Kubernetes clusters must upgrade one
minor version at a time; this role is not a shortcut from the old 1.24 baseline.
Configuration and role tests do not certify a full Ubuntu/Flatcar HA cluster rollout.
