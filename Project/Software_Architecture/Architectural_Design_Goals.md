# Architectural Design Goals



| Goal ID | Design Goal | Description | Related Requirement | Priority | Justification |
|---------|-------------|-------------|---------------------|----------|---------------|
| AG-01 | Maintainability and Modularity | The system is split into components with one clear responsibility each and narrow interfaces, so a change stays inside one or two components. | NFR-01, NFR-02 | High | Four team members work in parallel and earlier labs were revised several times. Low coupling lets each member own a component. |
| AG-02 | Security | Passwords, login attempts and admin access are controlled in one place, and the browser can never reach the stored data directly. | NFR-07, NFR-11, NFR-15, NFR-16 | High | The system stores personal data and passwords and has an admin role that can suspend accounts and remove listings. |
