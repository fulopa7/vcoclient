# Changelog

All notable changes to this project will be documented in this file.

## [0.1.8] - 2019-10
## Added:
- added edges_get_agg_lm to get aggregated link statistics
- added stats option to almost every method. Didn't documented it yet but a very cool feature!

## Changed:
- architecture change on how arguments are getting generated
- now login and logout are new methods in the class

## [0.1.7] - 2019-08
### Added:
- gateway_get_edges is a new method which gets the edges behind a given gateway
- enterprise_get_gateway is a new method which gets the gateways behind edges 

### Changed:
- edges_get method parameter ``id`` changed to ``enterpriseid`` to make sure we are consistent
- get_edges_lm method will convert user time to epoch to be more consistant
- Updated README to reflect new methods and changes

## [0.1.4] - 2019-07
### Changed:
- Fixing bug in setup.py

## [0.1.3] - 2019-07
### Added:
- new method for ``edge_get_lm`` which gets the link_metric of a given edge for a given enterprise.
- Added more description to given methods in argparse.
- Added envionment variables for verifying SSL (VCO_VERIFY_SSL) and cookie path (VCO_COOKIE_PATH)
### Changed:
- Fixing API payload extraction 
- Fixing error handling when method is not defined
- Making setup.py more reliable e.g. installing not from directory itself

## [0.1.2] - 2019-06
### Changed:
- Fixing bug in logout
- Added travis testing for overall package

## [0.1.1] - 2019-06
### Changed:
- Fixing bug in setup.py
- Printing out help if no method used in vcoclient.py

## [0.1] - 2019-06
### Added:
- Installation support now via pip3 install vcoclient
### Changed:
- Documentation in vcoclient.py, README and Changelog

## [0.0.7] - 2019-06
### Changed:
- There is now a ``msp_customers_get``and a ``operator_cusgtomers_get`` to support operator or partner customers respectively. Thereby ``customers_get``has been removed
- Better error handling for exceptions in execusion class.
- Printing only out something if there is anything to print out after execusion has happened.
- Handling invalid user/password and missing cookie better

## [0.0.6] - 2019-06
### Changed:
- Merged functions into one Class for easier creating new methods for vcoclient. Rather then having a function for each argparse, we have one Class taking care of it.
### Removed:
- Fixed warning issue with Pandas renaming syntax of index
- Removed memory footprint of variables

## [0.0.5] - 2019-06
### Added:
- Using getpass for ``--password`` to make it more secure.
- Adding os.env option for username (VCO_USER), password (VCO_PASS) and host (VCO_HOST) for easiness.
- Adding functionality to get row names only via ``--rows_name`` from results.
### Change:
- Handling hostname has changed and will raise exception if not given via os or input by user.
- Handling data structure more efficiently (e.g. unpacking only needed value from list)

## [0.0.4] - 2019-06
### Added:
- ``--search`` in edges_get for searching any value related to edges properties. Gives one a powerful method to extract/compare values between many edges.
### Changed:
- Method login and logout will not return True anymore but will just execute as is and will raise an exception otherwise.
        
## [0.0.3] - 2019-05 
### Added:
- Output of Pandas, JSON or CSV, will have the name of the Edge rather as a returned index. Simpler to read.
- ``--filters`` lets user to filter output more granular
- User can now define another enterprise ID rather then the default 1 
### Changed:
- ``--search`` changed to ``--name``in edges_get, reflecting really what is filtered

## [0.0.2] - 2019-05
### Added:
- README, Licences, and fixes bugs in vcoclient.py

## [0.0.1] - 2019-05
- First versions


