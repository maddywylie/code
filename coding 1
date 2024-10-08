const http = require('http');
const url = require('url')

// here the server created
const server = http.createServer((req, res) => {
   // Set the response headers
   const parseUrl = url.parse(req.url, true);
   const queryParams = parseUrl.query;


   res.writeHead(200, { 'Content-Type': 'text/html' });

    if (Object.keys(queryParams).length > 0){
       res.write('<h1> I got what you send bro : </h1>')
       res.write('<ul>')
       for (const param in queryParams){
           res.write(`<l1>${param} : ${queryParams[param]}</l1>`)
       }
       res.write('</ul>');
      
      
    }else{
       res.write('<h1>Hi just normal like before</h1>');
    }

    res.end();

});

// Specify the port to listen on
const port = 3000;

// server will begin listening after this command
server.listen(port, () => {
   console.log(`Node.js HTTP server is running on port ${port}`);
});
