# ohmyposh
windows ohmyposh themes
INSTRUCCIONES DE USO
1. Instalar windows terminal desde el store
https://www.microsoft.com/es-mx/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab

2. Instalar Meslo Nerd Font
https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/Meslo.zip

3. Editar el archivo .json en confirugracion de windows terminal y adicionar estas lineas:
<code>
{
    "commandline": "powershell.exe",
    "font": 
    {
        "face": "MesloLGL Nerd Font"
    },
    "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
    "hidden": false,
    "name": "Windows PowerShell"
    },
</code>

4. Activar la politica de ejecucion de scripts en la maquina

<code>
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
</code>
	nota. Desactivarla.
	Set-ExecutionPolicy -ExecutionPolicy Undefined -Scope LocalMachine

5. Instalar oh-myposh:
<code>
curl https://github.com/CarminaMatrix/ohmyposh.git
</code>

6. obtener Temas
Get-PoshThemes

7. Activar y Cambiar temas
notepad $PROFILE

8. Agregar al archivo:
oh-my-posh --init --shell pwsh --config "C:\Users\bufet\Documents\WindowsPowerShell\Modules\oh-my-posh\themes\powerlevel10k_classic.omp.json" | Invoke-Expression
***guardar
-- Cambiar tema provisionalmente
Set-PoshPrompt -Theme nombre_plantilla
ejemplo
Set-PoshPrompt -Theme powerlevel10k_classic
nota. Para cambiar definitivamente el tema, se necesita cambiar el nombre del tema en $PROFILE
