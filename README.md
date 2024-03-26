# npm run prod > /dev/null 2>&1 &

This command runs the npm run prod command in the background and redirects all standard output (stdout) to /dev/null. The 2>&1 statement directs the standard error output (stderr) to standard output (stdout). So no output will appear in the terminal.

# lsof -i :4321

Show Applications Running on port 4231 , if we want more than one we can sepaarete them witg , for Example :   lsof -i :4321 , 5321
