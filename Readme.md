Note: you must have deno install locally, to check if it is installed, run 'deno upgrade' or you can install using this command line for window user, remember to use powershell or gitbash to install locally run 'irm https://deno.land/install.ps1 | iex' for mac/linux users run 'curl -fsSL https://deno.land/install.sh | sh'
after successful installation run 'deno upgrade' to confirm your installation, the response expected is the version 
for local users go to https://marketplace.visualstudio.com/items?itemName=denoland.vscode-deno and install this vscode extension
run:  'deno install' ,after installing that extension
run: 'deno run generateToken.ts'
copy the api key into .env
jump to step 6 and install the vscode extension there too
run: 'deno test -A'
delete pets.db and rename pets-mock.db to pets.db (mock/database)
run: 'deno task serve' and open postman
http://127.0.0.1:5555

continue from step 6, watch the video and you may need the one below in postman
post request
http://127.0.0.1:5555/auth/admin/register
http://127.0.0.1:5555/auth/admin/login
after logging in copy bearer token to the token in the header
{
    "firstName": "",
    "lastName": "Stackie",
    "email": "",
    "password": "verysecurepassword"
}

put request
http://127.0.0.1:5555/api/animals/id
{
"owner": "stackup username"
}


for delete request
http://127.0.0.1:5555/api/people/id