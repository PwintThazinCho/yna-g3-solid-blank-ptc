# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [25-01-22]

### Fixes

- Update gradle version to fix the problem that snapshot version of gradle plugins might be used. (#135)


## [24-11-21]

### Fixes

- Fix the problem of unable to remote debugging.(#129)


## [24-11-14]

### Fixes

- Resolve the issue that encountering login page when it's with 'dummy-user' profile.

## [24-11-12]

### Fixes

- Fix the issue of `PJUserDetailsServiceLoader#loadUserByUsername` been called twice when login failed, by removing `http.authenticationProvider(authenticationProvider());` in `PJLoginSecurityConfiguration`.  


## [24-11-06]

### Changes

- Fix the session of logined user can't be expired in correct timeout when using not redis profile in `PJRedisConfiguration`. 


## [24-11-04]

### Changes
- update `Dockerfile` to use a new version of java base image(17.0.13_11).


## [24-10-25]

### Changes
- update `trivy-scan.yml`, solving the problem that trivy db might be downloaded failed due to traffic limit.


## [24-10-16]

### Changes
- update `codeql.yml` to use the latest version of github actions. 


## [24-10-10]

### Fixed
- update `logback-file.xml` to fix the problem that "ClassNotFound" exception happened due to `SizeAndTimeBasedFNATP` removed in logback new version.  


## [24-10-07]

### Fixed
- change `SecurityConfiguration` and `DummyAuthenticationInterceptor` to fix the problem that websocket can't be connected when using `dummy-auth`.  


## [24-09-24]

### Changes
- update solid framework_version to [1.1, 1.2) in `gradle.properties`.


## [24-09-13]

### Changes
- update `PJUserDetailsServiceLoader` to show how to set roles into `userDetails`.  
- update `SecurityConfiguration` that not ignoring `/error` from spring security, and add it as `permit` in `PJLoginSecurityConfiguration`.  