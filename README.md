ignite chain serve
make test-module-{MODULE_NAME}
make test-all-keepers
This guide will help you set up the Astraeus API server on the Suave Toliman Testnet to easily to use Transferable Acccounts.
# Steps
1. Copy the example environment file to creatr your own .env file:
   cp .env .example .env
2. Edit the .env file and set the PRIVATE_KEY to the private key of an account ath holds tokens on the Suave network.
3. Start the API server using Docker:
  make run-api-server-docker
At this point, the API server should be running locally via Docker.
4. Generate the Timed Signature required for API requests. Replace validFor with the UnixTime until which the signature is valid
   go run scripts/utils
