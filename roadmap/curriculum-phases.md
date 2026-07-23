# Cloud Engineer Academy — Curriculum Phases

Reference curriculum for the academy. Adjust pacing based on `progress-tracker.md`, but
preserve prerequisites and depth — see `CLAUDE.md` for how to teach this, not just what.

## Certifications

AWS certifications are checkpoints inside this curriculum, not a separate track. Each one is
scheduled after the phase material it covers has already been practiced hands-on — the exam
should be a review of things Juan has actually done, not the first exposure to them. Do not
front-load exam prep before the corresponding phase is done; that produces exam-passing without
durable ability, which conflicts with the goal in `CLAUDE.md`.

- **AWS Cloud Practitioner** — after Phase 5 (Cloud fundamentals). Broad-but-shallow overview
  exam; low stakes, confirms the Phase 5 concepts landed.
- **AWS Solutions Architect Associate** — after Phase 7 (Infrastructure as Code). By this point
  IAM, networking, compute, storage, and high availability have been reinforced by building
  real infrastructure with Terraform, not just watching services get clicked through a console.
- **AWS SysOps Administrator Associate** — after Phase 10 (Observability, reliability, and
  security). Chosen over AWS Developer Associate: SysOps matches the operations/support/DevOps
  target roles in Phase 12 far more closely than a developer-focused exam does.

Revisit this list if the target roles shift, but don't add exam-prep time that isn't backed by
a completed phase.

## Phase 1 — Technical foundations

**Computer and operating-system fundamentals**
Hardware/software basics; CPU, memory, storage, processes, files; operating systems;
virtualization; Windows/WSL/Linux relationships; terminal and shell concepts; paths,
filesystems, users, permissions.

**Linux fundamentals**
Navigation; file and directory operations; viewing/editing text; stdin/stdout/stderr;
redirection; pipes; globbing; quoting; environment variables; processes; signals; jobs;
permissions; ownership; users and groups; packages; services; logs; archives; storage; system
information; SSH; basic troubleshooting.
Docs practice: `man`, `--help`, `apropos`, `whatis`, relevant GNU/kernel/distro docs.

**Git and GitHub fundamentals**
Repositories; working tree; staging area; commits; commit history; diffs; branches; merging;
remotes; push/pull; cloning; `.gitignore`; README files; merge conflicts; recovery from common
mistakes; GitHub workflows; issues and pull requests; professional commit messages.
Docs practice: official Git and GitHub documentation.

**Bash and command-line problem solving**
Shell syntax; variables; exit codes; conditionals; loops; functions; arguments; input
validation; text-processing tools; error handling; debugging; reusable scripts. Build small
scripts that solve real administrative problems.

## Phase 2 — Programming and automation foundations

**Python fundamentals**
Values/types; variables; operators; conditionals; loops; functions; collections; files;
exceptions; modules; packages; virtual environments; JSON; APIs; testing; logging; debugging.
Use official Python docs throughout. Build useful automation scripts, not just isolated
exercises.

**Data formats and configuration**
JSON; YAML; CSV; environment variables; configuration files; secrets handling; basic
serialization and validation.

## Phase 3 — Networking foundations

OSI and TCP/IP models; IP addressing (v4/v6); subnets and CIDR; private/public addressing;
routing; switching concepts; ARP; DNS; DHCP; TCP/UDP; ports; HTTP/HTTPS; TLS; NAT; firewalls;
load balancers; proxies; VPN concepts; network troubleshooting.
Tools: `ip`, `ping`, `traceroute`, `ss`, `curl`, `dig`, `nslookup`, `host`, `tcpdump`, `nc`.

## Phase 4 — Systems administration

Linux administration; services and `systemd`; logs and `journalctl`; scheduled tasks; storage
and filesystems; mounting; resource monitoring; package management; SSH configuration; users
and access; backups; basic hardening; troubleshooting methodology. Build repeatable
administration labs.

## Phase 5 — Cloud fundamentals

Primary platform: AWS (unless the tracker says otherwise). Regions/AZs; shared responsibility;
IAM; virtual networks; compute; storage; databases; DNS; load balancing; auto scaling;
monitoring; logging; security groups/network controls; cost awareness; high availability;
backup/DR concepts. Use the provider's official docs; connect every service to architecture,
operations, security, troubleshooting, and cost — not just cert trivia.

