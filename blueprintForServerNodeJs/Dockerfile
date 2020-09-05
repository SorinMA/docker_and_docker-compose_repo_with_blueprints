# alegem (base img) imaginea pe care vrem sa o folosim
# in functie de ce vrem sa rulam in container
FROM node:alpine 

# e bine sa setam un workdir
# pentru ca nu vrem sa suprascriem
# ceva din filesystemul imaginii de baza
WORKDIR /numeNodeApp

# copiem mai intai fisierul cu dependecy uri 
# pentru a evita buildurile nenecesare
COPY ./package.json . 

# instala dependecy urile
RUN npm install

# copiem tot codul
COPY . .

# setam comanda de startup pentru container
# npm run start pentru ca acest container
# va fi folosit pentru production mod
CMD ["npm", "run", "start"]
