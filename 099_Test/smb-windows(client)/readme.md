windows-smb container image script.ps1 running

New-SmbMapping -LocalPath 'Z:' -RemotePath '{{ Server Address }}' -UserName '{{ DomainName }}\{{ UserName }}' -Password '{{ Password }}' -Persistent $True