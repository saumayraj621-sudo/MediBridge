# System Architecture

MediBridge follows a modular architecture designed to connect different healthcare stakeholders through a centralized digital platform.

The system separates the user interface, role-based workflows, data services, mapping services, and AI assistance to keep the platform organized and scalable.

---

## 1. High-Level Architecture

```text
                         MEDIBRIDGE PLATFORM
                                |
                                v
                     +----------------------+
                     |    React Frontend    |
                     +----------+-----------+
                                |
                    +-----------+-----------+
                    |           |           |
                    v           v           v
              Clinic Portal  Doctor Portal  Admin Portal
                    |           |           |
                    +-----------+-----------+
                                |
                                v
                     +----------------------+
                     |   Firebase Services  |
                     +----------+-----------+
                                |
                         +------+------+
                         |             |
                         v             v
                  Patient Data    Referral Data


              Supporting Services
              -------------------

        +------------+   +-------------+   +-------------+
        |  Leaflet   |   | Google Maps |   |   Gemini AI |
        |    Maps    |   | Navigation  |   |  Assistant  |
        +------------+   +-------------+   +-------------+
