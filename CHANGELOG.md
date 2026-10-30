# Changelog

Tutte le modifiche rilevanti a questo plugin sono documentate in questo file.

Il formato è basato su [Keep a Changelog](https://keepachangelog.com/it/1.1.0/)
e questo progetto aderisce al [Semantic Versioning](https://semver.org/lang/it/).

## [1.0.0] - 2026-10-27

### Added
- Negozi gestiti dall'admin di WordPress (custom post type `wo_sl_store`): nome, attivo, ordinamento, descrizione,
  indirizzo, paese, latitudine/longitudine, due telefoni, email, sito, Facebook, X/Twitter e orari per ogni giorno.
  Colonne in elenco e azioni di gruppo attiva/disattiva.
- Shortcode `[tc_store_locator]` e pagina creata all'attivazione. Elenco renderizzato dal server, mappa caricata solo
  quando entra nello schermo, ricerca per città, CAP o nome che filtra elenco e mappa, "Vicino a me" (geolocalizzazione
  del browser, distanza in formula dell'emisenoverso), fumetto con "Indicazioni stradali".
- Mappa a scelta: **OpenStreetMap** (default, Leaflet 1.9.4 incluso nel plugin, nessuna chiave né CDN) oppure
  **Google Maps** (chiave API e Map ID, Advanced Marker con Map ID). Con Google senza chiave resta l'elenco.
- Pannello *Store Locator → Impostazioni*: attiva, titolo pagina, provider, chiave e Map ID (solo con Google), zoom
  1-20, contenuto prima/dopo, meta title/description/keywords, eliminazione dei dati alla disinstallazione.
- API pubblica per altri plugin: `Threecommerce\StoreLocator\Stores`, `MapConfig`, filtro `wo_sl_store_fields`
  (campi aggiuntivi nella scheda negozio, nelle colonne e nel salvataggio) e azione `wo_sl_loaded`.
- Traduzione italiana. Porting per WordPress del modulo Magento `threecommerce/m2-storelocator` 1.2.0.
