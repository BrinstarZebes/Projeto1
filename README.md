# Projeto1
servidor local com mensagem Hello Word por Node js. 


var http = require('http'); //chamando http com modulo require, recurso do node
var fs = require('fs'); // usando file sistem para ler arquivos http locais

var server = http.createServer(function(request, response) {
  response.writeHead(200, {'Contente-type': 'text/html; charset=utf-8' }); //cabeçalho passando readers por objetos, com string Content-type, usando utf-8 pra não ter problemas com acentuação
   response.write('<h1>Hello World!</h1>'); //corpo com mensagem que quero mostrar no servidor
   response.end();// informando que acabei
});

server.listen(3000); //servidor "escutará" porta 3000
