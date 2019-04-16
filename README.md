# Tetris
Tetris game written in HTML5 + CSS3 + jQuery. This WebApp is a "Responsive Web Design" (RWD) website. 

Cloned to DockeriZe and run in DC/OS from:
<a href="https://tetris-90067.firebaseapp.com">Play game</a>

##Build Docker image:
docker build -t tetris-web:1.0 .
docker tag tetris-web:1.0 grahamh/tetris-web:1.0
docker push grahamh/tetris-web:1.0

##Test:
docker run --rm -d -p 8080:80 grahamh/tetris-web:1.0 

##Deploy to DC/OS using dcos cli:
dcos marathon app add tetrisweb.json
dcos marathon app show tetrisweb
