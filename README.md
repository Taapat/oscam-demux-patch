OSCam demux for reader patch
=========

This patch is for oscam from streamboard, to allow set used demux number for reader.

You can in file oscam.server, in reader add option use_for_demux to set demux number for which use this reader.

I use this to watch the picture in picture.
When used pip, for the channel in small screen is used demux0, but for channel in the main screen is used demux1.

Specifying for the all main readers use_for_demux = 0, and for the all backup readers use_for_demux = 1, allow use main readers when watching channel in the main screen, and backup readers only for additional pip channel when use pip.

Example:
=========

	[reader]
	label                         = main
	protocol                      = cs378x
	use_for_demux                 = 0
	device                        = xx,xx
	user                          = xx
	password                      = xx

	[reader]
	label                         = main_fallback
	protocol                      = cs378x
	use_for_demux                 = 0
	device                        = xx,xx
	user                          = xx
	password                      = xx
	fallback                      = 1

	[reader]
	label                         = backup
	protocol                      = cs378x
	use_for_demux                 = 1
	device                        = xx,xx
	user                          = xx
	password                      = xx

