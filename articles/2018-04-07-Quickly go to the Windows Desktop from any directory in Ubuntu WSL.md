## Quickly go to the Windows Desktop from any directory in Ubuntu WSL

### References:

  1. https://stackoverflow.com/questions/255414/why-doesnt-cd-work-in-a-bash-shell-script
  
  2. https://askubuntu.com/questions/582452/location-of-bash-aliases
  
### Procedures:

  1. shell script is ran inside a subshell, so "cd" command won't work directly inside shell script
  
  2. the better way is to make a commad/alias:
  
      - go to root directory in Ubuntu WSL
    
      - create a new file named ".bash_aliases"
    
        *Note:* as is documented in the original .bashrc, they don't recommend adding aliases directly to .bashrc
    
      - put the following line in ".bash_aliases"
    
        ```console
          alias Desktop="cd /mnt/c/Users/Yuchen/Desktop"
        ```
      - save the file, and type the following in the root directory:
    
        ```console
          source ~/.bashrc
        ```
  3. Now we can just type "Desktop" and change directory to the windows desktop instantly.
