---
name: "Adding end-to-end encryption to more clients"
desc: "All Matrix clients should support end-to-end encryption"
difficulty: "Hard"
issues:
mentors:
 - ara4n
 - uhoreg
initiatives:
 - GSoC
tags:
 - Encryption
 - Client
---

A lot of effort in Matrix is being put into End-to-End Encryption using the Olm & Megolm cryptographic ratchets (as assessed by NCC Group - see https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last/ for details.

However, the current implementation has only landed in matrix-js-sdk, matrix-ios-sdk and matrix-android-sdk. As a result, any client or bridge or bot which isn't built on one of those codebases is currently out of luck.

In this project, you would port the application-layer E2E implementation to one or more other clients - e.g. to Golang for use with go-neb, or to C++ for libqmatrixclient (as used by the Quaternion, Spectral & Tensor desktop clients) or to C for matrix-purple (as used by Pidgin). Alternatively, you might consider implementing an E2E-aware matrix proxy which any client can connect to (when running locally) to share encrypted communication with the rest of Matrix.

This would be a great way to improve your cryptography skills and learn about one of the most exciting and ambitious E2E cryptography projects out there.

#### Expected Results

Extend other Matrix clients to speak E2E, or implement an E2E-aware Matrix Proxy

#### Knowledge pre-req

Cryptography. The language for the platform you are targetting.
