===============
S3 To S3 Backup
===============

.. image:: https://travis-ci.org/YD-Technology/s3tos3backup.png?branch=master
   :target: http://travis-ci.org/YD-Technology/s3tos3backup

.. image:: https://coveralls.io/repos/YD-Technology/s3tos3backup/badge.png?branch=master
   :target: https://coveralls.io/r/YD-Technology/s3tos3backup/
   
.. image:: https://d2weczhvl823v0.cloudfront.net/YD-Technology/s3tos3backup/trend.png
   :alt: Bitdeli badge
   :target: https://bitdeli.com/free

s3tos3backup is a tool for managing backups for Amazon S3 storage with IAM role support.


Usage
=====

Simple
::

    s3tos3backup

With all options at runtime

::

    s3tos3backup --access_key=FOO --secret_key=BAR -b BAZ -o 14


Supported options
=================

::

  -c FILE, --config FILE Config file name. Defaults to ~/.s3tos3backup
  --access_key AWS_ACCESS_KEY AWS Access Key
  --secret_key AWS_SECRET_KEY AWS Secret Key
  -b BUCKET_NAME, --bucket BUCKET_NAME Bucket name
  -o REMOVE_OLDER_DAYS, --remove-older-days REMOVE_OLDER_DAYS Remove backups older than days
  -v, --verbose         Enable verbose output
  -d, --debug           Enable debug output
  --remove-only         Remove only old backups. Do not do a backup
  --backup-only         Do a backup. Do not remove only old backups
  --configure           Save configuration and exit


Configuration
=============

::

    [main]
    access_key = FOO
    secret_key = BAR
    bucket_name = BAZ
    remove_older_days = 14


Development
===========

Running tests

::

    python setup.py test

Running PEP8 checker
::

    pep8 --config=pep8.rc src/s3tos3backup
