https://phantom.com/
https://aws.amazon.com/kms/

## AWS KMS setup in theory
- Create a customer managed secret
- Take that kms secret to encrypt the key with KMS
- KMS policy
	- Only the specific app ARN is allowed to decrypt
	- Create a 
