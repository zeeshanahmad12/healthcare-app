Structure:
- 00-namespace: Logical isolation
- 01-rbac: Identity and permissions
- 02-config-secret: App settings and passwords
- 03-storage: Static PV for EC2
- 04-networking: Internal and External services
- 05-statefulset: The main stateful application


-------------------Project Structer----------------------------
manifests/
├── kustomization.yaml                 # The Master/Index file
├── healthcare-prod-namespace.yaml     # Creates the 'healthcare-prod' namespace
├── secrets/
│   └── prod-db-secret.yaml            # Stores database credentials
└── rbac/
    ├── service-account.yaml           # The identity for the app
    ├── role.yaml                      # The permission rules (read-only)
    └── role-binding.yaml              # Connects the identity to the rules
