TRAINOVA

TRAINOVA è un'applicazione full stack per il fitness che genera schede di allenamento personalizzate, tiene traccia dei progressi e affianca l'utente con un coach virtuale basato su intelligenza artificiale.

Progetto realizzato da solo, dal backend al deploy online.

Demo live: (https://trainova-frontend.netlify.app/dashboard)
Repository frontend: (https://github.com/mohamedjaouad/trainova-frontend)
Repository backend:(https://github.com/mohamedjaouad/trainova-backend)

Funzionalità principali
Autenticazione JWT — registrazione e login sicuri, con validazione password (lunghezza minima, numero e carattere speciale obbligatori).
Generazione scheda personalizzata
Modalità template: algoritmo deterministico che seleziona gli esercizi in base a obiettivo, livello, giorni a settimana e attrezzatura disponibile.
Modalità AI: generazione tramite intelligenza artificiale, con fallback automatico al template se il servizio AI non risponde.
Coach virtuale — chat AI che risponde a domande su tecnica, recupero e programmazione, con fallback a risposte pre-scritte se l'AI non è disponibile.
Catalogo esercizi — oltre 100 esercizi organizzati per gruppo muscolare ed attrezzatura, con immagini gestite tramite Cloudinary.
Allenamento guidato
I giorni della scheda si sbloccano in ordine: una volta completato un giorno, non è più ripetibile fino alla settimana successiva.
L'allenamento in corso resta salvato anche cambiando pagina, con un indicatore fluttuante (timer live) che permette di riprenderlo in qualsiasi momento.
Dashboard
Statistiche: sessioni totali, volume sollevato, streak di giorni consecutivi.
Calendario mensile di costanza, navigabile mese per mese.
Grafico dell'attività settimanale.
Storico allenamenti — log completo delle sessioni salvate, con dettaglio di esercizi, serie, ripetizioni e carichi per ciascuna.
Sistema XP/livello — l'utente guadagna esperienza e sale di livello completando allenamenti.
Stack tecnico

Backend

Java, Spring Boot
Spring Security + JWT
Spring Data JPA / Hibernate
PostgreSQL
Cloudinary (gestione immagini)
Groq API (AI coach e generazione scheda)

Frontend

React + TypeScript
React Router
React Bootstrap
Chart.js

Deploy

Frontend: Netlify
Backend:  Render
Cosa mi ha insegnato questo progetto

Le scelte più difficili non sono state quelle di design, ma quelle che si vedono solo a progetto finito: cosa fare quando l'AI non risponde e serve un fallback,
perché un calcolo di date sballa di un giorno per colpa del fuso orario, o perché un import che funziona in locale rompe la build appena il filesystem diventa case-sensitive. 
Portare TRAINOVA fino alla pubblicazione mi ha insegnato più su queste cose che qualsiasi lezione teorica.
