# Clean Room Development Guide

This document outlines the clean room development process for building a Win32-compatible operating system in the custom Hexa programming language, using ReactOS as a reference. The goal is to ensure legal safety and avoid intellectual property infringement, particularly with respect to Microsoft's proprietary Windows code.

Win32 compatibility is implemented as a plugin—operating system is operable without its presence. This further strengthens legal safety by openly demonstrating that Greentea OS is not a competitive threat to Microsoft's currently active commercial products (e.g. Windows 11), as required by the law.

## Purpose

Clean room development ensures our OS is functionally compatible with the Win32 API without copying proprietary code.

In this example, ReactOS, an open-source OS under the GNU GPL, serves as a third-party reference for understanding Win32 behavior and OS architecture.

Due to Greentea OS being new, independent project in different programming language, ReactOS works as a "clean room source of the third-party knowledge" in *relation* to it. The same applies to other projects.

## Clean Room Principles

Clean room states that replication of Win32 functionality should happen without copying proprietary code, using only public specifications and third-party references like ReactOS. **This requirement is relaxed to a degree according to directives related to reverse engineering**, but still is a strong general approach to maximize legal safeguards. *You may learn more about the directives from the README in the root of this repo.*

1. **Reference, Don’t Copy**:

   - Use ReactOS’s source code (available on GitHub) to study Win32 API behavior, kernel structures (e.g., `ntoskrnl`), and driver interfaces (e.g., `ntoskrnl/io`).

2. **Leverage Public Documentation**:

   - Rely on Microsoft’s public resources (e.g., MSDN, Windows SDK) for Win32 API specifications to minimize dependence on ReactOS.
   - Use public documentation to define expected behavior for APIs and kernel components.

3. **Custom Language Advantage**:

   - Implement all code in the Hexa programming language, which inherently distances our implementation from ReactOS’s and Microsoft's C/C++ codebases.
   - Hexa’s unique syntax forces reengineering of low-level components, strengthening our clean room claim.

4. **Document the Process**:

   - Maintain records of development, showing that ReactOS was used only as a functional reference (e.g., for API behavior or system design).
   - Log how each component was designed and implemented independently in Hexa.
   - This is not a strict requirement, and generally satisfied with the presence of the Git commit history.
   - A separate log or design document alongside Git history would be more robust for legal defense.

5. **Avoid LGPL Conflicts**:

   - Do not incorporate third-party licensed code into the project unless the code part in question is LGPL-compatible, as this is the primary Greentea OS license.
   - We do not accept proprietary code.

## Implementation Guidelines

Win32 compatibility is a modular plugin, ensuring Greentea OS operates independently and does not compete with Microsoft’s active products, per legal requirements.

- **Study References**: Analyze ReactOS’s `ntoskrnl` (kernel), `win32k` (graphics), and `dll/win32` (Win32 APIs) to understand Win32-compatible OS architecture.
- **Write Original Code**: Implement all functionality in Hexa, focusing on replicating observed behavior (e.g., API inputs/outputs/side effects) rather than code structure.
- **Test Independently**: Use Microsoft’s tools (e.g., Application Verifier, Driver Verifier) to validate Win32 compatibility, reducing reliance on ReactOS’s test suite.
- Testing with Microsoft’s tools ensures we’re aligning with official Win32 specs, not just ReactOS’s implementation.

## Legal Safeguards

- Consult an intellectual property lawyer to review the development process and ensure compliance with clean room principles.
- Avoid any direct use of Microsoft’s proprietary code or documentation not publicly available.
- If in doubt, prioritize public Win32 API specifications over ReactOS’s implementation details.

## Commitment

By following these guidelines, we ensure our OS is a legally independent implementation of a Win32-compatible system, leveraging ReactOS as a reference while maintaining clean room integrity.
