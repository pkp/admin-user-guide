# Appendix B: Configure the Statistics Framework

This section is only relevant to those using OJS 2.4.3+ and OJS 3.0+. Older versions of OJS do not have this framework, and need no configuration.

In most cases, the Statistics Framework should “just work”, in particular with fresh installs. Just the same, there are a number of configuration options available to you, and should be reviewed after installation or upgrade. You also need to put in place some sort of mechanism to run scheduled tasks so that usage stats are processed regularly.

**Note for Journal Managers and Editors:** Most of the following steps would be considered expert-level, and should only be undertaken by Site Administrators and systems administrators. If you have questions about the more advanced issues presented here, consult with your service provider. The main exception to this is the Statistics Display option described in the next section. If you want to publicly display article usage statistics on article abstract pages, you can enable this option.

There are three configuration steps that you will have to consider: configuring the usage statistics plugin, configuring scheduled tasks, and configuring regional data tracking, if you want to track regional data. \(OJS can track country, region and city data.\)

## Configure the Usage Statistics Plugin

* Enable “Create Log Files” if it isn’t enabled already
* Leave the “Parse Log File Regex” option alone unless you know what you are doing
* Leave the “Compress Archives” option disabled, unless server space is a consideration \(see the Troubleshooting section below\)
* Leave the “Data Privacy Option disabled, unless you can follow the instructions provided
* Enable the “City” and “Region” options, and follow the section on Configuring Regional Data Tracking below
* If available in your OJS install, consider enabling the Statistics Display Options if you want basic abstract and galley views to be available on article landing pages

We won’t go into detail for every single configuration option for the plugin, but we do suggest the following as a reasonable setup:  


In order to enable the collection of usage data, make sure that this plugin is enabled.  


Dashboard &gt; Settings &gt; Website &gt; Plugins &gt; Generic Plugins &gt; Usage Statistics Plugin &gt; Settings  


… and in OJS 3 by going to:  


User Home &gt; Journal Manager &gt; System Plugins &gt; Generic Plugins &gt; Usage Statistics Plugin &gt; Settings  


OJS 2.4.3+ and 3+ include a generic Usage Statistics Plugin that is responsible for how these statistics are logged and recorded in the system. The plugin’s default configurations are reasonable, and work for most use cases, though you will want to review them after you install or upgrade OJS. The plugin settings can be found in OJS 2 by going to:  


  
  
  


