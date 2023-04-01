# wd-bitcoincore-rpc
Client JSON-RPC pour Bitcoin Core en WINDEV

Crée un composant WINDEV qui permet d'acceder aux API JSON RPC d'un noeud bitctoin


# Prérequis

- Bitoin core doit être lancée sur la même machine **ou** un tunnel VPN vers la machine doit exister
- la gestion du RPC doit être activée pour Bitcoin core. Il suffitt de mettre les paramètres suivant dans le fichier bitcoin.conf 
```
# Connexion RPC
server=1
rpcuser=<NOM RPC>
rpcpassword=<MOT DE PASSE RRC>
rpcport=8332
rpcallowip=127.0.0.1
```


# Utilisation

Compiler le composant et l'intégrer dans un projet.

Exemple de code :
```javascript
bitcoin_core_rpc est un NoeudBitcoin(SAI_login, SAI_MotDePasse)
taille_blockchain est entier
taille_blockchain =  bitcoin_core_rpc.getblockcount() 
SI  ErreurDétectée ALORS
	Erreur()
	RETOUR
FIN
Info("Taille de la blockchain : [%taille_blockchain%] blocks" )
```
