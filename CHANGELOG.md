# Changelog Sysinfo Viewer

## [3.2 beta1] - 2018-05-06

### Added
- support for CAS system information files up to version 2.3, although there's not much useful information in them
- the VPM CPL file can now be viewed and downloaded
- experimental option to export/download some of the generated graphs as PNG, JPEG and PDF (still have to make sure it works without Internet and correct some scaling issues)
- a .htaccess file to overwrite the original values for post_max_size and upload_max_filesize to "150M", saves you to edit the original php.ini, it's also better compared to set those values globally, and it makes it easier to deploy in a docker container ;)
- some translations to the sysinfo tags (like HTTP_MAIN...) to the Sysinfo in sections view, not for all tags, just for the ones I've used already
- a new interactive Current overall Policy view to replace the old one which I removed (see below)
  (Note: this is not perfect. I noticed problems with universal policies installed from the cloud services. Please use the plain policy view in such cases.)

### Changed
- heavily optimized initial parsing of snapshot files by using the snapshot size values to calculate jumps within the snapshot file, first time parsing of snapshot archives is now blazingly fast and neglectible compared to the time it takes to uncompress the files, in one example it brought parsing time down from 49 seconds to 0.008 seconds
- changed Sysinfo in sections to Bootstrap collapse style, replacing the custom script that I used before
- current plain policy view is now really is what it says, just a plain view, no links etc. for anyone who needs to look at the original current policy as found in the sysinfo
- redid the XML-pretty-print for displaying the inline CAS config for ASG

### Fixed
- a bug in the VPM policy view regarding combined objects where the second part is negated. It should now correctly show "... AND  None of these objects"

### Removed
- the old Current overeall Policy view, it was not working properly for versions 6.6+ and instead of reparing it I tried to come up with something new to replace it


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
