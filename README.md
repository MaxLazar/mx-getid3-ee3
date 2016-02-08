# MX GetID3#

**MX GetID3** is a PHP script that extracts useful information from MP3s & other multimedia file formats for  ExpressionEngine 

## Supported formats
* Tag formats:
* * ID3v1 (v1.0 & v1.1)
* * ID3v2 (v2.2, v2.3 & v2.4)
* * APE tags (v1 & v2)
* * (Ogg) VorbisComment
* * Lyrics3 (v1 & v2)
* * IDivX
* * Lossy Audio-only formats:
* * MP3, MP2, MP1 (MPEG-1, layer III/II/I audio, including Fraunhofer, Xing and LAME VBR/CBR headers)
* * Ogg Vorbis
* * Musepack (versions SV4-SV8)
* * AAC & MP4
* * AC-3
* * DTS
* * RealAudio
* * VQF
* * Speex
* * Digital Speech Standard (DSS)
* * Audible Audiobooks
* Lossless Audio-only formats:
* * WAV (including extended chunks such as BWF and CART)
* * AIFF
* * Monkey's Audio
* * FLAC & OggFLAC
* * LA (Lossless Audio)
* * OptimFROG
* * WavPack
* * TTA
* * LPAC (Lossless Predictive Audio Compressor)
* * Bonk
* * LiteWave
* * Shorten
* * RKAU
* * Apple Lossless Audio Codec
* * RealAudio Lossless
* * CD-audio (*.cda)
* * NeXT/Sun .au
* * Creative .voc
* * AVR (Audio Visual Research)
* * MIDI
* Audio-Video formats:
* * AVI
* * Matroska (WebM)
* * ASF (ASF, Windows Media Audio (WMA), Windows Media Video (WMV))
* * MPEG-1 & MPEG-2
* * Quicktime
* * RealVideo
* * NSV (Nullsoft Streaming Video)
* Graphic formats:
* * JPEG
* * PNG
* * GIF
* * BMP (Windows & OS/2)
* * TIFF
* * SWF (Flash)
* * PhotoCD
* Data formats:
* * ZIP
* * TAR
* * GZIP
* * ISO 9660 (CD-ROM image)
* * CUEsheets (.cue)
* * SZIP
* Metadata types:
* * EXIF (Exchangeable image file format)
* * IPTC
* * XMP (Adobe Extensible Metadata Platform)
* Formats identified, but not parsed:
* * PDF
* * RAR
* * MS Office (.doc, .xls, etc)

## Installation
* Download the latest version of MX GetID3 and extract the .zip to your desktop.
* Copy *mx_getid3* to */system/user/addons/*

## Configuration
Once the Plugin is installed, you should be able to see it listed in the Add-On Manager in your ExpressionEngine Control Panel. Is no needs in any control panel activation or configuration.

## Template Tags
{exp:mx_calc}

**JPEG:**

	{exp:mx_getid3 file='/IMG00018-20100929-1318.jpg'}
	{jpg}
	<p>Size: {height}x{width}</p>
	<p>Made by: {make} {model}</p>
	<p>Date: {datetime}</p>
	<p>Software: {software}</p>
	{/jpg}
	{/exp:mx_getid3} 
	
**JPEG Output:**

	Size: 1600x1200
	
	Made by: Research In Motion BlackBerry 9000
	
	Date: 2010:09:29 13:17:42
	
	Software: Rim Exif Version1.00a 


**MP3:**

	{exp:mx_getid3 file='Brain Rules-Part01.mp3'}
	    <p>File Name: {filename}</p>
	    <p>Length: {playtime_seconds}</p>
	    <p>Playtime: {playtime_string}</p>
	
		{id3v1}
			<p>Title: {title}</p>
			<p>Artist: {artist}</p>
			<p>Album: {album}</p>
			<p>Year: {year}</p>
			<p>Genre: {genre}</p>
		{/id3v1}
	{/exp:mx_getid3} 

**MP3 Output:**

	File Name: Brain Rules-Part01.mp3
	
	Length: 4534.67428571
	
	Playtime: 1:15:35
	
	Title: Brain Rules - Part 1
	
	Artist: John Medina
	
	Album: Brain Rules - 12 Principles fo
	
	Year:
	
	Genre: Other

### Parameters


*file*

Path to file (**full PATH!** not URL)

*refresh*

Refresh is the number of minutes between cache refreshes.

*debug*

Telling the true - description for all tags which you can use with getID3 library can take more time than writing this plugin. So , if you want to see available tags for target file, just add debug parameter to tag.

*debug = "on" *

**IMPORTANT**

Variables can be Single or Pairs.


## Support Policy
This is Communite Edition (CE) add-on.

## Contributing To MX GetID3 for ExpressionEngine 3

Your participation to MX GetID3 development is very welcome!

You may participate in the following ways:

* [Report issues](https://github.com/MaxLazar/mx-getid3-ee3/issues)
* Fix issues, develop features, write/polish documentation
Before you start, please adopt an existing issue (labelled with "ready for adoption") or start a new one to avoid duplicated efforts.
Please submit a merge request after you finish development.


### License

The MX GetID3 is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)