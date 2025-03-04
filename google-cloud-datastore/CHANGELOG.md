# Release History

### 1.5.3 / 2019-06-12

* Enable grpc.service_config_disable_resolution
* Use VERSION constant in GAPIC client

### 1.5.2 / 2019-04-29

* Add AUTHENTICATION.md guide.
* Update generated documentation.
* Extract gRPC header values from request.

### 1.5.1 / 2019-02-13

* Add `ReadOnlyTransaction` convenience methods:
  * Add `ReadOnlyTransaction#query`
  * Add `ReadOnlyTransaction#gql`
  * Add `ReadOnlyTransaction#key`

### 1.5.0 / 2019-02-01

* Make use of Credentials#project_id
  * Use Credentials#project_id
    If a project_id is not provided, use the value on the Credentials object.
    This value was added in googleauth 0.7.0.
  * Loosen googleauth dependency
    Allow for new releases up to 0.10.
    The googleauth devs have committed to maintaining the current API
    and will not make backwards compatible changes before 0.10.

### 1.4.4 / 2018-09-20

* Update documentation.
  * Change documentation URL to googleapis GitHub org.
* Fix circular require warning.

### 1.4.3 / 2018-09-12

* Update documentation.
* Add missing documentation files to package.

### 1.4.2 / 2018-09-10

* Fix issue where client_config was not being passed when connecting to the
  datastore emulator.
* Update documentation.

### 1.4.1 / 2018-08-21

* Update documentation.

### 1.4.0 / 2018-02-27

* Support Shared Configuration.

### 1.3.0 / 2017-12-19

* Support Read-Only Transactions
  * Add ReadOnlyTransaction class.
  * Add Dataset#read_only_transaction.
* Dataset#transaction now automatically retries on error,
* Add Dataset#transaction previous_transaction and deadline arguments,
* Update google-gax dependency to 1.0.

### 1.2.1 / 2017-11-21

* Remove warning when connecting to Datastore Emulator.

### 1.2.0 / 2017-11-14

* Add `Google::Cloud::Datastore::Credentials` class.
* Rename constructor arguments to `project_id` and `credentials`.
  (The previous arguments `project` and `keyfile` are still supported.)
* Document `Google::Auth::Credentials` as `credentials` value.
* Updated `google-gax` (`grpc`, `google-protobuf`), `googleauth` dependencies.

### 1.1.0 / 2017-07-11

* Update GAPIC configuration to exclude `UNAVAILABLE` errors from automatic retry.
* Update gem spec homepage links.

### 1.0.1 / 2017-05-06

* Update google-protobuf to the previous known working version

### 1.0.0 / 2017-03-31

* Release 1.0
* Updated documentation
* Automatic retry on `UNAVAILABLE` errors

### 0.24.2 / 2017-03-03

* No public API changes.
* Update GRPC header value sent to the Datastore API.

### 0.24.1 / 2017-03-01

* No public API changes.
* Update GRPC header value sent to the Datastore API.

### 0.24.0 / 2017-02-21

* Add emulator_host parameter
* Fix GRPC retry bug
* The client_config data structure has replaced retry_codes/retry_codes_def with retry_codes
* Update GRPC/Protobuf/GAX dependencies

### 0.23.0 / 2016-12-8

* Many documentation improvements
* Add documentation for Low Level API

### 0.21.0 / 2016-10-20

* New service constructor Google::Cloud::Datastore.new
* New constructor argument client_config
* Entity properties can now be accessed with symbols as well as strings

### 0.20.1 / 2016-09-02

* Fix an issue with the GRPC client and forked sub-processes

### 0.20.0 / 2016-08-26

This gem contains the Google Cloud Datastore service implementation for the `google-cloud` gem. The `google-cloud` gem replaces the old `gcloud` gem. Legacy code can continue to use the `gcloud` gem.

* Namespace is now `Google::Cloud`
* The `google-cloud` gem is now an umbrella package for individual gems

#### Changes

* Upgraded to V1
* Fix issue with embedded entities (@Dragor2)
