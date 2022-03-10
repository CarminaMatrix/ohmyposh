# ohmyposh
windows ohmyposh themes
INSTRUCCIONES DE USO
1. Instalar windows terminal desde el store
https://www.microsoft.com/es-mx/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab

2. Instalar Meslo Nerd Font
https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/Meslo.zip

3. Ediatr el archivo .json en confirugracion de windows terminal y adicionar estas lineas
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

4. Acivar la politica de ejecucion de scripts en la maquina
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

	nota. Desactivarla.
	Set-ExecutionPolicy -ExecutionPolicy Undefined -Scope LocalMachine

5. Instalar oh-myposh
curl 

6. obtener Temas
Get-PoshThemes

7. Activar y Cambiar temas
notepad $PROFILE

agregar:
oh-my-posh --init --shell pwsh --config "C:\Users\bufet\Documents\WindowsPowerShell\Modules\oh-my-posh\themes\powerlevel10k_classic.omp.json" | Invoke-Expression
***guardar
-- Cambiar tema provisionalmente
Set-PoshPrompt -Theme nombre_plantilla
ejemplo
Set-PoshPrompt -Theme powerlevel10k_classic
nota. Para cambiar definitivamente el tema, se necesita cambiar el nombre del tema en $PROFILE
