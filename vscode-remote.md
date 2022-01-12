# Using VSCode Remote

Steps on how to use VSCode Remote to connect to a droplet for development.

## Steps

1. Install VSCode
2. Check the [supported ssh client](https://code.visualstudio.com/docs/remote/troubleshooting#_installing-a-supported-ssh-client)
and take what steps are necessary to install the needed ssh client.
3. Install the Remote Development extension pack by Microsoft ([marketplace link](https://code.visualstudio.com/docs/remote/troubleshooting#_installing-a-supported-ssh-client))
4. Verify you can connect to the remote host by connecting [via ssh](https://docs.digitalocean.com/products/droplets/how-to/connect-with-ssh/) in your terminal
5. In VS Code, use the command palette and execute "Remote-SSH: Connect to Host..."

   The command palette can be opened with `CONTROL/CMD` + `SHIFT` + `P` or `F1`
  
 6. Use the same `<user>@<host-ip-address>` you used in step 4
 7. Select Linux if prompted for type of OS
 8. Boom you're connected and developing on the remote server

## Sources

- [Remote Development using SSH (from vscode docs)](https://code.visualstudio.com/docs/remote/ssh)
