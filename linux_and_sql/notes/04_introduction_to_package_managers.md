# Introduction to package managers

## Packages

A **package** is a piece of software that can be combined with other packages to form an application. Some packages may be large enough to form applications on their own.

Packages contain the files needed to **install** an application. Those files include **dependencies**—supplemental files used to run an application.

**Package managers** can help resolve dependency issues and perform other management tasks. A **package manager** is a tool that helps users **install**, **manage**, and **remove** packages or applications. **Linux** uses multiple package managers.

**Note:** Use the **most recent** version of a package when possible. Newer versions include the latest **bug fixes** and **security patches**, which help keep the system more secure.

---

## Types of package managers

Many common Linux distributions share the same **parent** distribution. For example, **KALI LINUX** ™, **Ubuntu**, and **Parrot** come from **Debian**. **CentOS** comes from **Red Hat**.

That matters when **installing applications**: certain package managers match certain distribution families. For example:

- **Red Hat Package Manager (RPM)** — used with Linux distributions **derived from Red Hat**.  
- **dpkg** — used with Linux distributions **derived from Debian**.

Different package managers often use different **file extensions**:

- **RPM** — `.rpm` files, e.g. `Package-Version-Release_Architecture.rpm`.  
- **Debian-style** managers (e.g. **dpkg**) — `.deb` files, e.g. `Package_Version-Release_Architecture.deb`.

---

## Package management tools

Besides low-level package managers like **RPM** and **dpkg**, there are **package management tools** that make it easier to work with packages from the **shell**. They are often preferred for routine tasks such as **installing** a new package.

Two notable tools:

### Advanced Package Tool (APT)

**APT** is used with **Debian-derived** distributions. It is run from the **command-line interface** to **manage**, **search**, and **install** packages.

### Yellowdog Updater Modified (YUM)

**YUM** is used with **Red Hat-derived** distributions. It is run from the **command-line interface** to **manage**, **search**, and **install** packages. **YUM** works with **`.rpm`** files.

---

## Key takeaways

- A **package** is software that can be combined with other packages to form an application.  
- **Packages** are managed with **package managers**; Linux has several, depending on the distribution.  
- **Package management tools** help users work with packages easily through the **shell**.  
- **Debian-derived** distributions use managers like **dpkg** and tools like **APT**.  
- **Red Hat-derived** distributions use **RPM** and tools like **YUM**.
