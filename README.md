# onvif-client
ONVIF client in Python using zeep

Hello! I pushed this file to github so people can sse an example of using zeep to send ONVIF commands to cameras.
I had to download and edit the wsdl files - had to add the wsdl:service section at the bottom.  Since I'm using downloaded wsdl files also had to change the relative address at top of files for the schemaLocation.
I start by send a WS-Discovery probe to the camera to get the URI of the device service for the camera.  Yes, I know it's always ip_addr/onvif/device_service, but I think it sounds cool to say I sent a probe :)
I send a GetServices request to camera see all the services it supports, and I get the URI of the media service.
I send a GetProfiles request and let user choose a profile, and then send GetStreamUri to get the video URI of the selected profile
I wrote with Python 3.8
Put the wsdl files in working directory (usually same directory as the python file)
Please comment if you like it, and/or with any questions
