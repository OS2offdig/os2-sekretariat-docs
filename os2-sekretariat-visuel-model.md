---
title: Sekretariatets ydelser
layout: default
nav_order: 100
has_toc: false
---

<style>
  #os2-secretariat-model {
    --series-1: var(--viz-series-1, var(--primary));
    --series-2: var(--viz-series-2, var(--primary));
    --series-3: var(--viz-series-3, var(--primary));
    --series-4: var(--viz-series-4, var(--primary));
    --series-5: var(--viz-series-5, var(--primary));
    --series-6: var(--viz-series-6, var(--primary));
    color: var(--foreground);
    font-family: var(--font-sans, ui-sans-serif, system-ui, sans-serif);
    width: 100%;
    padding: 1rem 0 1.5rem;
  }

  #os2-secretariat-model *,
  #os2-secretariat-model *::before,
  #os2-secretariat-model *::after {
    box-sizing: border-box;
  }

  #os2-secretariat-model .stage-label {
    color: var(--muted-foreground);
    font-size: var(--text-xs, 0.75rem);
    font-weight: 500;
    letter-spacing: 0.08em;
    margin: 0 0 0.45rem;
    text-align: center;
    text-transform: uppercase;
  }

  #os2-secretariat-model .card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: var(--radius-lg, 0.75rem);
    color: var(--card-foreground, var(--foreground));
    box-shadow: var(--shadow-sm, 0 1px 2px rgba(0, 0, 0, 0.06));
  }

  #os2-secretariat-model .mission {
    background: var(--primary);
    border-color: var(--primary);
    color: var(--primary-foreground);
    margin: 0 auto;
    max-width: 76rem;
    padding: 1.25rem 1.4rem;
  }

  #os2-secretariat-model .mission strong {
    display: block;
    font-size: var(--text-xl, 1.25rem);
    line-height: 1.35;
    margin-bottom: 0.85rem;
    text-align: center;
  }

  #os2-secretariat-model .mission p {
    margin: 0.65rem 0 0;
  }

  #os2-secretariat-model .mission-more {
    border-top: 1px solid color-mix(in srgb, var(--primary-foreground) 35%, transparent);
    display: block;
    font-size: var(--text-sm, 0.875rem);
    margin-top: 1rem;
    padding-top: 0.75rem;
    text-align: center;
  }

  #os2-secretariat-model .connector {
    align-items: center;
    display: flex;
    flex-direction: column;
    height: 2.6rem;
    justify-content: center;
  }

  #os2-secretariat-model .connector::before {
    background: var(--border);
    content: "";
    height: 1.75rem;
    width: 2px;
  }

  #os2-secretariat-model .connector::after {
    border-left: 0.32rem solid transparent;
    border-right: 0.32rem solid transparent;
    border-top: 0.42rem solid var(--muted-foreground);
    content: "";
  }

  #os2-secretariat-model .services {
    margin: 0 auto;
    max-width: 76rem;
    padding: 1rem;
  }

  #os2-secretariat-model .services h2 {
    font-size: var(--text-lg, 1.125rem);
    margin: 0 0 0.8rem;
    text-align: center;
  }

  #os2-secretariat-model .service-grid {
    display: grid;
    gap: 0.7rem 1.1rem;
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  #os2-secretariat-model .service-item {
    background: color-mix(in srgb, var(--primary) 9%, var(--card));
    border-left: 0.25rem solid var(--primary);
    border-radius: var(--radius-md, 0.5rem);
    padding: 0.75rem 0.8rem;
  }

  #os2-secretariat-model .service-item h3 {
    margin: 0 0 0.35rem;
  }

  #os2-secretariat-model .service-item p {
    color: var(--foreground);
    font-size: var(--text-sm, 0.875rem);
    margin: 0;
  }

  #os2-secretariat-model .role-grid {
    align-items: start;
    display: grid;
    gap: 0.8rem;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    margin: 0 auto;
    max-width: 96rem;
  }

  #os2-secretariat-model .role-column {
    min-width: 0;
  }

  #os2-secretariat-model .role-head {
    align-items: center;
    border-top: 0.35rem solid var(--role-color);
    display: flex;
    flex-direction: column;
    gap: 0.35rem;
    justify-content: center;
    min-height: 8rem;
    padding: 0.75rem 0.55rem;
    text-align: center;
  }

  #os2-secretariat-model .role-head h3 {
    font-size: var(--text-base, 1rem);
    line-height: 1.25;
    margin: 0;
  }

  #os2-secretariat-model .role-scope {
    color: var(--muted-foreground);
    font-size: var(--text-xs, 0.75rem);
    line-height: 1.25;
    margin: 0;
  }

  #os2-secretariat-model .task-label {
    color: var(--muted-foreground);
    font-size: var(--text-xs, 0.75rem);
    font-weight: 500;
    letter-spacing: 0.05em;
    margin: 0.65rem 0 0.4rem;
    text-align: center;
    text-transform: uppercase;
  }

  #os2-secretariat-model .task-list {
    display: grid;
    gap: 0.45rem;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  #os2-secretariat-model .task-list li {
    background: color-mix(in srgb, var(--role-color) 9%, var(--background));
    border-left: 0.25rem solid var(--role-color);
    border-radius: 0 var(--radius-md, 0.5rem) var(--radius-md, 0.5rem) 0;
    font-size: var(--text-sm, 0.875rem);
    line-height: 1.3;
    padding: 0.45rem 0.55rem;
  }

  #os2-secretariat-model .task-link,
  #os2-secretariat-model .services-more {
    margin: 1rem auto 0;
    max-width: 96rem;
    text-align: center;
  }

  #os2-secretariat-model .task-link a,
  #os2-secretariat-model .services-more a {
    color: var(--primary);
    font-weight: 500;
  }

  #os2-secretariat-model .role-1 { --role-color: var(--series-1); }
  #os2-secretariat-model .role-2 { --role-color: var(--series-2); }
  #os2-secretariat-model .role-3 { --role-color: var(--series-3); }
  #os2-secretariat-model .role-4 { --role-color: var(--series-4); }
  #os2-secretariat-model .role-5 { --role-color: var(--series-5); }
  #os2-secretariat-model .role-6 { --role-color: var(--series-6); }

  #os2-secretariat-model .reading-key {
    align-items: center;
    color: var(--muted-foreground);
    display: flex;
    flex-wrap: wrap;
    font-size: var(--text-sm, 0.875rem);
    gap: 0.35rem 0.55rem;
    justify-content: center;
    margin-top: 1.1rem;
    text-align: center;
  }

  #os2-secretariat-model .reading-key strong {
    color: var(--foreground);
  }

  #os2-secretariat-model .reading-key .arrow {
    color: var(--primary);
    font-weight: 500;
  }

  @media (max-width: 1100px) {
    #os2-secretariat-model .role-grid {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }
  }

  @media (max-width: 640px) {
    #os2-secretariat-model {
      padding-inline: 0.25rem;
    }

    #os2-secretariat-model .service-grid,
    #os2-secretariat-model .role-grid {
      grid-template-columns: 1fr;
    }

    #os2-secretariat-model .role-column {
      display: block;
      margin-bottom: 0.55rem;
    }

    #os2-secretariat-model .role-head {
      height: 100%;
      min-height: 0;
    }
  }
