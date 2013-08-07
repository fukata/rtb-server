rtb-server
==========

RTB server mocks and benchmarks.

# Specifications
## for SSP side
### routes

- /ad
  - method: GET
  - parameters
    - dsp: total DSP number.
    - dN_t: DSP bid response time.
    - dN_s: DSP bid response status.
    - dN_p: DSP bid response auction price.

## for DSP side
### routes

- /ad/dN
  - method: POST
  - parameters
    - t: bid response time.
    - s: bid response status.
    - p: auction price.
  - response
	  - format: json

===
	{
		"id": "${UNIQUE BID ID}",
		"price": "${PRICE}"
	}

# Benchmak
## Make Scenario
	$ ./bin/make_scenario --help

## Execution AD Request to SSP side
	$ ./bin/bench_ssp --help

## Execution AD Request to DSP side
	$ ./bin/bench_dsp --help
