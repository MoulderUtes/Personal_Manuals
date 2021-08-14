# External Drives
*Cause they can get confusing as crap*


**Table of Contents**
- [External Drives](#external-drives)
  - [Theory](#theory)
  - [Overview](#overview)
## Theory
External drives are a easy way to transport and organize data. Although more unreliable they also should not serve as the only location data is stored. 
## Overview
* Naming - All drives should be named using shortened manufacture followed by size in GB `KING16` for a kingston 16GB drive
* They should follow the [file structure conventions](../../../../Data_Management/file_structure_conventions.md) as well as [naming conventions](../../../../Data_Management/naming_conventions.md)
* External drives should be formatted in exFAT for compatibility and modernization
* External drivers should have a GPT partition table for modernization and uniformity 
* Drives should have partitions separated according to use case
* If drives are going to have encrypted data on them it needs to be stored in a file on root named Encrypted via gpg encryption
