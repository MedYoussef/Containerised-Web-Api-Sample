commandes Docker :

1- docker build -t counter-image -f Dockerfile . (counter-image : nom de l'image docker)

2- docker images (pour identifier l'image docker qui a été créé : counter-image, IMAGE ID : 85e0e82dad76)

3- Créer un conteneur basé sur l'image "counter-image"

   docker create --name container counter-image
   Container id : a57b392a5b550c01494f637d3d4dc07d1e4a051c5c0a1fae329bc9014c331575

4- Lister les conteneur disponibles : docker ps -a

5- démarrer un conteneur : docker start container (container : nom du conteneur)

6- docker run -it --rm -p 5001:80 --name test counter-image

7- exécuter la web api : http://localhost:5001/weatherforecast