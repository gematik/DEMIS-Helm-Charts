<div style="text-align:right"><img src="https://raw.githubusercontent.com/gematik/gematik.github.io/master/Gematik_Logo_Flag_With_Background.png" width="250" height="47" alt="gematik GmbH Logo"/> <br/> </div> <br/>   

# DEMIS Helm Charts Repository

## Overview

The repository provides Helm charts for the various microservices and components of the DEMIS platform. 
It serves as central source of deploying a local DEMIS Development Environment.


### Prerequisites
- Helm 3+
- DEMIS Cluster
- Docker

**Install Helm**

Helm is a tool for managing Kubernetes charts. Charts are packages of pre-configured kubernetes resources.

To install Helm, refer to the [Helm Install Guide](https://github.com/helm/helm#install) and ensure that the `helm` binary is in the `PATH` of your shell.

**Using Helm**

Once you have installed the Helm client, you can add this repository to your local machine using the following command.
1. Add Repo `helm repo add github-demis https://gematik.github.io/DEMIS-Helm-Charts/`
2. List all Chart `helm search repo github-demis`

_Note_ You don´t have to install you charts local, this will be done automatically by the terraform project.


### DEMIS Development Environment

The DEMIS-Dev-Environment can be found on [here](https://github.com/gematik/DEMIS-Development-Cluster).

### DEMIS Services

The following table provides an overview of all available DEMIS components, whose Helm Charts are contained in this repository. 
Not every service has its own Source Code Repository or Docker Image. 
Specific **Releases Notes** can be found either in the Source Code Repository or in the DEMIS-Dev-Environment.

| Service                                | Docker Image                                                                                                                                                                                                                                                                                                  | Source Code Repository                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| ARS-Service                            | [gematik1/demis-ars-service](https://hub.docker.com/r/gematik1/demis-ars-service)                                                                                                                                                                                                                             | https://github.com/gematik/DEMIS-antibiotic-resistance-surveillance-service  |
| Certificate-Update-Service             | [gematik1/demis-certificate-update-service](https://hub.docker.com/r/gematik1/demis-certificate-update-service)                                                                                                                                                                                               | https://github.com/gematik/DEMIS-certificate-update-service                  |
| Context-Enrichment-Service             | [gematik1/demis-context-enrichment-service](https://hub.docker.com/r/gematik1/demis-context-enrichment-service)                                                                                                                                                                                               | https://github.com/gematik/DEMIS-context-enrichment-service                  |
| FHIR-Profile-Snapshots                 | [gematik1/demis-fhir-profile-snapshots](https://hub.docker.com/r/gematik1/demis-fhir-profile-snapshots)                                                                                                                                                                                                       | n.a.                                                                         |
| FHIR-Storage-Service                   | [gematik1/demis-fhir-storage-reader](https://hub.docker.com/r/gematik1/demis-fhir-storage-reader)<br/>[gematik1/demis-fhir-storage-writer](https://hub.docker.com/r/gematik1/demis-fhir-storage-writer)<br/>[gematik1/demis-fhir-storage-purger](https://hub.docker.com/r/gematik1/demis-fhir-storage-purger) | https://github.com/gematik/DEMIS-fhir-storage-service                        |
| Fhir-UI-Data-Model-Translation-Service | [gematik1/demis-futs](https://hub.docker.com/r/gematik1/demis-futs)                                                                                                                                                                                                                                           | https://github.com/gematik/DEMIS-fhir-ui-data-model-translation-service      |
| Gateway-IGS                            | [gematik1/demis-gateway-igs](https://hub.docker.com/r/gematik1/demis-gateway-igs)                                                                                                                                                                                                                             | https://github.com/gematik/DEMIS-gateway-igs                                 |
| Gematik-IDP                            | [gematik1/idp-server](https://hub.docker.com/r/gematik1/idp-server)                                                                                                                                                                                                                                           | n.a.                                                                         |
| Hospital-Location-Service              | [gematik1/demis-hospital-location-service](https://hub.docker.com/r/gematik1/demis-hospital-location-service)                                                                                                                                                                                                 | https://github.com/gematik/DEMIS-hospital-location-service                   |
| IGS-Profile-Snaphots                   | [gematik1/demis-igs-profile-snapshots](https://hub.docker.com/r/gematik1/demis-igs-profile-snapshots)                                                                                                                                                                                                         | n.a.                                                                         |
| IGS-Service                            | [gematik1/demis-igs-service](https://hub.docker.com/r/gematik1/demis-igs-service)                                                                                                                                                                                                                             | https://github.com/gematik/DEMIS-integrierte-genomische-surveillance-service |
| Keycloak-User-Purger                   | [gematik1/demis-keycloak-user-purger](https://hub.docker.com/r/gematik1/demis-keycloak-user-purger)                                                                                                                                                                                                           | https://github.com/gematik/DEMIS-keycloak-user-purger                        |
| Keycloak                               | [gematik1/demis-keycloak](https://hub.docker.com/r/gematik1/demis-keycloak)                                                                                                                                                                                                                                   | n.a.                                                                         |
| Lifecycle-Validation-Service           | [gematik1/demis-lifecycle-validation-service](https://hub.docker.com/r/gematik1/demis-lifecycle-validation-service)                                                                                                                                                                                           | https://github.com/gematik/DEMIS-lifecycle-validation-service                |
| Minio                                  | [gematik1/demis-minio](https://hub.docker.com/r/gematik1/demis-minio)                                                                                                                                                                                                                                         | n.a.                                                                         |
| Istio-Network-Rules                    | n.a.                                                                                                                                                                                                                                                                                                          | n.a.                                                                         |
| Istio-Routing                          | n.a.                                                                                                                                                                                                                                                                                                          | n.a.                                                                         |
| Istio-Policies                         | n.a.                                                                                                                                                                                                                                                                                                          | n.a.                                                                         |
| Notification-Gateway                   | [gematik1/demis-notification-gateway](https://hub.docker.com/r/gematik1/demis-notification-gateway)                                                                                                                                                                                                           | https://github.com/gematik/DEMIS-notification-gateway                        |
| Notification-Processing-Service        | [gematik1/demis-notification-processing-service](https://hub.docker.com/r/gematik1/demis-notification-processing-service)                                                                                                                                                                                     | https://github.com/gematik/DEMIS-notification-processing-service             |
| Notification-Routing-Data-Public       | [gematik1/demis-notification-routing-data-public](https://hub.docker.com/r/gematik1/demis-notification-routing-data-public)                                                                                                                                                                                   | n.a.                                                                         |
| Notification-Routing-Service           | [gematik1/demis-notification-routing-service](https://hub.docker.com/r/gematik1/demis-notification-routing-service)                                                                                                                                                                                           | https://github.com/gematik/DEMIS-notification-routing-service                |
| PDFGen-Service                         | [gematik1/demis-pdfgen-service](https://hub.docker.com/r/gematik1/demis-pdfgen-service)                                                                                                                                                                                                                       | https://github.com/gematik/DEMIS-pdfgen-service                              |
| PgBouncer                              | [gematik1/demis-pgbouncer](https://hub.docker.com/r/gematik1/demis-pgbouncer)                                                                                                                                                                                                                                 | n.a.                                                                         |
| Postgres                               | [gematik1/demis-postgres](https://hub.docker.com/r/gematik1/demis-postgres)                                                                                                                                                                                                                                   | n.a.                                                                         |
| Portal-Bedoccupancy                    | [gematik1/demis-portal-bedoccupancy](https://hub.docker.com/r/gematik1/demis-portal-bedoccupancy)                                                                                                                                                                                                             | https://github.com/gematik/DEMIS-portal-bedoccupancy                         |
| Portal-Disease                         | [gematik1/demis-portal-disease](https://hub.docker.com/r/gematik1/demis-portal-disease)                                                                                                                                                                                                                       | https://github.com/gematik/DEMIS-portal-disease                              |
| Portal-IGS                             | [gematik1/demis-portal-igs](https://hub.docker.com/r/gematik1/demis-portal-igs)                                                                                                                                                                                                                               | https://github.com/gematik/DEMIS-portal-igs                                  |
| Portal-Shell                           | [gematik1/demis-portal-shell](https://hub.docker.com/r/gematik1/demis-shell)                                                                                                                                                                                                                                  | https://github.com/gematik/DEMIS-portal-shell                                |
| Portal-Pathogen                        | [gematik1/demis-portal-pathogen](https://hub.docker.com/r/gematik1/demis-pathogen)                                                                                                                                                                                                                            | https://github.com/gematik/DEMIS-portal-pathogen                             |
| Pseudonymization-Service               | [gematik1/demis-pseudonymization-service](https://hub.docker.com/r/gematik1/demis-pseudonymization-service)                                                                                                                                                                                                   | https://github.com/gematik/DEMIS-pseudonymization-service                    |
| Pseudonymization-Storage-Service       | [gematik1/demis-pseudonymization-storage-service](https://hub.docker.com/r/gematik1/demis-pseudonymization-storage-service)                                                                                                                                                                                   | https://github.com/gematik/DEMIS-pseudonymization-storage-service            |
| Redis                                  | [gematik1/demis-redis](https://hub.docker.com/r/gematik1/demis-redis)                                                                                                                                                                                                                                         | n.n.                                                                         |
| Report-Processing-Service              | [gematik1/demis-report-processing-service](https://hub.docker.com/r/gematik1/demis-report-processing-service)                                                                                                                                                                                                 | https://github.com/gematik/DEMIS-report-processing-service                   |
| Stage-Configuration-Data-Public        | [gematik1/demis-stage-configuration-data-public](https://hub.docker.com/r/gematik1/demis-stage-configuration-data-public)                                                                                                                                                                                     | n.a.                                                                         |
| Validation-Service                     | [gematik1/demis-validation-serivce](https://hub.docker.com/r/gematik1/demis-validation-serivce)                                                                                                                                                                                                               | https://github.com/gematik/DEMIS-validation-service                          |

## Security Policy
If you want to see the security policy, please check our [SECURITY](.github/SECURITY.md).

## Contributing
If you want to contribute, please check our [CONTRIBUTING](.github/CONTRIBUTING.md).

## License

Copyright 2025-2025 gematik GmbH

EUROPEAN UNION PUBLIC LICENCE v. 1.2

EUPL © the European Union 2007, 2016

See the [LICENSE](./LICENSE) for the specific language governing permissions and limitations under the License

## Additional Notes and Disclaimer from gematik GmbH

1. Copyright notice: Each published work result is accompanied by an explicit statement of the license conditions for use. These are regularly typical conditions in connection with open source or free software. Programs described/provided/linked here are free software, unless otherwise stated.
2. Permission notice: Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
   1. The copyright notice (Item 1) and the permission notice (Item 2) shall be included in all copies or substantial portions of the Software.
   2. The software is provided "as is" without warranty of any kind, either express or implied, including, but not limited to, the warranties of fitness for a particular purpose, merchantability, and/or non-infringement. The authors or copyright holders shall not be liable in any manner whatsoever for any damages or other claims arising from, out of or in connection with the software or the use or other dealings with the software, whether in an action of contract, tort, or otherwise.
   3. We take open source license compliance very seriously. We are always striving to achieve compliance at all times and to improve our processes. If you find any issues or have any suggestions or comments, or if you see any other ways in which we can improve, please reach out to: ospo@gematik.de
3. Please note: Parts of this code may have been generated using AI-supported technology. Please take this into account, especially when troubleshooting, for security analyses and possible adjustments.


## Contact
E-Mail to [DEMIS Entwicklung](mailto:demis-entwicklung@gematik.de?subject=[GitHub]%20Helm-Charts)
