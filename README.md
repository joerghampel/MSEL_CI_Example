# MSEL_CI_Example

This is a simple example project that will be used to demonstrate how different CI toolchains can operate on a LabVIEW project.

Proposed workflow:
- Show CI operating on project as-is
- In subVI.vi, delete the wire between the initialize array and Array of Hello Worlds indicator.  This will cause unit tests to fail but no VI will be broken.
- Then, delete the wire on the top-level VI connecting the Hello Count control to the Hello Count input terminal of the subVI.  Since this is a required input, the VI will be broken and the build will throw an error.
- Fix the issues and get back to a clean build.
