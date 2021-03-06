v 9.1.1 (2017-05-02)
- Fix apt-get syntax to install a specific version. !563
- Remove the build container after execution has completed !571

v 9.1.0 (2017-04-22)
- Don't install docs for the fpm Gem !526
- Mention tagged S3 sources in installation documentation !513
- Extend documentation about accessing docker services !527
- Replace b.CurrentStage with b.CurrentState where it was misused !530
- Docker provider metrics cleanups and renaming !531
- Replace godep with govendor !505
- Add histogram metrics for docker machine creation !533
- Fix cache containers dicsovering regression !534
- Add urls to environments created with CI release jobs !537
- Remove unmanaged docker images sources !538
- Speed up CI pipeline !536
- Add job for checking the internal docs links !542
- Mention Runner -> GitLab compatibility concerns after 9.0 release !544
- Log error if API v4 is not present (GitLab CE/EE is older than 9.0) !528
- Cleanup variables set on GitLab already !523
- Add faq entry describing how to handle missing zoneinfo.zip problem !543
- Add documentation on how Runner uses Minio library !419
- Update docker.md - typo in runners documentation link !546
- Add log_level option to config.toml !524
- Support private registries with Kubernetes !551
- Cleanup Kubernetes typos and wording !550
- Fix runner crashing on builds helper collect !529
- Config docs: Fix syntax in example TOML for Kubernetes !552
- Docker: Allow to configure shared memory size !468
- Return error for cache-extractor command when S3 cache source returns 404 !429
- Add executor stage to ci_runner_builds metric's labels !548
- Don't show image's ID when it's the same as image's name !557
- Extended verify command with runner selector !532
- Changed information line logged by Runner while unregistering !540
- Properly configure connection timeouts and keep-alives !560
- Log fatal error when concurrent is less than 1 !549

v 9.0.4 (2017-05-02)
- Fix apt-get syntax to install a specific version. !563
- Remove the build container after execution has completed !571

v 9.0.3 (2017-04-21)
- Fix runner crashing on builds helper collect !529
- Properly configure connection timeouts and keep-alives !560

v 9.0.2 (2017-04-06)
- Speed up CI pipeline !536

v 9.0.1 (2017-04-05)
- Don't install docs for the fpm Gem !526
- Mention tagged S3 sources in installation documentation !513
- Replace b.CurrentStage with b.CurrentState where it was misused !530
- Replace godep with govendor !505
- Fix cache containers dicsovering regression !534
- Add urls to environments created with CI release jobs !537
- Mention Runner -> GitLab compatibility concerns after 9.0 release !544
- Log error if API v4 is not present (GitLab CE/EE is older than 9.0) !528

v 9.0.0
- Change dependency from `github.com/fsouza/go-dockerclient` to `github.com/docker/docker/client`" !301
- Update docker-machine version to fix coreos provision !500
- Cleanup windows install docs !497
- Replace io.Copy with stdcopy.StdCopy for docker output handling !503
- Fixes typo: current to concurrent. !508
- Modifies autoscale algorithm example !509
- Force-terminate VirtualBox and Parallels VMs so snapshot restore works properly !313
- Fix indentation of 'image_pull_secrets' in kubernetes configuration example !512
- Show Docker image ID in job's log !507
- Fix word consistency in autoscaling docs !519
- Rename the binary on download to use gitlab-runner as command !510
- Improve details around limits !502
- Switch from CI API v1 to API v4 !517
- Make it easier to run tests locally !506
- Kubernetes private credentials !520
- Limit number of concurrent requests to builds/register.json !518
- Remove deprecated kubernetes executor configuration fields !521
- Drop Kubernetes executor 'experimental' notice !525

v 1.11.4 (2017-04-28)
- Fixes test that was failing 1.11.3 release

v 1.11.3 (2017-04-28)
- Add urls to environments created with CI release jobs !537
- Speed up CI pipeline !536
- Fix runner crashing on builds helper collect !529