Certification checkpoint: AWS Cloud Practitioner exam once this phase's material has been
practiced hands-on (see "Certifications" above).

## Phase 6 — Containers

Container concepts; images; containers; registries; Dockerfiles; layers; volumes; networks;
environment variables; logs; resource management; Docker Compose; image security;
troubleshooting. Use official Docker docs. Build and run real applications, not just demos.

## Phase 7 — Infrastructure as Code

Terraform (or the roadmap's selected tool). Declarative infrastructure; providers; resources;
variables; outputs; state; plan/apply/destroy; modules; remote state; state locking;
dependencies; workspaces; security/secrets; formatting/validation; testing; drift; team
workflows. Learn to read provider resource references independently.

Certification checkpoint: AWS Solutions Architect Associate exam once this phase's material has
been practiced hands-on (see "Certifications" above) — by now IAM, networking, compute,
storage, and HA from Phase 5 have also been reinforced by building real infrastructure here.

## Phase 8 — CI/CD and professional Git workflows

Continuous integration/delivery/deployment; build pipelines; tests; linting; artifacts;
secrets; environments; approvals; rollbacks; branch strategies; pull requests; code review;
release workflows. Use GitHub Actions (or the roadmap's tool); read the official workflow/syntax
docs.

## Phase 9 — Kubernetes and orchestration

Start only after Linux, networking, containers, YAML, and cloud fundamentals are solid.
Cluster architecture; control plane/worker nodes; Pods; Deployments; ReplicaSets; Services;
ConfigMaps; Secrets; Namespaces; storage; Ingress; health checks; resource requests/limits;
scaling; updates/rollbacks; logs; events; troubleshooting; security fundamentals. Use official
Kubernetes docs extensively — don't reduce it to memorizing YAML.

## Phase 10 — Observability, reliability, and security

Metrics, logs, traces; dashboards; alerts; availability/latency/errors/saturation; SLIs/SLOs;
incident response; root-cause analysis; postmortems; capacity awareness; least privilege;
secrets management; vulnerability awareness; patch management; network/cloud security basics.
Use practical failure scenarios and troubleshooting exercises.

Certification checkpoint: AWS SysOps Administrator Associate exam once this phase's material
has been practiced hands-on (see "Certifications" above).

## Phase 11 — Portfolio projects

Build projects integrating multiple skills: Linux server administration lab; automated
system-health report; secure web-server deployment; Python cloud automation tool; containerized
application; cloud-hosted application; Terraform-deployed infrastructure; CI/CD pipeline;
monitored application; backup/recovery workflow; multi-tier cloud architecture; a final
capstone integrating Git, Linux, Python, networking, cloud, Docker, Terraform, CI/CD, security,
and observability.

Each project needs: problem statement, requirements, architecture explanation, implementation,
official documentation references, security considerations, cost considerations, testing,
troubleshooting notes, a clear README, diagrams where useful, cleanup instructions, and lessons
learned. Never keep a portfolio project he can't explain.

Self-directed initiative projects (YouTube channel, TradeForge, etc.) live in
`projects/personal/` and run alongside this phase rather than replacing it — see
`projects/personal/README.md`.

## Phase 12 — Career preparation

Introduce professional habits throughout, not only at the end — but don't replace technical
development with job-hunting too early. Once the foundation is solid: resume updates, LinkedIn
positioning, GitHub profile improvement, portfolio review, technical/behavioral/troubleshooting
interview prep, architecture discussions, job-description analysis, application strategy,
entry-level targeting (Cloud Support Associate, Technical Support Engineer, Linux Support
Technician, Junior Systems Administrator, NOC Technician, Infrastructure Support Specialist,
Cloud Operations Associate, Junior DevOps/Cloud Engineer, automation-focused support roles).

## Professional habits reinforced throughout

Clear written communication; technical English; accurate terminology; careful reading;
documentation use; note-taking; command-line confidence; Git discipline; troubleshooting;
security awareness; cost awareness; asking precise questions; explaining assumptions; testing
before concluding; verifying outputs; recognizing uncertainty; avoiding random changes; writing
useful documentation; finishing and maintaining projects.
