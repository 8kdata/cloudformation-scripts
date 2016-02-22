# cloudformation-scripts

A collection of [AWS
CloudFormation](https://aws.amazon.com/cloudformation/) scripts to
deploy different stacks.

*Important note*: while this scripts are provided as free software, and
you may obtain them from the master repository free of charge, running
the scripts in your AWS environment will result in charges to you by
Amazon AWS.


## Available CFs

### greenplum/gpdb-segments_within_single_host.cf.json

Creates a [Greenplum](https://github.com/greenplum-db/gpdb) cluster,
where all the segments are created within the same host. Only one host
is created. It downloads Greenplum's source code, compiles, installs it
and inits the cluster. It can also optionally run regression tests.

It supports parameter options to specify the Git repository from where
to download the source code, the intended branch to compile, the
instance type (restricted to instances with 2 SSDs as instance storage),
the ``./configure`` build arguments or whether to run no regression
tests or ``make installcheck-good``.
