# Release History

### 1.1.0 / 2019-06-17

* KeyManagementServiceClient  changes:
  * Added methods
    * create_import_job
    * get_import_job
    * list_import_jobs
    * import_crypto_key_version
  * Argument changes
    * Add filter and order_by arguments to:
      * list_key_rings
      * list_crypto_keys
      * list_crypto_key_versions
    * Add skip_initial_version_creation argument to create_crypto_key
* CryptoKeyVersion changes:
  * Add CryptoKeyVersionAlgorithm constants:
    * RSA_SIGN_PSS_4096_SHA512
    * RSA_SIGN_PKCS1_4096_SHA512
    * RSA_DECRYPT_OAEP_4096_SHA512
  * Add CryptoKeyVersionState constants:
    * PENDING_IMPORT
    * IMPORT_FAILED
* Add import_job_path helper method
* Update documentation

### 1.0.2 / 2019-06-11

* Update IAM Policy documentation.
* Add VERSION constant.

### 1.0.1 / 2019-04-29

* Update RPC retry configuration.
* Add AUTHENTICATION.md guide.
* Update documentation for common types.
* Update generated code examples.

### 1.0.0 / 2019-03-11

* Bump release level to GA.
* Support Cavium V2 compression.
* Add example to readme.

### 0.3.0 / 2019-02-07

* Move library to Beta.

### 0.2.5 / 2018-12-13

* Alias the following KeyManagementServiceClient class methods to instance methods.
  * crypto_key_version_path
  * key_ring_path
  * crypto_key_path_path
  * crypto_key_path
  * location_path

### 0.2.4 / 2018-09-20

* Update documentation.
  * Change documentation URL to googleapis GitHub org.

### 0.2.3 / 2018-09-12

* Add Assymetric Sign/Decrypt.
* Add CryptoKeyVersion template and view classes.
* Add KeyOperationAttestation.

### 0.2.2 / 2018-09-10

* Update documentation.

### 0.2.1 / 2018-08-21

* Update documentation.

### 0.2.0 / 2018-07-09

* Minor rework to how requests are nested.

### 0.1.0 / 2018-07-06

* Initial release
