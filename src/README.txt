
1. PROJECTS

There are two projects included in this distribution:  ical2rdf.csproj and ICalParser.csproj.  

The ICalParser.csproj project will build a .Net assembly API dll that can be included in other .Net projects.  Please refer to the source code for more information on the use of this library.

The ical2rdf.csproj project will build a stand-alone command-line executable called ical2rdf.exe.  The purpose of this program is to convert RFC2445 iCalendar format files to the proposed iCalendar RDF/XML format (see http://www.w3.org/2002/12/cal/ for more info on the W3C working group responsible for the iCalendar RDF schema development).

Here's the usage of ical2rdf:

    ical2rdf [-chp][-x | -f rdffile] icalfile1 [icalfile2 ... icalfileN]

	options:
	    c - print copyright information
	    h - print help/usage information
	    p - supress output of error messages - will force a file to be 
		written out regardless of error conditions (should be used 
		for debugging only)
	    x - name all rdf output files with the same name as their 
		corresponding iCalendar files, except with an '.rdf' suffix
	    f rdffile - generate the RDF file with the given name.  If 
		multiple iCalendar files are specified this option is ignored
	    icalfileN - the iCalendar (RFC2445) file(s) that are to be parsed.
		These must be the last parameters in the command.  This 
		program will not expand wildcard characters

		NOTE: icalfiles will be assumed to be files on a local 
		filesystem or mounted network drives.  If you prefix the 
		name with 'http:', it will be fetched from the internet 
		URL supplied. No attempt will be made to do any Authentication 
		for internet fetches.


2. BUILD and INSTALL

To build this software, you will need MS Visual Studio developement environment (or some other .Net development tools ;) ) and the .Net runtime environment.  This software was developed using Visual Studio v7.1 for .Net v1.1

For each project, there are two different configurations.  DEBUG and RELEASE.  The DEBUG configuration generates extra debugging code, but it also enables the csUnit unit test cases included in the software.  If you don't have csUnit - just switch over to the RELEASE configuration to do the build.  csUnit is an awesome little product, though, so while you're at it, why don't you go and grab it over at:  http://www.csunit.org

For those who don't have a development environment but want to run the ical2rdf.exe converter program - there's two steps:

- get the .Net runtime installed in your machine.  The recommended way of doing this is to run Windows Update on our machine and select the .Net 1.1 Runtime  --- altenatively ---  go over to:

http://www.microsoft.com/downloads/details.aspx?FamilyID=262d25e3-f589-4842-8157-034d1e7cf3a3&displaylang=en

- the executable is located in the distribution directory's 'bin' sub-directory.  Copy the executable (ical2rdf.exe) to somewhere in your path, or include the sub-directory in you PATH 

3.  CONTACT

J. Tim Spurway
tspurway@semaview.com

4. SHOUTS

This program is partially based on and inspired by the the ical2rdf.pl converter developed by Dan Connolly and Libby Miller (see http://www.w3.org/2002/12/cal/ for more info on the W3C working group responsible for the iCalendar/RDF schema development)


5. COPYRIGHT

/***
 * <copyright>
 *   ICalParser is a general purpose .Net parser for iCalendar format files (RFC 2445)
 * 
 *   Copyright (C) 2004  J. Tim Spurway
 *
 *   This program is free software; you can redistribute it and/or modify
 *   it under the terms of the GNU General Public License as published by
 *   the Free Software Foundation; either version 2 of the License, or
 *   (at your option) any later version.
 *
 *   This program is distributed in the hope that it will be useful,
 *   but WITHOUT ANY WARRANTY; without even the implied warranty of
 *   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 *   GNU General Public License for more details.
 *
 *   You should have received a copy of the GNU General Public License
 *   along with this program; if not, write to the Free Software
 *   Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.
 * </copyright>
 */


