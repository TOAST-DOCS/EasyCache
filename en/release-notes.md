## Database > EasyCache > Release Notes

### February 23, 2021

#### Feature Updates

* Added read-only domain tooltip

#### Bug Fixes

* Fixed an issue where no replicated group is created if the maximum value is entered for a profile.

### Nov 24, 2020

#### Improvements/changes

* View All Logs added

### January 26, 2021

#### Feature Updates

- Changed Maxmemory default from 70% to 50% of available memory
- Added `activedefrag`-related options in profile
- **View Log**  dialog box UI improved

#### Bug Fixes

- Fixed a bug where the date changes to January 2 when the time is changed in monitoring

### December 29, 2020

#### More Features

- Added read-only domain feature

#### Feature Updates

- Improved the feature related to login control information
- Improved to show guidance when mouse is hovered over the Change instance type button
- Changed the dialog button name to OK.

#### Bug Fixes

- Fixed an issue where the task of profile modification fails and made unavailable when changing the profile of a duplicate group if the profile before the change is modified
- Fixed an issue of Korean filter option names were displayed when the website language is set to 'Japanese'

### October 27, 2020

#### Bug Fixes

- Modified node name to reflect changes in group name when changing name of duplicate group
- Modified error message in cases where a quarter of CPU and RAM is exceeded

### September 22, 2020

#### Feature Updates

- Korea (Pyeongchon) region opened
- Added log check feature
- Sort and display VPC subnet list by name
- Service use permissions response

#### Bug Fixes

- Modified unit of monitoring graph
  - Input byte: byte -> bytes/1min
  - Output byte: byte -> bytes/1min
  - Processed commands per second: counts/seconds -> count/1sec
- During profile modification, the bug where the status of a duplicate group using the profile currently being modified is displayed as normal rather than displaying modification in progress

### August 25, 2020

#### Feature Updates

- Changed the password setting for Redis access as optional

#### Bug Fixes

- Fixed an issue where node promotion completion time and condition display does not accord when promoting replica nodes

### July 28, 2020

#### More Features

- Instance type change feature added

#### Feature Updates

- Deleted Compute Optimized type from supported instance type

#### Bug Fixes

- Fixed an issue where clients connected from monitoring graph is displayed as an accumulation
- Fixed a bug where, when restoring from Redis 3.2.12 duplicate group which used custom profile, the profile would be restored to Redis 3.2 default profile

### June 23, 2020

#### Feature Updates

- Registered events on CloudTrail service

#### Bug Fixes

- Fixed an issue in which the operation duration (uptime_in_seconds) of INFO’s Redis server is displayed in values with additional 9 hours
- Fixed an issue where, when users click the View button to check their passwords, nodes fail to acquire passwords during node failures
- Fixed an issue where HA reset fails even after HA reset button is displayed and reset is executed
- Fixed an issue where dates could not be selected freely from search period on the monitoring screen

### May 26, 2020

#### Feature Updates

- Redis 5.0 supported
- Profile copying feature provided
- Monitoring updated
  - Moved query tab from duplicate group details screen to a separate tab on top of the initial screen
  - Added Current Time button
  - Added Auto Renew checkbox
  - Added duplicate group selection drop-down menu
  - Updated single graph to be displayed additionally as a pop-up to allow users to select statistical entries and aggregation duration
- Changed features to allow user to modify values through detailed settings when creating or modifying profiles

#### Bug Fixes

- Fixed an issue where the modification button is disabled when trying to modify duplicate groups with no nodes added after modifying duplicate groups with added nodes
- Fixed a bug where 「Number of Connected Clients」 and 「Number of Blocked Clients」 on the monitoring option is displayed as an accumulation value
- Fixed an issue where the profile list is not fully displayed after modification
- Fixed an issue where the screen does not reload after modifying profiles currently being used by duplicate groups

### April 28, 2020

#### Feature Updates

- Provided feature to allow users to enable health check response time on watch setting
- Provided master manual promotion feature
- Changed a monitoring field to display successful/failed query numbers as per time instead of an accumulation value
- Changed alarm rules to allow changing memory usage in %

#### Bug Fixes

- Fixed an issue where monitoring graphs are partially displayed every 10 minutes
- Fixed an issue where duplicate group and node status is not properly reflected after failed nodes are restored within a few seconds after a failover
- Made changes to allow password modification of warning duplicate groups
- Modified a portion of menus and labels

### March 24, 2020

#### Feature Updates

- Changed default config value of EasyCache(tcp-keepalive [0→300])

### February 25, 2020

#### Feature Updates

- Modified feature to allow users to simultaneously add multiple connection information
- Updated SMS content
- Modified messages when entering duplicated CIDR

#### Bug Fixes

- Fixed an issue where infinite loops of data synchronization occurs when replica node is added in presence of bulk data
- Fixed an issue where node is displayed as creating on node alarm even after node creation failure within a duplicate group

### February 11, 2020

#### Feature Updates

- Upgraded version of NHN Cloud user authentication module

#### Bug Fixes

- Fixed an issue where selection fails in cases of selecting VPC subnets of users that did not set up internet gateways when creating duplicate groups

### January 21, 2020

#### Feature Updates

- Japanese supported for console screen and event messages
- Event registration added when domain change fails after failover

### December 24, 2019

#### New service release

- NHN Cloud EasyCache is a service that provides Redis(REmote DIctionary Server)in a cloud environment.