v 1.11.2
- Force-terminate VirtualBox and Parallels VMs so snapshot restore works properly !313
- Don't install docs for the fpm Gem !526
- Mention tagged S3 sources in installation documentation !513
- Limit number of concurrent requests to builds/register.json !518
- Replace b.CurrentStage with b.CurrentState where it was misused !530

v 1.11.1
- Update docker-machine version to fix coreos provision !500

v 1.11.0
- Fix S3 and packagecloud uploads step in release process !455
- Add ubuntu/yakkety to packages generation list !458
- Reduce size of gitlab-runner-helper images !456
- Fix crash on machine creation !461
- Rename 'Build (succeeded|failed)' to 'Job (succeeded|failed)' !459
- Fix race in helpers/prometheus/log_hook.go: Fire() method !463
- Fix missing VERSION on Mac build !465
- Added post_build_script to call scripts after user-defined build scripts !460
- Fix offense reported by vet. Add vet to 'code style' job. !477
- Add the runner name to the first line of log output, after the version !473
- Make CI_DEBUG_TRACE working on Windows CMD !483
- Update packages targets !485
- Update Makefile (fix permissions on /usr/share/gitlab-runner/) !487
- Add timezone support for OffPeak intervals !479
- Set GIT_SUBMODULE_STRATEGY=SubmoduleNone when GIT_STRATEGY=GitNone !480
- Update maintainers information !489

v 1.10.8
- Force-terminate VirtualBox and Parallels VMs so snapshot restore works properly !313
- Don't install docs for the fpm Gem !526
- Mention tagged S3 sources in installation documentation !513
- Limit number of concurrent requests to builds/register.json !518
- Replace b.CurrentStage with b.CurrentState where it was misused !530

v 1.10.7
- Update docker-machine version to fix coreos provision !500

v 1.10.6
- Update Makefile (fix permissions on /usr/share/gitlab-runner/) !487

v 1.10.5
- Update packages targets !485

v 1.10.4
- Fix race in helpers/prometheus/log_hook.go: Fire() method !463

v 1.10.3
- Fix crash on machine creation !461

v 1.10.2
- Add ubuntu/yakkety to packages generation list !458
- Reduce size of gitlab-runner-helper images !456

v 1.10.1
- Fix S3 and packagecloud uploads step in release process !455

v 1.10.0
- Make /usr/share/gitlab-runner/clear-docker-cache script /bin/sh compatible !427
- Handle Content-Type header with charset information !430
- Don't raise error if machines directory is missing on machines listing !433
- Change digital ocean autoscale to use stable coreos channel !434
- Fix package's scripts permissions !440
- Use -q flag instead of --format. !442
- Kubernetes termination grace period !383
- Check if directory exists before recreating it with Windows CMD !435
- Add '--run-tagged-only' cli option for runners !438
- Add armv6l to the ARM replacements list for docker executor helper image !446
- Add configuration options for Kubernetss resource requests !391
- Add poll interval and timeout parameters for Kubernetes executor !384
- Add support for GIT_SUBMODULE_STRATEGY !443
- Create index file for S3 downloads !452
- Add Prometheus metric that counts number of catched errors !439
- Exclude unused options from AbstractExecutor.Build.Options !445
- Update Docker Machine in official Runner images to v0.9.0 !454
- Pass ImagePullSecrets for Kubernetes executor !449
- Add Namespace overwrite possibility for Kubernetes executor !444

v 1.9.10
- Force-terminate VirtualBox and Parallels VMs so snapshot restore works properly !313

v 1.9.9
- Update docker-machine version to fix coreos provision !500

v 1.9.8
- Update Makefile (fix permissions on /usr/share/gitlab-runner/) !487

v 1.9.7
- Update packages targets !485

v 1.9.6
- Add ubuntu/yakkety to packages generation list !458

v 1.9.5
- Update Docker Machine in official Runner images to v0.9.0 !454

