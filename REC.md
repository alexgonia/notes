Getting positions from exchanges, onchain
Cefi / solgizmo process

Another process to calculate deltas, pnls

splitting the writing feed handlers out in a separate container
calculate positions instead of going on solscan or different exchanges

need to be able to see those things when the rest of system is down

Supposed to be a new UI

3 process out of the current proces
- solgizmo subscription
	- write only process from onchain
- cefi positions feed
- new process for UI