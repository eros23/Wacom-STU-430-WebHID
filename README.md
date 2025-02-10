# Firma e Salva - Wacom STU‑430

Questo progetto utilizza una tavoletta grafometrica Wacom STU‑430 per catturare una firma digitale e salvarla come immagine PNG. 
**Nota:** La firma digitale generata con questo strumento **non ha valenza legale**; viene usata esclusivamente per produrre una grafica in formato PNG della firma.

## Cosa Fa

- **Connetti la Tavoletta:**  
  Cliccando sul pulsante **Connect** il sistema si collega alla tavoletta, cancella eventuali firme precedenti e imposta l'area di scrittura per ricevere i dati della penna.

- **Firma Digitalmente:**  
  Quando scrivi con il pennino sulla tavoletta, il disegno viene automaticamente riportato su un'area del browser (canvas) di 320×200 pixel.

- **Cancella la Firma:**  
  Il pulsante **Clear** elimina la firma sia dal canvas del browser che dalla tavoletta.

- **Salva la Firma:**  
  Cliccando su **Save Signature** la firma viene salvata come file PNG con sfondo trasparente, pronta per essere utilizzata in altri documenti o applicazioni.

## Come Usarlo

1. **Apri la Pagina Web:**  
   Assicurati di aprire la pagina tramite un server sicuro (HTTPS o localhost) per garantire il corretto funzionamento delle API WebHID.

2. **Collega la Tavoletta:**  
   Collega la Wacom STU‑430 al computer.

3. **Clicca "Connect":**  
   Premi il pulsante **Connect** per connetterti alla tavoletta. Il sistema cancellerà automaticamente eventuali firme precedenti e imposterà l'area di scrittura.

4. **Firma:**  
   Firma sulla tavoletta; il disegno apparirà sul browser nell'area di 320×200 pixel.

5. **Clear:**  
   Se vuoi cancellare la firma, premi **Clear** per pulire sia il canvas del browser che lo schermo della tavoletta.

6. **Save Signature:**  
   Premi **Save Signature** per salvare la tua firma come file PNG con sfondo trasparente.

## Requisiti

- **Browser Compatibile:**  
  Utilizza un browser che supporti WebHID (ad esempio, Google Chrome).

- **Connessione Sicura:**  
  La pagina deve essere servita tramite HTTPS o localhost.

- **Dispositivo:**  
  È necessaria la tavoletta digitale Wacom STU‑430.

## Note Tecniche

- **Mapping delle Coordinate:**  
  I dati grezzi provenienti dalla tavoletta (X da 0 a 9600 e Y da 0 a 6000) vengono convertiti per adattarsi all'area di 320×200 pixel del canvas.

- **Sensibilità della Firma:**  
  È stata impostata una soglia di pressione (35) per rendere la firma più reattiva. Tale valore può essere modificato nel codice se necessario.

- **Sfondo Trasparente:**  
  L'immagine PNG salvata ha uno sfondo trasparente. Il background bianco visibile nell'interfaccia è applicato solo tramite CSS e non viene incluso nell'immagine.

