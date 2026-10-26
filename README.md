# fluxd releases

Release artefacts for **fluxd**, the autonomous Linux performance-optimization platform: the
installer, packages (deb/rpm), static binaries, the Helm chart, SBOMs and signatures. The
container images are at `ghcr.io/olivercheok20/fluxd-{agent,control,operator}`, the chart at
`oci://ghcr.io/olivercheok20/charts/fluxd`.

Install (every host, one line — the control plane address and enrollment token come from
your fluxd console):

    curl -fsSL https://github.com/olivercheok20/fluxd-releases/releases/download/v1.0.0-rc.1/install.sh | sudo FLUXD_CONTROL_ADDR=https://CONTROL:50051 FLUXD_ENROLL_TOKEN=TOKEN sh

Every asset is listed in `SHA256SUMS` and signed with cosign (`cosign.pub` is in the release).