v 1.9.4
- Add armv6l to the ARM replacements list for docker executor helper image !446

v 1.9.3
- Fix package's scripts permissions !440
- Check if directory exists before recreating it with Windows CMD !435

v 1.9.2
- Handle Content-Type header with charset information !430
- Don't raise error if machines directory is missing on machines listing !433

v 1.9.1
- Make /usr/share/gitlab-runner/clear-docker-cache script /bin/sh compatible !427

v 1.9.0
- Add pprof HTTP endpoints to metrics server !398
- Add a multiple prometheus metrics: !401
- Split prepare stage to be: prepare, git_clone, restore_cache, download_artifacts !406
- Update CONTRIBUTING.md to refer to go 1.7.1 !409
- Introduce docker.Client timeouts !411
- Allow network-sourced variables to specify that they should be files !413
- Add a retry mechanism to prevent failed clones in builds !399
- Remove shallow.lock before fetching !407
- Colorize log entries for cmd and powershell !400
- Add section describing docker usage do Kubernetes executor docs !394
- FreeBSD runner installation docs update !387
- Update prompts for register command !377
- Add volume_driver Docker configuration file option !365
- Fix bug permission denied on ci build with external cache !347
- Fix entrypoint for alpine image !346
- Add windows vm checklist for virtualbox documentation !348
- Clarification around authentication with the Kubernetes executor !296
- Fix docker hanging for docker-engine 1.12.4 !415
- Use lib machine to fetch a list of docker-machines !418
- Cleanup docker cache clear script !388
- Allow the --limit option to control the number of jobs a single runner will run !369
- Store and send last_update value with API calls against GitLab !410
- Add graceful shutdown documentation !421
- Add Kubernete Node Selector !328
- Push prebuilt images to dockerhub !420
- Add path and share cache settings for S3 cache !423
- Remove unnecessary warning about using image with the same ID as provided !424
- Add a link where one can download the packages directly !292
- Kubernetes executor - use pre-build container !425

v 1.8.8
- Update Makefile (fix permissions on /usr/share/gitlab-runner/) !487

v 1.8.7
- Update packages targets !485

v 1.8.6
- Add ubuntu/yakkety to packages generation list !458

v 1.8.5
- Update Docker Machine in official Runner images to v0.9.0 !454

v 1.8.4
- Add armv6l to the ARM replacements list for docker executor helper image !446

v 1.8.3
- Fix package's scripts permissions !440
- Check if directory exists before recreating it with Windows CMD !435

v 1.8.2
- Handle Content-Type header with charset information !430

v 1.8.1
- Rrefactor the private container registry docs !392
- Make pull policies usage clear !393

v 1.8.0
- Fix {Bash,Cmd,Ps}Writer.IfCmd to escape its arguments !364
- Fix path to runners-ssh page !368
- Add initial Prometheus metrics server to runner manager !358
- Add a global index.md for docs !371
- Ensure that all builds are executed on tagged runners !374
- Fix broken documentation links !382
- Bug Fix: use a regex to pull out the service and version in the splitServiceAndVersion method !376
- Add FAQ entry about handling the service logon failure on Windows !385
- Fix "unit tests" random failures !370
- Use correct constant for kubernetes ressource limits. !367
- Unplug stalled endpoints !390
- Add PullPolicy config option for kubernetes !335
- Handle received 'failed' build state while patching the trace !366
- Add support for using private docker registries !386

v 1.7.5
- Update Docker Machine in official Runner images to v0.9.0 !454

v 1.7.4
- Add armv6l to the ARM replacements list for docker executor helper image !446

v 1.7.3
- Fix package's scripts permissions !440
- Check if directory exists before recreating it with Windows CMD !435

v 1.7.2
- Handle Content-Type header with charset information !430

v 1.7.1
- Fix {Bash,Cmd,Ps}Writer.IfCmd to escape its arguments !364

