# Luo Protected Environment Setup

This repository contains the configuration files used to set up the
HIPAA-compliant protected environment for Dr. Luo.

The cfn template (`cfncluster-with-p2.cfn.json`) differs from the original
created by X-ISS in that it includes the p2.\* instance types as available
values for the master and compute instance type parameters. Note that this
template is available in S3 at
[https://pe-cfn.s3.amazonaws.com/Common/cfncluster-with-p2.cfn.json](https://pe-cfn.s3.amazonaws.com/Common/cfncluster-with-p2.cfn.json).

The config file used to create the cluster was `config.pe1-luo.gpu`, using the
following command:
	
	cfncluster -c config.pe1-luo.gpu create LuoCluster1

Which must be run from the `CFN Manager` node in the art-rch-hpc AWS account.
