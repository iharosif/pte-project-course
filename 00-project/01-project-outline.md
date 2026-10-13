---
name: Ihárosi Ferenc
neptun: AXFISX
id: 2026-NP-01
github: https://github.com/iharosif/pte-project-course
github_project: https://github.com/users/iharosif/projects/1
---
# Kliensoldali előrejelzés és szerverrel történő állapot-egyeztetés többszereplős játékban

A projekt célkitűzése összetett. Először meg kell tervezni és implementálni egy kliensoldali előrejelzési stratégiát, illetve azt, hogy a kliens és a szerver hogyan cserél információt egymással. Utána meg kell vizsgálni, hogyan teljesít az előrejelzési stratégia egy naiv állapotegyeztetési megoldással szemben. Vizsgálni kell, hogy a hálózati körülmények milyen hatással vannak a szinkronizációs eljárásokra. A mérések során szimulálni kell a késleltetésnek és a csomagvesztésnek különböző mértékű kombinációit.

## Célok

- **Elsődleges cél:** Kliensoldali előrejelzés megvalósítása, annak szemléltetése egy egyszerű demonstrátorral, majd összehasonlítása egy naiv szinkronizációs technikával különböző hálózati körülmények között

- **Célfelhasználók / érintettek:** Játékkészítés iránt érdeklődők

- **Mérhető sikerkritériumok:**
	- Elkészült az egyszerű demonstrátor
	- Elkészült a szerver
	- A kliens és a szerver egymással információt képes megosztani
	- A kliens megvalósítja a specifikációban előírt előrejelzési technikát
	- Hálózati körülmények szimulálhatók
	- A naiv és a komplex szinkronizációs technika egymással összehasonlítható
	
- **Korlátok:** Authoritative szerver-kliens architektúra; Demonstrátor C++, SFML; Szerver C++, boost.asio; hálózati körülmények szimulálása Python, pydivert; mérési adatsorok kiértékelése és vizualizálása Python, matplotlib

## Hatókör

### Benne van a hatókörben

- Egyszerű videójáték megtervezése és elkészítése (demonstrátor)
- Kliensoldali előrejelzés és egy naiv állapotszinkronizációs technika megtervezése és implementálása
- Egyszerű alkalmazásrétegbeli protokoll megtervezése és megvalósítása
- Hálózati körülmények (késleltetés, csomagvesztés) szimulálása 
- Mérések, mérőszámok pontos meghatározása

### Nincs benne a hatókörben

- Szinkronizáció bemutatása egy komplex videójátékon keresztül
- Saját hálózati könyvtár elkészítése
- Saját játékmotor elkészítése
- Több száz vagy ezer kliens egyidejű kiszolgálása

## Jegyzetek

A rendszer egyes komponenseinek megvalósítására külön-külön fázisban kerül sor. Az első fázis során a szervert készíteném el, megtervezem a klienssel együttesen használt protokollt, a szerver belső adatstruktúráit, a felhasználótól érkező adatok feldolgozásának módját. A második fázisban a demonstrátort készítem el. Meghatározom, hogy milyen bemenetekre milyen változás menjen végbe, milyen időközönként küldjön a szervernek frissítéseket, hogyan igazítja magát a szervertől érkező játékállapothoz. A harmadik fázisban a hálózati körülményeket szimuláló komponenst készítem el. A legfontosabb feladata ennél a komponensnél az, hogy pontosan meg legyen határozva milyen körülményeket kell szimulálni. Miután elkészült a rendszer összes eleme, a negyedik fázisban végzek egy rendszerszintű tesztelést. Az ötödik fázisban végrehajtom a méréseimet és összegzem az eredményeket.

