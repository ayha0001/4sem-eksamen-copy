# Teknisk dokumentation

Afsluttende eksamensprojekt lavet af Agnete, Aylin, Emilie og Oscar. Team Ulvene.

## Projektbeskrivelse

Projektet er udviklet som afsluttende eksamensprojekt på 4. semester.

Formålet med den tekniske løsning er at udvikle en moderne og responsiv hjemmeside med fokus på komponentbaseret udvikling, semantisk HTML og genbrugelige UI-løsninger.

## Teknologier

Projektet er bygget op med:

- Astro 6
- React 19
- Tailwind CSS 4
- Prettier
- Supabase

## Installation

For at installere projektet lokalt skal dependencies først installeres:

```bash
npm install
```

Start derefter udviklingsserveren:

```bash
npm run dev
```

Projektet vil herefter kunne tilgås lokalt i browseren.

## Arbejdstilgang

Projektet er udviklet gennem Git og GitHub med feature-branch workflow.
Dette har gjort det muligt at arbejde parallelt uden at påvirke main-branchen direkte.

- Arbejd ikke direkte på main
- Opret en branch pr. feature/fix
- Merge tilbage til main når det virker og er testet

## Navngivning

I projektet er der arbejdet med en konsistent navngivningsstruktur for at sikre overblik, læsbarhed og genbrug af komponenter.

### Branches

Branches navngives med små bogstaver og bindestreger i stedet for mellemrum. Afslutningsvis tilføjes navnet på den person, der har arbejdet på branchen.

Eksempel: nyt-komponent-navn

### Pages

Sider i src/pages er navngivet med kebab-case, hvilket følger web-standarder for URL-struktur. Kebab-case er en navngivningskonvention, hvor ord skrives med små bogstaver og adskilles af bindestreger.

Eksempler:

- bliv-frivillig.astro
- kontakt-os.astro
- julegaveindsamling.astro

Dette sikrer SEO-venlige URLs og let genkendelige ruter.

### Komponenter

Komponenter er opdelt i mapper baseret på funktionalitet, fx:

- generelt
- faq
- forside

Komponenter navngives med PascalCase:

- Header.astro
- Hero.astro
- HeroLille.astro
- DelerStreg.astro

Dette gør det tydeligt, at der er tale om genbrugelige UI-komponenter.

### Semantisk navngivning

Navne er valgt ud fra funktion fremfor design:

Eksempler:

- Header → sidens topnavigation
- FooterMedlem → specifik footer variant
- TekstBillede / BilledeTekst → variationer af tekst placering

## Commit-strategi

Der anvendes en fast struktur i commit-beskeder for at skabe overblik og konsistens i projektets udvikling.

Alle commits starter med en handling:

- tilføjet → når ny funktionalitet eller filer oprettes
- fjernet → når kode eller filer slettes
- fikset → når fejl rettes

Eksempler:

- "tilføjet header komponent"
- "tilføjet kontakt-os side"
- "fjernet ikon i header"
- "fikset readme fil"

## Formatterings- og kode-standard

Vi bruger Prettier til formattering af vores kode.

- Prettier: til formatering af kode.
- prettier-plugin-tailwindcss: sorterer Tailwind-klasser automatisk

## Projektstruktur

I projektet har vi opbygget strukturen på følgende måde:

```text
/
├── public/assets
│   ├── grafik
│   │   └──  some-ikon
│   ├── holdet
│   ├── img
│   └── pdf
│  
├── src
│   ├── components
│   │   ├── afsnit
│   │   │    ├──  BilledeTekst.astro
│   │   │    ├──  IkonKort.astro
│   │   │    ├──  ProjektKort.astro
│   │   │    ├──  ProjektSektion.astro
│   │   │    ├──  TekstBillede.astro
│   │   │    └──  TekstCenter.astro
│   │   │ 
│   │   ├── bliv-frivillig
│   │   │    ├──  FormFrivillig.astro
│   │   │    └──  Galleri.astro
│   │   │ 
│   │   ├── faq
│   │   │    └──  DropDown.astro
│   │   │ 
│   │   ├── forside
│   │   │    ├──  DelerCitat.astro
│   │   │    ├──  FormHero.astro
│   │   │    ├──  MissionSektion.astro
│   │   │    ├──  MotionGraphics.astro
│   │   │    ├──  Taeller.astro
│   │   │    └──  TaellerSektion.astro
│   │   │ 
│   │   ├── generelt
│   │   │    ├──  Deler.astro
│   │   │    ├──  DelerGraa.astro
│   │   │    ├──  DelerStreg.astro
│   │   │    ├──  Footer.astro
│   │   │    ├──  FooterMedlem.astro
│   │   │    ├──  HDNBanner.astro
│   │   │    ├──  Header.astro
│   │   │    ├──  HeroLille.astro
│   │   │    ├──  Knap.astro
│   │   │    └──  Link.astro
│   │   │ 
│   │   ├── julegaveindsamling
│   │   │    └──  VideoKort.astro
│   │   │ 
│   │   ├── nyt-hjem
│   │   │    ├──  HjaelpSektion.astro
│   │   │    ├──  ImageSlider.astro
│   │   │    ├──  SliderKort.astro
│   │   │    └──  SogHjaelp.astro
│   │   │ 
│   │   ├── om-os
│   │   │    ├──  AnsatJob.astro
│   │   │    ├──  AnsatKort.astro
│   │   │    └──  AnsatSektion.astro
│   │   │ 
│   │   ├── partnere
│   │   │    ├──  FormPartner.astro
│   │   │    ├──  PartnerBanner.astro
│   │   │    ├──  PartnerKort.astro
│   │   │    ├──  PartnerSektion.astro
│   │   │    ├──  PartnerSektion2.astro
│   │   │    └──  PartnerSektion3.astro
│   │   │ 
│   │   ├── stoet-form
│   │   │    ├──  Betaling.astro
│   │   │    ├──  Oplysninger.astro
│   │   │    └──  StoetForm.astro
│   │   │ 
│   │   ├── testamente
│   │   │    └──  KontaktHjaelp.astro
│   │   │ 
│   │   └── udtalelser
│   │        ├──  UdtalelseKort.astro
│   │        └──  UdtalelseSektion.astro
│   │    
│   ├── layouts
│   │        └──  Layout.astro
│   │  
│   ├── pages
│   │        ├──  baeredygtighed.astro
│   │        ├──  betaling.astro
│   │        ├──  bliv-frivillig.astro
│   │        ├──  faq.astro
│   │        ├──  gennemsigtighed.astro
│   │        ├──  hvem-er-vi.astro
│   │        ├──  index.astro
│   │        ├──  julegaveindsamling.astro
│   │        ├──  kontakt-os.astro
│   │        ├──  nyt-hjem.astro
│   │        ├──  oplysninger-form.astro
│   │        ├──  partnere.astro
│   │        ├──  stoet-os.astro
│   │        ├──  tak.astro
│   │        ├──  testamente.astro
│   │        ├──  uddelinger.astro
│   │        ├──  udtalelser.astro
│   │        └──  vaernemidler.astro
│   │  
│   └── styles
│            └──  global.css
└── package.json
```
