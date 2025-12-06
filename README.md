PAiCore Technologies SMSC – Free Basic Edition
Overview

The PAiCore SMSC is a high-performance, multi-protocol Short Message Service Center designed for MNOs, MVNOs, aggregators, and enterprise platforms that require robust routing, high throughput, and reliability.

Supported end-to-end messaging flows:

HTTP ↔ SMPP

HTTP ↔ SS7/SIGTRAN

SMPP ↔ SS7/SIGTRAN

HTTP-based custom integrations

Its modular architecture enables horizontal scaling of each component independently.

Key Features – Free Basic Open Source Edition

Fully open-source core for customization and community-driven enhancements.

Up to 12,000 TPS per instance (hardware and tuning dependent).

Native support for SS7 / SIGTRAN / SMPP / HTTP.

Advanced routing logic, DLR mapping, and broadcast messaging.

Modular deployment (HTTP/SP, SMPP/SP, Routing, Retries, Management, Data Init).

Compatible with Kafka, ScyllaDB, Redis Cluster, PostgreSQL/Citus.

Documentation

Full architecture, module specifications, routing flows, APIs, and deployment guides are available at:

👉 https://documentation.paic-bd.com/books/official-smsc-documentation

Installation (Recommended) – Using the Installer

The official and recommended method to deploy the Free Basic Edition is the SMSC Installer, provided as a .tar.gz file in GitHub Releases.

The installer package includes:

Docker Compose templates

Environment configuration files

Module definitions

Setup and validation scripts

Directory structure

License directory

A built-in README with the complete installation steps

1. Download Installer

👉 https://github.com/paicbd/smsc/releases/latest

You will find a file similar to:

SMSC_Installer_FreeBasic_build-XX.tar.gz

2. Extract Package
tar -xzvf SMSC_Installer_FreeBasic_build-XX.tar.gz
cd SMSC_installer/


Inside the extracted folder you will find:

README.md   ← includes the full step-by-step installation guide
installer.sh
env/
smsc/
docker-compose.yml
scripts/

3. Add License File
sudo cp /path/to/new_license.txt ./smsc/data/license/license_paic.txt

4. Run Installer
sudo ./installer.sh


The installer automatically performs:

OS validation (Ubuntu 22.04/24.04)

Docker installation and prerequisites

Deployment of Kafka, ScyllaDB, Redis Cluster, PostgreSQL/Citus

Deployment of all SMSC Free Basic modules

Docker Images – Free Basic Edition
SMSC Modules
paicbusinessdev/free-basic-db-insert-data:3.0.0-2
paicbusinessdev/free-basic-http-client-module:3.0.0-2
paicbusinessdev/free-basic-http-server-module:3.0.0-2
paicbusinessdev/free-basic-retries-module:3.0.0-2
paicbusinessdev/free-basic-smpp-client-module:3.0.0-3
paicbusinessdev/free-basic-smpp-server-module:3.0.0-3
paicbusinessdev/free-basic-smsc-management-be:3.0.0-2
paicbusinessdev/free-basic-smsc-management-fe:3.0.0-2
paicbusinessdev/free-basic-smsc-routing-module:3.0.0-3

Supporting Infrastructure
paicbusinessdev/kafka:4.0.0
paicbusinessdev/scylla:5.2.0
provectuslabs/kafka-ui:latest
citusdata/citus:12.0.0
citusdata/membership-manager:0.3.0

Manual Deployment

Manual deployments are not included in this public README.
If you require a fully manual Docker or bare-metal deployment:

Please contact us to grant you access to the detailed internal documentation and provide you with step-by-step guidance.

👉 https://paicore.tech/smsc/

Source Code

Clone all open-source SMSC repositories:

chmod +x fork-and-clone-smsc-repos.sh
./fork-and-clone-smsc-repos.sh "<destination_directory>"

Support

For enterprise support, integration assistance, or commercial licensing visit us:

👉 https://paicore.tech/smsc/
