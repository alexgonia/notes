BybitSecret(
	"ByBit-001-UnifiedTrading",
	bybit_secrets["ByBit-001-UnifiedTrading_api_key"],
	bybit_secrets["ByBit-001-UnifiedTrading_api_secret"],
),
BybitSecret(
	a.account_id,
	bybit_secrets[f"{a.account_id}_api_key"],
	bybit_secrets[f"{a.account_id}_api_secret"],
),

### Current whitelist
#### SG VPCE
52.220.30.99 <<<<< current SG VPCE

#### TK VPCE
52.220.30.99

#### cirrus
203.55.214.248/32
203.55.214.250/32

#### unknown - assuming old cirrus, not in our AWS account
13.215.25.25
13.251.224.223
18.142.211.23
18.142.59.99
18.143.209.16
3.1.2.58
Solved: [[oldcirrus]]

## Future whitelist needed
52.220.30.99 <-- backup SG VPCE path

#### high tier cirrus
203.55.214.250
203.55.214.242
203.55.214.248
203.55.214.240

#### low tier cirrus
18.140.161.240
52.74.20.47
52.76.242.84
13.229.163.118
18.142.131.120

#### randomly cirrus token
13.251.220.127

### Finalized
52.220.30.99
203.55.214.250
203.55.214.242
203.55.214.248
203.55.214.240
18.140.161.240
52.74.20.47
52.76.242.84
13.229.163.118
18.142.131.120


## Endpoints


http-mm-vpce:9014 -> 8083 -> y3gtgmgwc2vk7xcpkrwrx5sam65zuy5a.bybit.com
http-vpce:9013 -> 8081 -> api.bybit.com (keep VPC endpoint)
ws-vpce:9012 -> 8080 -> vkmvynjr8moppg2w5kg55jjwiur39z7e.bybit-aws.com

mm websocket 
`y3gtgmgwc2vk7xcpkrwrx5sam65zuy5a.bybit.com`
/v5/private​
/v5/trade​
/v5/public/linear​
/v5/public/inverse​
/v5/public/spot​
/v5/public/option​

mm gateway
/v5/order/*
/v5/position/*
/v5/execution/list
/v5/account/wallet-balance
