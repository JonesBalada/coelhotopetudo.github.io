---
layout: post
---

#!/usr/bin/env node
// var sys = require('sys');
var exec = require('child_process').exec;
var child;
var comando = 'mocha --reporter spec --compilers coffee:coffee-script/register';

// executes `pwd`
child = exec(
  'cd /home/00737990929/git/gitlab.com/coisarada/identificador && ' 
  + comando, function (error, stdout, stderr) 
  {
    console.log(stdout);
  }
);

  process.stdin.resume();
  process.stdin.setEncoding('utf8');
  process.stdin.on('data', function (text) {
    process.exit();
  });
