# Rojo Studio Plugin Change Log

## Current Master
* *No changes*

## 0.3.1
* Fixed minor bug with `.lua` appearing anywhere except the end of a file
* Added a detailed error message in the console if there's a protocol version mismatch between the dev plugin and server.
* Reduced polling interval from 300ms to 200ms -- this should be a safe change.
	* In the future, long polling is a much better idea, but Roblox's HTTP interface is limited.

## 0.3.0
* Factored out the plugin into a separate repository
* Fixed using a service as the target of a partition (part of #11)
	* There are still cases that will trigger errors, like putting an `init.lua` file inside of a service.
	* **Note that the contents of the service will be synced with the filesystem, so any existing items will be deleted!**