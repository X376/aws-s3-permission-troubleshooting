# AWS S3 Permission Troubleshooting Lab

## Overview
This lab demonstrates how to troubleshoot an AWS S3 AccessDenied issue using a layered troubleshooting model.

The scenario:
An EC2 instance attempts to access an S3 bucket, but the request fails due to an AWS permissions misconfiguration.

## Goals
- Verify caller identity using STS
- Review IAM role permissions
- Review S3 bucket policy
- Understand how different policy layers interact
- Restore access using least-privilege principles

## Architecture
EC2 Instance -> IAM Role -> S3 Bucket

## Troubleshooting Layers
1. Identity
2. IAM Policy
3. Bucket Policy
4. Object-Level Controls
5. Encryption
6. Environmental / Network Conditions

## Steps Performed
- Created EC2 instance
- Verified role attachment
- Checked caller identity with AWS STS
- Tested S3 access
- Reviewed bucket policy
- Corrected permissions
- Retested access

## Lessons Learned
- AccessDenied errors must be investigated in layers
- IAM allow does not override all other denial boundaries
- AWS STS is a critical first troubleshooting step
