rtb-server
==========

RTB server mocks and benchmarks.

# Specifications
## for SSP side
### Auction
- 1st price auction

### Routes

- /ad
  - method: GET
  - parameters
      - dsp: total DSP number.
      - dN_t: DSP bid response time.
      - dN_s: DSP bid response status.
      - dN_p: DSP bid response auction price.

## for DSP side
### Routes

- /ad/dN
  - method: GET 
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
	$ bundle exec ./bin/make_scenario --help
