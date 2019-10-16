# Deprecated/Archived Library

This library is no longer going to be used, since the official Arduino library has been updated and works great https://github.com/arduino-libraries/Ethernet

# Additional Notes

Since nothing has changed since 2016 with possibility of handling multiple connections from the same client, we have applied patch proposed and discussed here https://subethasoftware.com/2013/04/08/arduino-ethernet-and-multiple-socket-server-connections/

It resolves problem when connection is considered active while in reality physical layer has been damaged (cable has been removed, or cut). In that case server has no clue that client is no longer valid and in the same time server is not accepting new connections. Even if we start to listening for new connections, request from the same IP is considered as one that belongs to the previous session, so nothing really happens. Moreover we cannot disconnect each time new request happens as we could accidentally disconnect in the middle of connection procedure.

License
-------

Copyright (c) 2009-2016 Arduino LLC. All right reserved.

This library is free software; you can redistribute it and/or
modify it under the terms of the GNU Lesser General Public
License as published by the Free Software Foundation; either
version 2.1 of the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public
License along with this library; if not, write to the Free Software
Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301 USA


[W5100]:                   http://www.wiznet.co.kr/product-item/w5100/
[W5500]:                   http://www.wiznet.co.kr/product-item/w5500/
