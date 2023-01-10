# Changelog

This changelog lists all additions and updates to the Adatree CDR APIs, in chronological order.

### January 9, 2023

- Add support for `accountOwnership` to Bank Account list and Bank Account Detail. The value indicating the number of customers that have ownership of the account, according to the data holder's definition of account ownership. 
Does not indicate that all account owners are eligible consumers. Values are `UNKNOWN`, `ONE_PARTY`, `TWO_PARTY`, `MANY_PARTY`, or `OTHER`.
- Add support for new value `DIGITAL_WALLET` on enum Payee.type to Payee list for both standard CDR API and Data API
- Add support for new value `digitalWallet` on enum PayeeDetail.payeeUType to Payee detail for both standard CDR API and Data API
- Add support for `digitalWallet` to Payee Detail on standard CDR API
- Add support for `digitalWallet` to Payee Detail and Payee list on Data API for Payees
- Add support for `occupationCodeVersion` to Person Customer basic and Customer detail for both standard CDR API and Data API
  - The applicable [ANZSCO] release version of the occupation code provided. Mandatory if an occupationCode is supplied. If occupationCode is supplied but occupationCodeVersion is absent, default is ANZSCO_1220.0_2013_V1.2
  - Values are ANZSCO_1220.0_2006_V1.0, ANZSCO_1220.0_2006_V1.1, ANZSCO_1220.0_2013_V1.2, or ANZSCO_1220.0_2013_V1.3. Default value is ANZSCO_1220.0_2013_V1.2. 
- Add support for `industryCodeVersion` to Organisation Customer basic and Customer detail for both standard CDR API and Data API
  - The applicable ANZSIC release version of the industry code provided. Should only be supplied if industryCode is also supplied. If industryCode is supplied but industryCodeVersion is absent, default is ANZSIC_1292.0_2006_V2.0.
  - Values are ANZSIC_1292.0_2006_V1.0 or ANZSIC_1292.0_2006_V2.0. Default value is ANZSIC_1292.0_2006_V2.0.