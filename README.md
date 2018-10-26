Descrizione Role
=========

Trova il server LDAP master (o il primo server mirror in caso di configurazione MIRRORMODE) e modifica le applicazioni SIP controllando ed eventualmente aggiungendo l'exclude resource SIPSBC
Le applicazioni per cui viene fatta la modifica sono:

siprpchat
siprpin
siprpivr
siprpout
b2buavxml

Dopo aver fatto la modifica le applicazioni vengono riavviate

Requisiti
------------

La struttura LDAP del cliente deve essere corretta.Non ci devono essere errori in cui più macchine sono LDAP master.
E' ammessa la situazione in cui ci sono 2 server LDAP in mirror mode.

Per poter eseguire il modulo  ldap_attr (presente in questo role), sul server di destinazione deve essere presente il pacchetto rpm python_ldap (altrimenti a runtime otteniamo un errore).

Variabili
--------------

Nessuna

Dipendenze
------------

Nessuna

Esempio di chiamata
----------------

ansible-playbook /home/playbook/bugs/6571/main.yml

Informazioni Autore
------------------

Martino.Viganò
Martino.Vigano@enghouse.com
