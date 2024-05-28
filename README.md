# greyhack-secureSSH

encode.src на вашем сервере в каталоге /server.

Отредактируйте decode.src и поместите свой Encryption_key в строку 340, скомпилируйте decode.src в decode.bin на своем сервере в каталоге /server.

В каталоге /server/conf на вашем сервере вы найдете файл sshd.conf, откройте этот файл и установите для параметра encryption_enabled значение true.

Отредактируйте ssh.src и поместите другой Encryption_key из шага 2 в строке 417, скомпилируйте ssh.src в ssh на своем хост-компьютере в каталоге /bin (замените, если потребуется).

Отредактируйте AnonVPNsecure.src и поместите другой Encryption_key из шага 2 в строке 413, скомпилируйте AnonVPNsecure.src в AnonVPNsecure на своем хост-компьютере в каталоге /bin (не забудте добавить "[IP]":"[pass]" в 418 строке).

Чтобы добавить сервер в список серверов, просто введите «ssh add IP_OF_THE_SERVER Encryption_key_from_step_2 PORT_OF_THE_SERVICE».

Теперь вы можете подключиться к своему серверу, как обычно, через ssh или Map.exe или AnonVPNsecure.

original https://github.com/EntitySeaker/greyhack-SuperSecureShell