![NearbyLogo](https://www.nearbycommunity.it/wp-content/uploads/2024/10/splash1024500-e1736371921651.png)

<br>

Questa repository contiene una guida completa per integrare facilmente una mappa da **[Nearby](https://www.nearbycommunity.it)** all'interno delle tue applicazioni o dei siti web **gratuitamente**.

La documentazione include esempi pratici, istruzioni dettagliate per l'implementazione, e configurazioni personalizzabili per visualizzare posizioni, Punti di Interesse e dati geospaziali.

Perfetto per sviluppatori che desiderano migliorare l'esperienza utente con funzionalità di geolocalizzazione intuitive tramite Nearby ma utilizzabile da chiunque, con pochissima configurazione.

<br>

![NearbyMapPreview](https://www.nearbycommunity.it/wp-content/uploads/2025/01/map_placeholder.png)

<br>

> [!IMPORTANT]
> **Questo iFrame non registra Cookies e non profila il traffico, i dati temporanei relativi al suo utilizzo che vengono immagazzinati nei server sotto forma di cache vengono normalmente eliminati dopo 12 ore, per maggiori informazioni vista il sito [NearbyCommunity](https://www.nearbycommunity.it) oppure leggi i termini e le condizioni [qui](https://www.nearbycommunity.it/eula)** <br>

<br>
<br>
<br>

_____________________________________

<br>
<br>
<br>

# Incorporazione della mappa in una pagina

Per integrare correttamente la mappa in una pagina è necessario incorporare questo iframe nel modo seguente:

1. **Copiare ed incollare questo codice:**

```html
	<iframe
		src="https://include.nearbycommunity.it/"
  		allow="geolocation"
	></iframe>
```

> [!IMPORTANT]
> i permessi per la geolocalizzazione sono necessari quindi assicurarsi sempre che `allow="geolocation"` sia presente, in caso contrario potrebbero verificarsi errori o malfunzionamenti <br>

2. **Incollare nella pagina web**

3. **Modificare i parametri di stile:**

```html
	<iframe
		src="https://include.nearbycommunity.it/"
  		allow="geolocation"
		width="100%"
		height="500pt"
		style="border:none;"
	></iframe>
```

> [!NOTE]
> in width e in height è possibile utilizzare i parametri nelle unità di misura standard come px e pt o in percentuale <br>
> in style è possibile utilizzare proprietà standard css <br>
> è preferibile inserire l'`iframe` all'interno di un `div`, settare *width* e *height* dell'`iframe` al *100%* e di conseguenza usare lo styling nel `div` genitore <br>

<br>
<br>
<br>

_____________________________________

<br>
<br>
<br>

# URL personalizzati e parametri

Nell'url di *src* nell'*iframe* è possibile inserire vari parametri, vediamo come:

| Parametro               | Richiesto | Utilizzo                                                           | Default                       |
| ----------------------- | --------- | ------------------------------------------------------------------ | ----------------------------- |
| `map_center`            |           | Le coordinate di partenza della mappa                              | Posizione attuale dell'utente |
| `map_zoom`              |           | Lo zoom della mappa                                                | `18`                          |
| `display_user_position` |           | Visualizza la posizione dell'utente nella mappa                    | `true`                        |
| `locale`                |           | Linguaggio e paese di destinazione                                 | `it_it`                       |
| `target`                | `params`  | Che tipo di elementi devono essere visualizzati nella mappa        | `all`                         |
| `params`                | `target`  | Quali elementi devono essere visualizzati nella mappa              |                               |
| `from`                  |           | Esclusivamente contenuti di un singolo utente                      |                               |

La sintassi corretta per l'inserimento dei parametri è la seguente:

```
	https://include.nearbycommunity.it/
	https://include.nearbycommunity.it/?parametro1=valore1
	https://include.nearbycommunity.it/?parametro1=valore1&parametro2=valore2
	https://include.nearbycommunity.it/?parametro1=valore1&parametro2=valore2&parametro3=valore3
```

<br>

## Parametro `map_center`

il parametro `map_center` dichiara la posizione iniziale del centro della mappa segue ed il tipo è `LngLat`

#### Default

> map_center = **posizione dell'utente** <br>

#### Esempio

se latitudine è `39.523` e logitudine è `8.671`, il valore del del parametro `map_center` sarà `8.671,39.523`

```
	https://include.nearbycommunity.it/?map_center=8.671,39.523
```

> [!CAUTION]
> utilizzare i valori numerici decimali con il punto (`.`) e non con la virgola (`,`), in quanto la virgola funge solo ed esclusivamente da separatore <br>
> Corretto: `39.523` <br>
> Errato: `39,523` <br>

<br>

## Parametro `map_zoom`

il parametro `map_zoom` dichiara lo zoom iniziale del centro della mappa, il valore è di tipo `number`

#### Default

> map_zoom = **18** <br>

#### Esempio

```
	https://include.nearbycommunity.it/?map_zoom=18
```

<br>

## Parametro `display_user_position`

il parametro `display_user_position` segue il modello Boolean, con i soli tipi `true` e `false`

#### Default

> display_user_position = **false** <br>

#### Esempio

```
	https://include.nearbycommunity.it/?display_user_position=true
```

<br>

## Parametro `locale`

il parametro `locale` determina la lingua utilizzata

| Valori Accettati | Corrispondenza |
| ---------------- | -------------- |
| `it_it`          | Italiano       |
| `en_en`          | Inglese        |
| `fr_fr`          | Francese       |
| `es_es`          | Spagnolo       |
| `de_de`          | Tedesco        |

#### Default

> locale = **it_it** <br>

#### Esempio

```
	https://include.nearbycommunity.it/?locale=it_it
```

<br>

## Parametro `target` e Parametro `params`

Il parametro `target` indica che tipo di elementi devono essere visualizzati nella mappa mentre il parametro `params` fornisce le indicazioni sugli elementi specifici da visualizzare

| Target Accettati   | Corrispondenza                   | Parametri Accettati
| ------------------ | -------------------------------- | --------------------------------
| `poi`              | Punti di Interesse               | `id` di uno o più Punti di Interesse
| `poi_categories`   | Categorie dei Punti di Interesse | `id` o `slug` di una o più categorie di Punti di Interesse
| `events`           | Eventi                           | `id` di uno o più Punti di Interesse
| `event_categories` | Categorie degli Eventi           | `id` o `slug` di una o più categorie di Eventi

> [!IMPORTANT]
> **Il parametro `target` va sempre accompagnato da `params`**, in caso contrario produrrà un errore
> `target` accetta un singolo valore <br>
> `params` accetta più valori ed in questo caso, essi vanno separati da una virgola (`,`) <br>

#### Default

> target = **all** <br>
> map_zoom = **undefined** <br>

#### Esempio

```
	https://include.nearbycommunity.it/?target=esempio_target_singolo&param=esempio_param1
	https://include.nearbycommunity.it/?target=esempio_target_multipli&param=esempio_param1,esempio_param2
```

<br>
<br>
<br>

_____________________________________

<br>
<br>
<br>

# Copyright

**© Copyright 2022 - 2024 by [PRYSM](https://www.prysmlab.com) & [Rikozz](https://www.rikozz.me)**

"Nearby" e "Nearby Community" sono dei marchi registrati di proprietà esclusiva di [PRYSM](https://www.prysmlab.com) - Ogni riproduzione anche parziale non autorizzata è vietata
