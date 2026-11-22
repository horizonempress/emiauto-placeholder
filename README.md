# emiauto.lv pagaidu lapa

Statiska lapa bez ārējiem skriptiem, ko rādīt, kamēr vecā lapa ir noņemta no Devera servera.

## Publicēšana ar GitHub Pages

1. Izveido jaunu publisku GitHub repo, piemēram `emiauto-placeholder`, un ieliec tajā šīs mapes saturu (`index.html`, `404.html`, `CNAME`).
2. Repo iestatījumos: Settings → Pages → Source: "Deploy from a branch", Branch: `main`, folder `/ (root)`.
3. Turpat Custom domain: `emiauto.lv` (CNAME fails to jau satur). Kad DNS pārbaude izdodas un sertifikāts izdots, ieslēdz "Enforce HTTPS".

## nic.lv DNS ieraksti

Aizstāj esošo A ierakstu `emiauto.lv → 89.111.20.230` ar četriem A ierakstiem uz GitHub Pages:

    emiauto.lv  A  185.199.108.153
    emiauto.lv  A  185.199.109.153
    emiauto.lv  A  185.199.110.153
    emiauto.lv  A  185.199.111.153

Neaiztikt: MX `smtp.google.com` (e-pasts), CNAME `www.emiauto.lv → emiauto.lv`.

`404.html` ir tā pati lapa, lai vecās preču saites arī rāda kontaktus.

## LIAA publicitāte

Lapas apakšā ir Atveseļošanas fonda teksts no vecās lapas kājenes un logo ansamblis "Finansē Eiropas Savienība NextGenerationEU un Nacionālās attīstības plāns". Logo ir iebūvēts pašā HTML failā, tāpēc neviens cits fails nav vajadzīgs.

`emiauto-pagaidu-lapa.html`, `index.html` un `404.html` ir viens un tas pats fails. Uz jebkura cita hostinga pietiek augšupielādēt `index.html`.
