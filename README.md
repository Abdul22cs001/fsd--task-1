Program:
const http = require('http');

const server = http.createServer((req, res) => {
    res.setHeader('Content-Type', 'text/plain');

    if (req.url === '/home') {
        res.statusCode = 200;
        res.end('Welcome to the Home Page!');
    } else if (req.url === '/about') {
        res.statusCode = 200;
        res.end('Learn more About Us on this page.');
    } else if (req.url === '/contact') {
        res.statusCode = 200;
        res.end('Contact us through this page.');
    } else {
        res.statusCode = 404;
        res.end('Page Not Found');
    }
});
const PORT = 3001;
server.listen(PORT, () => {
    console.log(`Server is running on http://localhost:${PORT}`);
});
