Liferay Connector
=================

This module, available for Node.js and Titanium SDK, wraps the Liferay JSON WS into an easier to use (and easier to test!) API.


Usage
-----

An example is worth thousands of words.

```js
var liferay = require('liferay-connector');

liferay.authenticate('http://localhost:8080', {
    login: '??',
    password: '??'
}, function (err, session) {
  session.invoke({
  	"/group/get-user-sites": {}
  }, function (err, sites) {
  	console.dir(sites);
  });
});
```


Credits
-------

Humbly made the spry ladies and gents at SMC.


License
-------

This library, *liferay-connector*, is free software ("Licensed Software"); you can
redistribute it and/or modify it under the terms of the [GNU Lesser General
Public License](http://www.gnu.org/licenses/lgpl-2.1.html) as published by the
Free Software Foundation; either version 2.1 of the License, or (at your
option) any later version.

This library is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; including but not limited to, the implied warranty of MERCHANTABILITY,
NONINFRINGEMENT, or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Lesser General
Public License for more details.

You should have received a copy of the [GNU Lesser General Public
License](http://www.gnu.org/licenses/lgpl-2.1.html) along with this library; if
not, write to the Free Software Foundation, Inc., 51 Franklin Street, Fifth
Floor, Boston, MA 02110-1301 USA