# Changelog Sysinfo Viewer

## [3.1 beta3] - 2018-03-27

### Added
- this CHANGELOG.md
- the default services are now shown by name instead of a simple "default" under Configuration > Active Services 

### Changed
- Event Log is now shown in a searchable datatable, it can take a while to load, but is easier to work with
- modified the upload script to enable file selection and upload by clicking on the drag&drop area
- when selecting a particular snapshot from sysinfo or sysinfo_stats file selection the snapshot is now opened in a new window/tab to preserve the selection page
- ADN Configuration page was overhauled completely

### Fixed
- links to EOL and Release information on the Home page now point to the symantec.com website
- links to the Knowledgebase from Event Log Summary now point to the symantec.com website
- solved an issue where one could not open the Configuration menu item when in Traffic Mix, forgot to include a script
- title tag of the HTML page (which is seen in the browser tab) now shows correct Sysinfo Viewer version and file name

### Removed
- menu item HTTP Proxy Settings under Configuration, it was wrong for later versions because the defaults changed and not usefull enough to fix it


## [3.1 beta2] - 2018-03-11

### Added
- new translations for some OPP and TCP tags
- new Application Group object in VPM Viewer (introduced in SGOS 6.7.2.1)
- the Content Filter status under Feature Overview on the Home page now lists the data source 

### Changed
- OPP (ICAP) services are now displayed side-by-side in a table under External Services (ICAP)

### Fixed
- for some sysinfos with lots of active services (mainly ADN) the stats graphics under Services on the Home page where only displayed for the first three or four services, this was resolved by updating to a newer jQuery version
- the Content Filter status under Feature Overview on the Home page was not shown correctly due to a mistake in the parsing script


## [3.1 beta1] - 2017-06-30


## [3.0 beta3] - 2016-10-22