v 1.7.0
- Improve description of --s3-bucket-location option !325
- Use Go 1.7 !323
- Add changelog entries generation script !322
- Add docker_images release step to CI pipeline !333
- Refactor shell executor tests !334
- Introduce GIT_STRATEGY=none !332
- Introduce a variable to enable shell tracing on bash, cmd.exe and powershell.exe !339
- Try to load the InCluster config first, if that fails load kubectl config !327
- Squash the "No TLS connection state" warning !343
- Add a benchmark for helpers.ShellEscape and optimise it !351
- Godep: update github.com/Sirupsen/logrus to v0.10.0 !344
- Use git clone --no-checkout and git checkout --force !341
- Change machine.machineDetails to machine.Details !353
- Make runner name lowercase to work with GCE restrictions !297
- Add per job before_script handling for exec command !355
- Add OffPeak support for autoscaling !345
- Prevent caching failures from marking a build as failed !359
- Add missed "server" command for minio in autoscaled S3 cache tutorial !361
- Add a section for Godep in CONTRIBUTING.md !302
- Add a link to all install documentation files describing how to obtain a registration token !362
- Improve registration behavior !356
- Add the release process description !176
- Fix documentation typo in docs/configuration/advanced-configuration.md !354
- Fix data races around runner health and build stats !352

v 1.6.1
- Add changelog entries generation script !322
- Add docker_images release step to CI pipeline !333

