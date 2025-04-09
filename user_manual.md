# CYD Termosztát v4.0 Felhasználói Kézikönyv

Üdvözöljük a CYD Termosztát v4.0 használati útmutatójában! Ez az útmutató segít megérteni és hatékonyan használni a termosztátot.

---

## Tartalomjegyzék
1. [Bevezetés](#bevezetés)
2. [Funkciók](#funkciók)
3. [Első lépések](#első-lépések)
4. [Webes felület](#webes-felület)
5. [TFT kijelző](#tft-kijelző)
6. [Programozott ütemezések](#programozott-ütemezések)
7. [HTML Felület és Érintőképernyő Használata](#html-felület-és-érintőképernyő-használata)
8. [Hibaelhárítás](#hibaelhárítás)
9. [Műszaki adatok](#műszaki-adatok)

---

## Bevezetés

A CYD Termosztát v4.0 egy intelligens termosztát, amely pontos hőmérséklet-szabályozást biztosít otthonában. Webes felülettel, érintőképernyővel és fejlett ütemezési lehetőségekkel rendelkezik.

---

## Funkciók

- **Webes felület**: Felhasználóbarát webes felületen keresztül konfigurálhatja a beállításokat és az ütemezéseket.
- **TFT kijelző**: Valós idejű hőmérséklet, páratartalom és egyéb adatok megjelenítése a beépített érintőképernyőn.
- **Egyedi ütemezések**: Hétköznapi és hétvégi fűtési ütemezések beállítása.
- **Wi-Fi kapcsolat**: Távoli vezérlés és monitorozás.
- **Energiahatékonyság**: A fűtés optimalizálása az energiatakarékosság érdekében.

---

## Első lépések

### Hardver beállítás
1. Csatlakoztassa a termosztátot egy áramforráshoz.
2. Győződjön meg róla, hogy az eszköz csatlakozik a fűtési rendszerhez.
3. Csatlakoztassa az eszközt a Wi-Fi hálózathoz.

### Szoftver beállítás
1. Nyissa meg a webes felületet a termosztát IP-címének böngészőbe írásával.
2. Jelentkezzen be az alapértelmezett hitelesítő adatokkal (ha szükséges).

---

## Webes felület

A webes felület lehetővé teszi a termosztát konfigurálását és monitorozását. Böngészőn keresztül érhető el.

### Fő szekciók
- **Jelenlegi állapot**: A szoba aktuális hőmérsékletének, az üzemidőnek és a szoftver verziójának megtekintése.
- **Ütemezések**: Hétköznapi és hétvégi fűtési ütemezések konfigurálása.
- **Beállítások**: Hiszterézis, hőmérséklet-kompenzáció és kívánt hőmérséklet beállítása.

### Dátum és idő beállítása
1. Navigáljon a "Dátum és idő" szekcióhoz.
2. Adja meg a dátumot és időt az `ééééhhnnóópp` formátumban.
3. Kattintson a "Beállít" gombra a mentéshez.

### Saját Access Point üzemmód

A termosztát saját WiFi Access Point módban is elérhető, IP címe: 192.168.99.9. Ebben az üzemmódban WiFi kliensként nem szükséges csatlakozni, hiszen az eszköz önállóan szolgáltatja a weblapot és az ElegantOTA (firmware frissítés) felületet a következő URL-eken:
- Weblap: http://192.168.99.9
- OTA frissítés: http://192.168.99.9/iwannaupdate majd utána http://192.168.99.9/update

---

## TFT kijelző

A beépített érintőképernyő valós idejű adatokat és vezérlési lehetőségeket biztosít.

### Navigáció
- **Lapozás vagy érintés**: Navigáljon a képernyők között, hogy megtekintse a hőmérsékletet, páratartalmat, ütemezéseket és egyebeket.
- **Ikonok**: Érintse meg az ikonokat, hogy elérje a kézi módot vagy a naptárat.

### Képernyők
1. **Főképernyő**: A szoba hőmérsékletének és az üzemmódnak a megjelenítése.
2. **Beállítások képernyő**: Hőmérséklet beállítása és a rendszer állapotának megtekintése.
3. **Ütemezés képernyő**: Az aktív ütemezések megtekintése.

---

## Programozott ütemezések

### Hétköznapi ütemezés
1. Lépjen a "Hétköznap" szekcióba a webes felületen.
2. Állítson be legfeljebb hat idő-hőmérséklet párt (pl. 07:00 - 22°C).
3. Mentse a változtatásokat.

### Hétvégi ütemezés
1. Lépjen a "Hétvége" szekcióba a webes felületen.
2. Állítson be legfeljebb hat idő-hőmérséklet párt.
3. Mentse a változtatásokat.

---

## Hibaelhárítás

### Gyakori problémák
- **Nincs Wi-Fi kapcsolat**: Győződjön meg róla, hogy az eszköz a router hatótávolságán belül van.
- **Helytelen hőmérséklet-értékek**: Kalibrálja a hőmérséklet-kompenzációt a beállításokban.
- **Nem válaszoló kijelző**: Indítsa újra az eszközt.

### Az eszköz alaphelyzetbe állítása
1. Nyomja meg és tartsa lenyomva a reset gombot 10 másodpercig.
2. Konfigurálja újra a beállításokat.

---

## HTML Felület és Érintőképernyő Használata

### HTML Felület

A termosztát webes felületén keresztül könnyedén konfigurálhatja az eszközt. Az alábbi mezők érhetők el:

#### **Hétköznap és Hétvége Programozása**
- **Időpontok és Hőmérsékletek**: 
  - Például: `07:00` -> `22.0°C`
  - Mezők: `wd1i`, `wd1T`, `we1i`, `we1T` stb.
- **Hétköznapok (wd)**: 6 időpont-hőmérséklet pár.
- **Hétvégék (we)**: 6 időpont-hőmérséklet pár.

#### **Egyéb Beállítások**
- **Pozitív Hiszterézis**: `hystp` mező (pl. `0.5°C`).
- **Negatív Hiszterézis**: `hystn` mező (pl. `-0.5°C`).
- **Hőmérséklet Kompenzáció**: `tempoffset` mező (pl. `0.2°C`).
- **Kívánt Hőmérséklet**: `hofok` mező (pl. `21.0°C`).

#### **Dátum és Idő Beállítása**
- **Formátum**: `ééééhhnnóópp` (pl. `202401011230`).
- **Rendszeridő Lekérdezése**: Egy gombnyomással kitölthető az aktuális idő.

---

### Érintőképernyő

Az érintőképernyőn az alábbi funkciók érhetők el:

#### **Főképernyő**
- **Szoba Hőmérséklet**: Jelenlegi hőmérséklet megjelenítése.
- **Idő és Dátum**: Aktuális idő és dátum.

#### **Interakciók**
- **Kézi Mód Aktiválása**: Érintse meg a kulcs ikont.
- **Programozott Mód Aktiválása**: Automatikus üzemmód visszaállítása.
- **Naptár Megnyitása**: Érintse meg a naptár ikont.
- **Hőmérséklet Beállítása**: Forgassa az érintőképernyőn megjelenő "tekerőt".

#### **Egyéb Információk**
- **Wi-Fi Jelerősség**: Jelerősség ikon a jobb felső sarokban.
- **Fűtési Állapot**: Radiátor ikon, ha a fűtés aktív.

---

## Műszaki adatok

- **Kijelző**: 320x240 TFT érintőképernyő
- **Kapcsolódás**: Wi-Fi (2.4 GHz)
- **Tápellátás**: 5V DC
- **Hőmérséklet-tartomány**: 15°C - 30°C
- **Méretek**: 100mm x 100mm x 25mm

---

További segítségért látogasson el a [támogatási oldalunkra](#) vagy lépjen kapcsolatba velünk a monitroleez@gmail.com címen.