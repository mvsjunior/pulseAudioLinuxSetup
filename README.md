# pulseAudioLinuxSetup

Configurações para melhorar a qualidade do som no linux (pulse audio).

Debian 11
Pulseaudio 14.2

1 - Faça backup do conteúdo em: ~/.config/pulse/daemon.conf
cp `~/.config/pulse/daemon.conf` `~/.config/pulse/daemon.conf.bkp`

2 - Apague tudo o que estiver dentro do arquivo `~/.config/pulse/daemon.conf` e cole o seguinte conteúdo:

` default-sample-format = s24le
default-sample-rate = 96000
alternate-sample-rate = 44100
default-sample-channels = 2
default-channel-map = front-left,front-right

default-fragments = 2
default-fragment-size-msec = 125
resample-method = speex-float-5
remixing-produce-lfe = no
remixing-consume-lfe = no
high-priority = yes
nice-level = -11
realtime-scheduling = yes
realtime-priority = 9
rlimit-rtprio = 9
rlimit-rttime = -1
daemonize = no `

3 - Reinicie o pulse-audio:
`pulseaudio -k`
`pulseaudio --start`


Crédito: 
    Usuário: jazzman079 ~ https://plus.diolinux.com.br/u/jazzman079 do fórum Diolinux Plus.
    Tópico: https://plus.diolinux.com.br/t/problemas-com-audio-no-ubuntu-18-04-lts/464/3


  
  
