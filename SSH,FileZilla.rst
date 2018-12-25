SSH,Tmux,FILEZILLA
=============
SSH

Tmux
::
    how ....pogledamo katere seje tečejo
    tmux new -s django ..........odpremo v osnovnemu terminalu okno z imenom django
    tmux attach -t django .......vstopimo iz osnovnega ali drugega terminala na delujoco sejo
    tmux rename-session -t 0 django .........lahko preimenujemo sejo 0 v django
    tmux ls ..........pogledamo vse seje
    exit .......izhod iz tmuxa, ki ni aktiven sicer pa samo zapremo okno in on dela
    tmux kill-server ..... odstrani vse seje
    tmux kill-session

    s ctrl-b istocasno in sprostimo,  vklopimo hitro komando % , da razdeli na dva dela ali pa " na dva dela po vertikali
    s ctrl-b istocasno in potem s pušcico prehajamo med okni


::
   sudo su
   apt-get update
   apt-get upgrade
   apt-get install openssh-server
