- Split Market data feed [[Split MD]]
- Roy - consider enabling tailscale autogroup:self ssh policy
	- Probably not, don't want to start random machines. Look into it more
- Adjust leverage trade alerts
- Figure out how to store more secrets in databricks' dbutils.secrets.get(scope="general-secrets", key="slack_token")
- Reduce cloud cost databricks S3
	- Kicked off S3 inventory daily job for databricks-prototype-ergonia on 2025-04-04. Should be ready on 2025-04-06
	- Inventory is ready, about 100M files. Need to figure out strategy to
		- Reduce cost
		- Simplify
	- Next step is to wrap my head around the shape of files, usage
	- DELETE API calls are free
- Review cloud cost in general [[AWS Cost management]]
- Structured log proof of concept with Sam - loki
- Move from horizon/drw network to AWS systems manager
	- Vault access - useful for development (read only keys to services we integrate with, ie: exchanges)
	- Uniform login to prod for certain ppl
		- Very subject to improving who has access, how, from where to our AWS account
- Review KMS as replacement for DRW vault
- Review bandwidth monitoring for all ergonia interfaces
	- No easy answer, need to speak with diego to setup new tap potentially
		- Seems like current inputs are not far off the real thing.. could just tweak telegraf prod config
	- potentially ebpf setup
	- http://3.112.212.58:9090/d/cdui3uxlyc9a8c/host-system-and-docker-container-metrics?orgId=1&from=now-5m&to=now&timezone=browser
	- Some metrics there, some are in TB/s so it must be wrong units
- Onboard new cirrus /healthcheck endpoint
- Get ready to have a fast path between tokyo and Frankfurt
- Review phantom wallet documentation
- Find the discord for the validator and figure out whats needed to run one with the firedancer client
- Make a dump of the VRF configs, routing tables, dns configs, etc on the prod server
	- Partially done, add each VRF routing table and we should be good...
- Upgrade kernel
	- Currently on `Linux ty2e-supegsz01 5.15.0-121-generic #131-Ubuntu SMP Fri Aug 9 08:29:53 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux`
	- Upgrade to 6.12 to allow for 
		- `io_uring` improvements
		- multishot rx
		- better buffer management
		- zc send
		- general performance improvements
	- Eventually ideally 6.15, but not stable yet







