# electron + react + express(router server) + icp
```
npm install  
npm start
```
# How to
electron main
```javascript
import RouteServer from '../RouteServer';
...
function createWindow() {
...
  mainWindow = new BrowserWindow({ width: 800, height: 600 });
  
  RouteServer.createRouteServer(port, mainWindow);
  
  RouteServer.getInstance().addEvent('eventName', (req): any => {
    return req.body;
  });
...
}
```
react app
```javascript
import { listenEvent } from '../RouteClient';
...
listenEvent('eventName', (args: any) => {
  console.log(args);
});
...
```
