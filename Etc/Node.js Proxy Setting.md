# Node.js 프록시 설정

1. **json 수정**
	```{javascript} 
	proxy:"proxy link"
	```
	
2. **http-proxy-middleware** (in React)
	terminal
	```
	npm install http-proxy-middle ware
	```
	script
	```{javascript}
	const { createProxyMiddleware } = require('http-proxy-middleware');
	
	module.exports = function(app) {
    		app.use(
    		'/api',
    		createProxyMiddleware({
      			target: 'http://localhost:5000',
      			changeOrigin: true,
    		})
    		);
	};
	```
	