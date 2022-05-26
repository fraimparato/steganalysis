# Appunti dei papers

## Steganographic attacks
    Al giorno d'oggi molti attacchi sfruttano metodi di steganografia per nascondere payloads all'interno di documenti all'apparenza innoqui.
    I malware possono essere inseriti quasi in ogni tipo di file:
        1. Text file --> Changing words or insering rndom characters in random points of the txt
        2. Image file -->  Least significant bit insertion, Masking and Filtering, Pattern encoding, Coding, and Cosine transformation methods.
        3. Audio file --> Il malware viene nascosto in un file WAV che contiene anche un loader per decifrarlo edeseguirlo
        4. Video file --> Simile all'image file attack ma le dimensioni del malware steganografato sono molto maggiori

## Steganographic int TCP/IP Networks
    Il campo esiste dal 1996 ma ha avuto il suo sviluppo dopo l'11 Settembre.

    --> TCP/IP (Transmission Control Protocol) protocol:
        E' il protocollo internet più diffuso per la comunicazione server-client. WWW, email, file transfer utilizzano questo protocollo per la comunicazione. Siccome si basa su un handshake tra server e client che stabiliscono una connessione sicura prima di comunicare, il protocollo è generalmente affidabile. Implementa anche alcune forme di error correction.
    
    --> UDP (User Datagram Protocol):
        E' il secondo protocollo di trasmissione dati più diffuso. Non necessita di una connessione ma semplicemente broadcasta all'infinito il messaggio. In questo caso il client è libero di leggerne il contenuto o di ignorarlo. Siccome non viene stabilita nessuna connessione tra server e client questo sistema è meno affidabile. L'header del messaggio è ridotto rispetto a TCP.


    --> IP:
        Il messaggio inviato attraverso l' Internet protocol è composto da due parti principali:
            1) Header: contiene IP_source, IP_destination, metadata per verificare la validità del messaggio e poi delle opzioni utili all'invio di tale messaggio
            2) Payload: contiene effettivamente i dati che vengono trasportati nel messaggio

    --> ICMP (Internet Control Message Protocol): 
        E' un protocollo di invio di messaggi di errore. Anche questo protocollo si presenta con un header che encapsula il messaggio

    Tutti i protocolli pre citatati contengono informazioni ridondanti nei loro header che possono essere modificate per inserire messaggi al loro interno. Se fatto male cambiare i metadati del messaggio potrebbe rendere il messaggio illeggibile.
    