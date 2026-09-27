# OpenShift Pricing Compare

Single-page tool comparing **Red Hat OpenShift on OCI (BYOL)** with managed OpenShift on
**AWS (ROSA)**, **Azure (ARO)**, **Google Cloud (OSD)** and **IBM Cloud (ROKS)**.

Open `index.html` in a browser (no build, no dependencies).

## Inputs
- Master / infra / worker node counts
- VM vs bare metal (bare metal only for infra & worker nodes)
- OCI shape, OCPUs and memory per node (other clouds get the equivalent vCPU = 2 × OCPU)
- Persistent volumes: count, size, target IOPS and MB/s per volume; boot disk per node
- Red Hat subscription cost for OCI BYOL (per 2-core or per bare-metal socket pair)

## Output
Monthly / annual / 3-year cost per provider, broken down by masters, infra, workers,
OpenShift fee/subscription and storage, plus % delta vs OCI and the equivalent shapes/tiers.

## Notes
- All rates are indicative on-demand list prices (US) and editable in the **Rate card** panel.
- Only managed offerings are modelled for the hyperscalers; BYOL scenarios are planned.
- Excludes egress, load balancers, support and commitment discounts.

## Per-cloud choices
Region (only regions where each OpenShift offering is available), shape per node role, and
storage type with its own performance knobs: OCI VPU (0–120), AWS gp3/io2/io1 IOPS and throughput,
Azure Premium SSD v2 / Ultra Disk IOPS and MB/s, Google Hyperdisk IOPS and throughput, IBM sdp/custom IOPS.
