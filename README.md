# **MimiqArtifacts Repository**

## **Purpose**
The **MimiqArtifacts** repository is used to store and manage **binary artifacts** for the **Quantanium.jl** project (julia wrapper of Quantanium). It serves as a **public repository** for pre-built binaries generated via **BinaryBuilder.jl** and released through **GitHub Actions**.

## **What are Artifacts?**
Artifacts are **compiled binary dependencies** used by **Julia packages**. Instead of building dependencies locally, **Quantanium.jl** retrieves these pre-built binaries from **MimiqArtifacts**, ensuring:
- **Faster installation and execution**
- **Consistent and reproducible builds**
- **Seamless deployment without manual compilation**

## **How It Works**
1. **Building Artifacts**: Binary artifacts are compiled using **BinaryBuilder.jl** inside **GitHub Actions**.
2. **Releasing Artifacts**: Artifacts are packaged as tarballs and uploaded to **GitHub Releases** via **GitHub Actions**.
3. **Using Artifacts**: Julia packages can download and use these pre-built binaries instead of compiling them locally.

## **Release Process**
- Each release corresponds to a specific **tag** (e.g., `v0.1.0`).
- The release includes a **SHA256 checksum** for validation.
- The artifacts are uploaded to **GitHub Releases** under the **MimiqArtifacts** repository.

## **Important Notes**
- The main branch **does not contain source code**—only **artifact releases**.
- To create a new release, ensure that the **GitHub token** (`ARTIFACTS_RELEASE`) is correctly configured.
- If an error occurs when creating a release, check that the **tag exists** before publishing.