v 1.6.0
- Remove an unused method from the Docker executor !280
- Add note about certificate concatenation !278
- Restore 755 mode for gitlab-runner-service script !283
- Remove git-lfs from docker helper images !288
- Improve Kubernetes support !277
- docs: update troubleshooting section in development. !286
- Windows installation, added a precision on the install command (issue related #1265) !223
- Autodetect "/ci" in URL !289
- Defer removing failed containers until Cleanup() !281
- fix typo in tls-self-signed.md !294
- Improve CI tests !276
- Generate a BuildError when Docker/Kubernetes image is missing !295
- cmd.exe: Caret-escape parentheses when not inside double quotes !284
- Fixed some spelling/grammar mistakes. !291
- Update Go instructions in README !175
- Add APT pinning configuration for debian in installation docs !303
- Remove yaml v1 !307
- Add options to runner configuration to specify commands executed before code clone and build !106
- Add RC tag support and fix version discovering !312
- Pass all configured CA certificates to builds !299
- Use git-init templates (clone) and git config without --global (fetch) to disable recurseSubmodules !314
- Improve docker machine logging !234
- Add posibility to specify a list of volumes to inherit from another container !236
- Fix range mismatch handling error while patch tracing !319
- Add docker+machine and kubernetes executors to "I'm not sure" part of executors README.md !320
- Remove ./git/index.lock before fetching !316

v 1.5.3
- Fix Caret-escape parentheses when not inside double quotes for Windows cmd
- Remove LFS from prebuilt images

v 1.5.2
(no changes)

v 1.5.1
- Fix file mode of gitlab-runner-service script !283

v 1.5.0
- Update vendored toml !258
- Release armel instead arm for Debian packages !264
- Improve concurrency of docker+machine executor !254
- Use .xz for prebuilt docker images to reduce binary size and provisioning speed of Docker Engines !249
- Remove vendored test files !271
- Update gitlab-runner-service to return 1 when no Host or PORT is defined !253
- Log caching URL address
- Retry executor preparation to reduce system failures !244
- Fix missing entrypoint script in alpine Dockerfile !248
- Suppress all but the first warning of a given type when extracting a ZIP file !261
- Mount /builds folder to all services when used with Docker Executor !272
- Cache docker client instances to avoid a file descriptor leak !260
- Support bind mount of `/builds` folder !193

v 1.4.3
- Fix Caret-escape parentheses when not inside double quotes for Windows cmd
- Remove LFS from prebuilt images

v 1.4.2
- Fix abort mechanism when patching trace

v 1.4.1
- Fix panic while artifacts handling errors

v 1.4.0
- Add sentry support
- Add support for cloning VirtualBox VM snapshots as linked clones
- Add support for `security_opt` docker configuration parameter in docker executor
- Add first integration tests for executors
- Add many logging improvements (add more details to some logs, move some logs to Debug level, refactorize logger etc.)
- Make final build trace upload be done before cleanup
- Extend support for caching and artifacts to all executors
- Improve support for Docker Machine
- Improve build aborting
- Refactor common/version
- Use `environment` feature in `.gitlab-ci.yml` to track latest versions for Bleeding Edge and Stable
- Fix Absolute method for absolute path discovering for bash
- Fix zombie issues by using dumb-init instead of github.com/ramr/go-reaper

v 1.3.5
- Fix Caret-escape parentheses when not inside double quotes for Windows cmd

v 1.3.4
- Fix panic while artifacts handling errors

v 1.3.3
- Fix zombie issue by using dumb-init

v 1.3.2
- Fix architecture detection bug introduced in 1.3.1

v 1.3.1
- Detect architecture if not given by Docker Engine (versions before 1.9.0)

v 1.3.0
- Add incremental build trace update
- Add posibility to specify CpusetCpus, Dns and DnsSearch for docker containers created by runners
- Add a custom `User-Agent` header with version number and runtime information (go version, platform, os)
- Add artifacts expiration handling
- Add artifacts handling for failed builds
- Add customizable `check_interval` to set how often to check GitLab for a new builds
- Add docker Machine IP address logging
- Make Docker Executor ARM compatible
- Refactor script generation to make it fully on-demand
- Refactor runnsers Acquire method to improve performance
- Fix branch name setting at compile time
- Fix panic when generating log message if provision of node fails
- Fix docker host logging
- Prevent leaking of goroutines when aborting builds
- Restore valid version info in --help message
- [Experimental] Add `GIT_STRATEGY` handling - clone/fetch strategy configurable per job
- [Experimental] Add `GIT_DEPTH` handling - `--depth` parameter for `git fetch` and `git clone`

v 1.2.0
- Use Go 1.6
- Add `timeout` option for the `exec` command
- Add runtime platform information to debug log
- Add `docker-machine` binary to Runner's official docker images
- Add `build_current` target to Makefile - to build only a binary for used architecture
- Add support for `after_script`
- Extend version information when using `--version` flag
- Extend artifacts download/upload logs with more response data
- Extend unregister command to accept runner name
- Update shell detection mechanism
- Update the github.com/ayufan/golag-kardianos-service dependency
- Replace ANSI_BOLD_YELLOW with ANSI_YELLOW color for logging
- Reconcile VirtualBox status constants with VBoxManage output values
- Make checkout quiet
- Make variables to work at job level in exec mode
- Remove "user mode" warning when running in a system mode
- Create `gitlab-runner` user as a system account
- Properly create `/etc/gitlab-runner/certs` in Runner's official docker images
- Disable recursive submodule fetchin on fetching changes
- Fix nil casting issue on docker client creation
- Fix used build platforms for `gox`
- Fix a limit problems when trying to remove a non-existing machines
- Fix S3 caching issues
- Fix logging messages on artifacts dowloading
- Fix binary panic while using VirtualBox executor with no `vboxmanage` binary available

v 1.1.4
- Create /etc/gitlab-runner/certs
- Exclude architectures from GOX, rather then including
- Update mimio-go to a newest version
- Regression: Implement CancelRequest to fix S3 caching support
- Fix: Skip removal of machine that doesn't exist (autoscaling)

v 1.1.3
- Regression: On Linux use `sh -s /bin/bash user -c` instead of `sh user -c`. This fixes non-login for user.
- Regression: Fix user mode warning
- Fix: vet installation
- Fix: nil casting issue on docker client creation
- Fix: docker client download issue

v 1.1.2
- Regression: revert shell detection mechanism and limit it only to Docker

v 1.1.1
- Fix: use different shell detection mechanism
- Regression: support for `gitlab-runner exec`
- Regression: support for login/non-login shell for Bash

v 1.1.0
- Use Go 1.5
- Change license to MIT
- Add docker-machine based auto-scaling for docker executor
- Add support for external cache server
- Add support for `sh`, allowing to run builds on images without the `bash`
- Add support for passing the artifacts between stages
- Add `docker-pull-policy`, it removes the `docker-image-ttl`
- Add `docker-network-mode`
- Add `git` to gitlab-runner:alpine
- Add support for `CapAdd`, `CapDrop` and `Devices` by docker executor
- Add support for passing the name of artifacts archive (`artifacts:name`)
- Add support for running runner as system service on OSX
- Refactor: The build trace is now implemented by `network` module
- Refactor: Remove CGO dependency on Windows
- Fix: Create alternative aliases for docker services (uses `-`)
- Fix: VirtualBox port race condition
- Fix: Create cache for all builds, including tags
- Fix: Make the shell executor more verbose when the process cannot be started
- Fix: Pass gitlab-ci.yml variables to build container created by docker executor
- Fix: Don't restore cache if not defined in gitlab-ci.yml
- Fix: Always use `json-file` when starting docker containers
- Fix: Error level checking for Windows Batch and PowerShell

v 1.0.4
- Fix support for Windows PowerShell

v 1.0.3
- Fix support for Windows Batch
- Remove git index lock file: this solves problem with git checkout being terminated
- Hijack docker.Client to use keep-alives and to close extra connections

v 1.0.2
- Fix bad warning about not found untracked files
- Don't print error about existing file when restoring the cache
- When creating ZIP archive always use forward-slashes and don't permit encoding absolute paths
- Prefer to use `path` instead of `filepath` which is platform specific: solves the docker executor on Windows

v 1.0.1
- Use nice log formatting for command line tools
- Don't ask for services during registration (we prefer the .gitlab-ci.yml)
- Create all directories when extracting the file

v 1.0.0
- Add `gitlab-runner exec` command to easy running builds
- Add `gitlab-runner status` command to easy check the status of the service
- Add `gitlab-runner list` command to list all runners from config file
- Allow to specify `ImageTTL` for configuration the frequency of docker image re-pulling (see advanced-configuration)
- Inject TLS certificate chain for `git clone` in build container, the gitlab-runner SSL certificates are used
- Remove TLSSkipVerify since this is unsafe option
- Add go-reaper to make gitlab-runner to act as init 1 process fixing zombie issue when running docker container
- Create and send artifacts as zip files
- Add internal commands for creating and extracting archives without the system dependencies
- Add internal command for uploading artifacts without the system dependencies
- Use umask in docker build containers to fix running jobs as specific user
- Fix problem with `cache` paths never being archived
- Add support for [`cache:key`](http://doc.gitlab.com/ce/ci/yaml/README.html#cachekey)
- Add warnings about using runner in `user-mode`
- Push packages to all upcoming distributions (Debian/Ubuntu/Fedora)
- Rewrite the shell support adding all features to all shells (makes possible to use artifacts and caching on Windows)
- Complain about missing caching and artifacts on some executors
- Added VirtualBox executor
- Embed prebuilt docker build images in runner binary and load them if needed
- Make possible to cache absolute paths (unsafe on shell executor)

v 0.7.2
- Adjust `umask` for build image
- Use absolute path when executing archive command
- Fix regression when variables were not passed to service container
- Fix duplicate files in cache or artifacts archive

v 0.7.1
- Fix caching support
- Suppress tar verbose output

v 0.7.0
- Refactor code structure
- Refactor bash script adding pre-build and post-build steps
- Add support for build artifacts
- Add support for caching build directories
- Add command to generate archive with cached folders or artifacts
- Use separate containers to run pre-build (git cloning), build (user scripts) and post-build (uploading artifacts)
- Expand variables, allowing to use $CI_BUILD_TAG in image names, or in other variables
- Make shell executor to use absolute path for project dir
- Be strict about code formatting
- Move network related code to separate package
- Automatically load TLS certificates stored in /etc/gitlab-runner/certs/<hostname>.crt
- Allow to specify tls-ca-file during registration
- Allow to disable tls verification during registration

v 0.6.2
- Fix PowerShell support
- Make more descriptive pulling message
- Add version check to Makefile

v 0.6.1
- Revert: Fix tags handling when using git fetch: fetch all tags and prune the old ones

v 0.6.0
- Fetch docker auth from ~/.docker/config.json or ~/.dockercfg
- Added support for NTFSSecurity PowerShell module to address problems with long paths on Windows
- Make the service startup more readable in case of failure: print a nice warning message
- Command line interface for register and run-single accepts all possible config parameters now
- Ask about tags and fix prompt to point to gitlab.com/ci
- Pin to specific Docker API version
- Fix docker volume removal issue
- Add :latest to imageName if missing
- Pull docker images every minute
- Added support for SIGQUIT to allow to gracefully finish runner: runner will not accept new jobs, will stop once all current jobs are finished.
- Implicitly allow images added as services
- Evaluate script command in subcontext, making it to close stdin (this change since 0.5.x where the separate file was created)
- Pass container labels to docker
- Force to use go:1.4 for building packages
- Fix tags handling when using git fetch: fetch all tags and prune the old ones
- Remove docker socket from gitlab/gitlab-runner images
- Pull (update) images and services every minute
- Ignore options from Coordinator that are null
- Provide FreeBSD binary
- Use -ldflags for versioning
- Update go packages
- Fix segfault on service checker container
- WARNING: By default allow to override image and services

v 0.5.5
- Fix cache_dir handling

v 0.5.4
- Update go-dockerclient to fix problems with creating docker containers

v 0.5.3
- Pin to specific Docker API version
- Fix docker volume removal issue

v 0.5.2
- Fixed CentOS6 service script
- Fixed documentation
- Added development documentation
- Log service messages always to syslog

v 0.5.1
- Update link for Docker configuration

v 0.5.0
- Allow to override image and services for Docker executor from Coordinator
- Added support for additional options passed from coordinator
- Added support for receiving and defining allowed images and services from the Coordinator
- Rename gitlab_ci_multi_runner to gitlab-runner
- Don't require config file to exist in order to run runner
- Change where config file is stored: /etc/gitlab-runner/config.toml (*nix, root), ~/.gitlab-runner/config.toml (*nix, user)
- Create config on service install
- Require root to control service on Linux
- Require to specify user when installing service
- Run service as root, but impersonate as --user when executing shell scripts
- Migrate config.toml from user directory to /etc/gitlab-runner/
- Simplify service installation and upgrade
- Add --provides and --replaces to package builder
- Powershell: check exit code in writeCommandChecked
- Added installation tests
- Add runner alpine-based image
- Send executor features with RunnerInfo
- Verbose mode by using `echo` instead of `set -v`
- Colorize bash output
- Set environment variables from bash script: this fixes problem with su
- Don't cache Dockerfile VOLUMEs
- Pass (public) environment variables received from Coordinator to service containers

v 0.4.2
- Force GC cycle after processing build
- Use log-level set to info, but also make `Checking for builds: nothing` being print as debug
- Fix memory leak - don't track references to builds

v 0.4.1
- Fixed service reregistration for RedHat systems

v 0.4.0
- Added CI=true and GITLAB_CI=true to environment variables
- Added output_limit (in kilobytes) to runner config which allows to enlarge default build log size
- Added support for custom variables received from CI
- Added support for SSH identity file
- Optimize build path to make it shorter, more readable and allowing to fix shebang issue
- Make the debug log human readable
- Make default build log limit set to 4096 (4MB)
- Make default concurrent set to 1
- Make default limit for runner set to 1 during registration
- Updated kardianos service to fix OSX service installation
- Updated logrus to make console output readable on Windows
- Change default log level to warning
- Make selection of forward or back slashes dependent by shell not by system
- Prevent runner to be stealth if we reach the MaxTraceOutputSize
- Fixed Windows Batch script when builds are located on different drive
- Fixed Windows runner
- Fixed installation scripts path
- Fixed wrong architecture for i386 debian packages
- Fixed problem allowing commands to consume build script making the build to succeed even if not all commands were executed

v 0.3.4
- Create path before clone to fix Windows issue
- Added CI=true and GITLAB_CI=true
- Fixed wrong architecture for i386 debian packages

v 0.3.3
- Push package to ubuntu/vivid and ol/6 and ol/7

v 0.3.2
- Fixed Windows batch script generator

v 0.3.1
- Remove clean_environment (it was working only for shell scripts)
- Run bash with --login (fixes missing .profile environment)

v 0.3.0
- Added repo slug to build path
- Build path includes repository hostname
- Support TLS connection with Docker
- Default concurrent limit is set to number of CPUs
- Make most of the config options optional
- Rename setup/delete to register/unregister
- Checkout as detached HEAD (fixes compatibility with older git versions)
- Update documentation

v 0.2.0
- Added delete and verify commands
- Limit build trace size (1MB currently)
- Validate build log to contain only valid UTF-8 sequences
- Store build log in memory
- Integrate with ci.gitlab.com
- Make packages for ARM and CentOS 6 and provide beta version
- Store Docker cache in separate containers
- Support host-based volumes for Docker executor
- Don't send build trace if nothing changed
- Refactor build class

v 0.1.17
- Fixed high file descriptor usage that could lead to error: too many open files

v 0.1.16
- Fixed systemd service script

v 0.1.15
- Fix order of executor commands
- Fixed service creation options
- Fixed service installation on OSX

v 0.1.14
- Use custom kardianos/service with enhanced service scripts
- Remove all system specific packages and use universal for package manager

v 0.1.13
- Added abstraction over shells
- Moved all bash specific stuff to shells/bash.go
- Select default shell for OS (bash for Unix, batch for Windows)
- Added Windows Cmd support
- Added Windows PowerShell support
- Added the kardianos/service which allows to easily run gitlab-ci-multi-runner as service on different platforms
- Unregister Parallels VMs which are invalid
- Delete Parallels VM if it doesn't contain snapshots
- Fixed concurrency issue when assigning unique names

v 0.1.12
- Abort all jobs if interrupt or SIGTERM is received
- Runner now handles HUP and reloads config on-demand
- Refactored runner setup allowing to non-interactive configuration of all questioned parameters
- Added CI_PROJECT_DIR environment variable
- Make golint happy (in most cases)

v 0.1.11
- Package as .deb and .rpm and push it to packagecloud.io (for now)

v 0.1.10
- Wait for docker service to come up (Loïc Guitaut)
- Send build log as early as possible

v 0.1.9
- Fixed problem with resetting ruby environment

v 0.1.8
- Allow to use prefixed services
- Allow to run on Heroku
- Inherit environment variables by default for shell scripts
- Mute git messages during checkout
- Remove some unused internal messages from build log

v 0.1.7
- Fixed git checkout

v 0.1.6
- Remove Docker containers before starting job

v 0.1.5
- Added Parallels executor which can use snapshots for fast revert (only OSX supported)
- Refactored sources

v 0.1.4
- Remove Job and merge it into Build
- Introduce simple API server
- Ask for services during setup

v 0.1.3
- Optimize setup
- Optimize multi-runner setup - making it more concurrent
- Send description instead of hostname during registration
- Don't ask for tags

v 0.1.2
- Make it work on Windows

v 0.1.1
- Added Docker services

v 0.1.0
- Initial public release
