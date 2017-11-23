# electron-react-express-icp
```
npm install  
npm start
```
# How to
```javascript
import RouteServer from '../RouteServer';
....
function createWindow() {
....
  mainWindow = new BrowserWindow({ width: 800, height: 600 });
  
  RouteServer.createRouteServer(port, mainWindow);
  
  RouteServer.getInstance().addEvent(GET_LOG, (req): any => {
    return req.body;
  });
....
}
