clean:
	rm -rf test-*/*.json test-*/*.png test-*/*.mp4 test-*/logs

# @external/@pending features are excluded so the default run is deterministic:
#   * @external features hit live third-party sites/APIs that drift (run on demand
#     with: --tags @external)
#   * @pending scenarios are intentionally-undefined step demos
test:
	auto-runner.py --project ${ABDD_PROJECT} --rerunfailed=1 -- --cucumberOpts.tags='not @external and not @pending'
