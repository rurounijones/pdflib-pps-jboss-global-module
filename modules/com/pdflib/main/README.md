# PDFLib PPS Global Module

PDFLib ( http://www.pdflib.com ) "PDFLib Personalization Server library" wrapped in a JBoss AS7 global module.

This will allow Java (or JRuby) applications running on your JBoss (or Torquebox) installation to access the evaluation version
of PDFLib Version 8.

## Supported operating systems.

This repository contains the required library files to support 32bit and 64bit Windows and Linux
operating systems. Other operating systems can be added by reading the following documentation

https://docs.jboss.org/author/display/MODULES/Native+Libraries

And adding the OS specific library files in the correct locations according to the rules specified.

## Install

### Server modifications

Use the downloads section of this repository to download a .zip or .tar.gz file and extract it to the
root of your JBOSS server installation. 

After extraction open your JBoss configuration file (for example domain/standalone.xml) and edit/add the following:

	<subsystem xmlns="urn:jboss:domain:ee:1.0">
		<global-modules>
			<module name="com.pdflib" slot="main" />
		</global-modules>
	</subsystem>

### Application modifications

In your application'S WEB-INF folder please add the following to your jboss-deployment-descriptor.xml file

	<jboss-deployment-structure>
		<deployment>
			<dependencies>
				<module name="com.pdflib" />
			</dependencies>
		</deployment>
	</jboss-deployment-structure>

## Support

This global module code was created by a user of PDFLib and is not supported by PDFLib GmbH. 
If you have any issues please raise an issue on the github issue tracker.

## Licensing

### PDFLib

For licensing of PDFLib please visit the http://www.pdflib.com website
For Terms and Conditions of using PDFLib please
see http://www.pdflib.com/fileadmin/pdflib/pdf/license/PDFlib-terms-and-conditions.pdf

### Global Module

The code written to wrap the PDFLib library is released under the MIT License (Please see the LICENSE file).
