# i3blocks_powerlines
Configurações do i3blocks com inúmeras funções de uso interno do arch linux.


# Instalaçao

    Se voçe esta usando Arch linux + i3wm, e quer usar essas configuraçoes do i3blocks
voçe deve seguir os seguintes passos.

# Passo 0

-- Clonagem

    Clone o repositorio na sua home
    copie o arquivo "i3blocks.conf" para .config/i3

# Passo 1

-- Instalação do i3blocks
	$ sudo pacman -S i3blocks	(Instala o i3blocks)
	$ sudo pacman -S ttf-font-awesome otf-font-awesome powerline powerline-fonts	(Instala as fontes)
	$ sudo pacman -S pacman-contrib		(Instala o pacote usado para checar as atualizações)

# Passo 2

-- Configurações
    Para que essas configuraçoes funcionem de forma correta no seu sistema, voçe de realizar alguns passos simples.

Com o editor de texto de sua escolha edite o arquivo "config" que devera estar dentro de ~/.config/i3.
No fim do arquivo adicione as seguintes linhas.

#==========================================================================

bar {
         position top
         font pango:FontAwesome -10 11
         #font pango:Ubuntu Mono derivative Powerline Bold-12 10
         status_command i3blocks -c ~/.config/i3/i3blocks.conf
   colors {
     separator #000000
     background #282c34
     statusline #ff0000
     focused_workspace #1c1c1c #BF4040 #fdf6e3
     active_workspace #1c1c1c #1c1c1c #000000
     inactive_workspace #002b36 #586e75 #002b36
     urgent_workspace #d33682 #d33682 #fdf6e3
   }
 }

#===========================================================================

Estas linhas sao responssaveis pela aparencia e parte do comportamento do i3blocks.

Por fim basta restartar seu i3 e se tudo foi feito de forma correta ele estara funcionando corretamente