</style>

<div id="os2-secretariat-model" aria-label="Model for sekretariatets mission, ydelser, roller og opgavekort">
  <p class="stage-label">Hvorfor sekretariatet findes</p>
  <section class="card mission" aria-labelledby="mission-title">
    <strong id="mission-title">I OS2-sekretariatet gør vi OS2’s medlemmer og produktfællesskaber i stand til at lykkes sammen.</strong>
    <p>Sekretariatet understøtter medlemmer, produktfællesskaber og bestyrelse ved at skabe og vedligeholde fælles rammer, relationer, kompetencer og værktøjer. Arbejdet tager afsæt i OS2’s vedtægter, vision, mission, styringsmodel, organisering og fælles principper.</p>
    <p>Sekretariatet lykkes, når medlemmerne og produktfællesskaberne kan samarbejde mere selvstændigt, åbent og bæredygtigt. Sekretariatet skal opbygge kapacitet i fællesskabet, ikke gøre fællesskabet afhængigt af sekretariatet.</p>
    <span class="mission-more">Læs mere om sekretariatets mission</span>
  </section>

  <div class="connector" aria-hidden="true"></div>

  <p class="stage-label">Hvad sekretariatet leverer</p>
  <section class="card services" aria-labelledby="services-title">
    <h2 id="services-title">Ydelser og ydelsesområder</h2>
    <div class="service-grid">
      <article class="service-item">
        <h3>Strategisk ledelse og foreningsudvikling</h3>
        <p>Omsætter OS2’s strategi og bestyrelsens beslutninger til prioriteringer, planer og konkrete indsatser. Området omfatter også udvikling af foreningen, sekretariatet og den samlede produktportefølje.</p>
      </article>
      <article class="service-item">
        <h3>Governance og organisationsudvikling</h3>
        <p>Udvikler og vedligeholder styringsmodeller, roller, mandater og beslutningsprocesser. Formålet er at skabe tydelige rammer og understøtte velfungerende, selvstyrende produktfællesskaber.</p>
      </article>
      <article class="service-item">
        <h3>Udvikling af produktfællesskaber</h3>
        <p>Etablerer og styrker samarbejdet omkring OS2’s produkter. Det omfatter blandt andet onboarding, facilitering, erfaringsdeling og udvikling af fællesskabet mellem produktkoordinatorer, product owners, community managers og øvrige deltagere.</p>
      </article>
      <article class="service-item">
        <h3>Produktmodning og innovationsstøtte</h3>
        <p>Hjælper idéer og projekter med at udvikle sig til levedygtige og skalerbare OS2-produkter. Det indebærer afklaring af behov, værdi, organisering, finansiering, roadmap og grundlag for fælles drift.</p>
      </article>
      <article class="service-item">
        <h3>Arkitektur og teknisk kvalitet</h3>
        <p>Understøtter åbne og bæredygtige tekniske løsninger. Området omfatter arkitektur, åbne standarder, dokumentation, sikkerhed, kodekvalitet, repositories og mulighederne for at skifte leverandør.</p>
      </article>
      <article class="service-item">
        <h3>Kommunikation og community</h3>
        <p>Gør OS2’s arbejde, produkter og resultater forståelige og synlige. Det omfatter kommunikationsplanlægning, indhold, fælles kanaler, produktfortællinger og aktiviteter, der styrker deltagelse og tilhørsforhold.</p>
      </article>
      <article class="service-item">
        <h3>Arrangementer og netværk</h3>
        <p>Planlægger og gennemfører møder, webinarer, temadage, konferencer og netværksaktiviteter. Formålet er at skabe relationer, dele viden og engagere medlemmer og samarbejdspartnere.</p>
      </article>
      <article class="service-item">
        <h3>Forretningsdrift og administration</h3>
        <p>Sikrer en stabil og professionel daglig drift. Området omfatter økonomi, budgetopfølgning, fakturering, medlemsadministration, aftaler, kontrakter, indkøb og håndtering af henvendelser.</p>
      </article>
      <article class="service-item">
        <h3>Fælles værktøjskasse og metoder</h3>
        <p>Udvikler og vedligeholder fælles skabeloner, vejledninger, procesbeskrivelser og arbejdsredskaber. Det gør OS2’s arbejdsformer lettere at forstå, genbruge og anvende på tværs.</p>
      </article>
      <article class="service-item">
        <h3>Interessevaretagelse og strategiske relationer</h3>
        <p>Repræsenterer OS2’s og medlemmernes interesser i relevante samarbejder og debatter. Området omfatter relationsopbygning, partnerskaber og dialog om blandt andet open source, digital suverænitet og offentligt digitalt samarbejde.</p>
      </article>
    </div>
    <p class="services-more"><a href="docs/03-ydelseskatalog.md">Læs mere om ydelser og ydelsesområder →</a></p>
  </section>

  <div class="connector" aria-hidden="true"></div>

  <p class="stage-label">Hvem der løser arbejdet – og hvordan</p>
  <div class="role-grid">
    <section class="role-column role-1" aria-labelledby="role-leadership">
      <div class="card role-head">
        <h3 id="role-leadership">Ledelse / strategi</h3>
        <p class="role-scope">Sætter retning, prioriterer kapacitet og omsætter bestyrelsens beslutninger til planer, relationer og opfølgning.</p>
      </div>
      <p class="task-label">Eksempler på opgavekort</p>
      <ul class="task-list">
        <li>Omsæt strategisk beslutning til leveranceplan</li>
        <li>Udarbejd sagsoplæg</li>
        <li>Prioritér portefølje og ressourcer</li>
        <li>Følg op på strategiske mål</li>
      </ul>
    </section>

    <section class="role-column role-2" aria-labelledby="role-business">
      <div class="card role-head">
        <h3 id="role-business">Forretnings&shy;koordinator</h3>
        <p class="role-scope">Sikrer den administrative og økonomiske drift og skaber kontinuitet i aftaler, data, møder, adgange og fælles rutiner.</p>
      </div>
      <p class="task-label">Eksempler på opgavekort</p>
      <ul class="task-list">
        <li>Modtag og fordel henvendelser</li>
        <li>Følg op på budget og økonomi</li>
        <li>Håndtér fakturaer og indkøb</li>
        <li>Koordinér aftaler og kontrakter</li>
      </ul>
    </section>

    <section class="role-column role-3" aria-labelledby="role-community">
      <div class="card role-head">
        <h3 id="role-community">Produktkonsulent / fællesskabskonsulent</h3>
        <p class="role-scope">Driver fællesskabet mellem produktroller og understøtter onboarding og modning af nye projekter og produkter.</p>
      </div>
      <p class="task-label">Eksempler på opgavekort</p>
      <ul class="task-list">
        <li>Driv fællesskabet for produktroller</li>
        <li>Facilitér erfaringsdeling og fælles praksis</li>
        <li>Onboard nye projekter og produkter til OS2</li>
        <li>Understøt governance og produktmodning</li>
      </ul>
    </section>

    <section class="role-column role-4" aria-labelledby="role-architecture">
      <div class="card role-head">
        <h3 id="role-architecture">IT-arkitekt</h3>
        <p class="role-scope">Sikrer fælles tekniske rammer, åben arkitektur, dokumentation, sikkerhed og kvalitet på tværs af OS2’s produkter.</p>
      </div>
      <p class="task-label">Eksempler på opgavekort</p>
      <ul class="task-list">
        <li>Gennemfør arkitektursparring</li>
        <li>Etablér GitHub og repositories</li>
        <li>Kvalitetssikr teknisk dokumentation</li>
        <li>Koordinér sikkerhedsscan og code review</li>
      </ul>
    </section>

    <section class="role-column role-5" aria-labelledby="role-communication">
      <div class="card role-head">
        <h3 id="role-communication">Kommunikations&shy;medarbejder</h3>
        <p class="role-scope">Gør OS2’s arbejde synligt og forståeligt og understøtter produkter og fællesskaber med kommunikation, kanaler og arrangementer.</p>
      </div>
      <p class="task-label">Eksempler på opgavekort</p>
      <ul class="task-list">
        <li>Analysér kommunikationsbehov</li>
        <li>Udarbejd kommunikationsplan</li>
        <li>Publicér i fælles kanaler</li>
        <li>Skab produktfortælling og skabeloner</li>
      </ul>
    </section>

    <section class="role-column role-6" aria-labelledby="role-product">
      <div class="card role-head">
        <h3 id="role-product">Produkt&shy;koordinator</h3>
        <p class="role-scope">Har operativt ansvar for ét konkret OS2-produkt og koordinerer roadmap, leverancer, styring, leverandører og brugere.</p>
      </div>
      <p class="task-label">Eksempler på opgavekort</p>
      <ul class="task-list">
        <li>Vedligehold roadmap og backlog</li>
        <li>Følg op på leverancer og afhængigheder</li>
        <li>Forbered styre- og koordinationsmøder</li>
        <li>Koordinér leverandør- og brugerbehov</li>
      </ul>
    </section>
  </div>

  <p class="task-link"><a href="playbooks/README.md">Se alle detaljerede opgavekort →</a></p>
</div>
