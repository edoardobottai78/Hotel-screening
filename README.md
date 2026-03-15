# Hotel Talent — Screening CV

Tool di screening e ranking automatico dei curriculum per posizioni alberghiere.

## Struttura del progetto

```
hotel-screening/
├── index.html          # Frontend completo
├── api/
│   └── analyze.js      # Serverless function (proxy Anthropic API)
├── vercel.json         # Configurazione Vercel
└── README.md
```

## Deploy su Vercel (5 minuti)

### 1. Crea un repository GitHub

1. Vai su [github.com](https://github.com) e accedi (o crea un account)
2. Clicca **"New repository"**
3. Dai un nome: `hotel-screening`
4. Lascia tutto il resto di default, clicca **"Create repository"**
5. Carica i file: trascina la cartella `hotel-screening` nella pagina del repository oppure usa il pulsante **"uploading an existing file"**

### 2. Collegati a Vercel

1. Vai su [vercel.com](https://vercel.com) e accedi con il tuo account GitHub
2. Clicca **"Add New Project"**
3. Seleziona il repository `hotel-screening` appena creato
4. Clicca **"Deploy"** — Vercel rileva automaticamente la configurazione

### 3. Aggiungi la chiave API Anthropic

Dopo il primo deploy (che fallirà perché manca la chiave):

1. Nel pannello Vercel, vai su **Settings → Environment Variables**
2. Clicca **"Add New"**
3. Nome: `ANTHROPIC_API_KEY`
4. Valore: la tua chiave API (inizia con `sk-ant-...`)
5. Ambiente: seleziona **Production**, **Preview**, **Development**
6. Clicca **"Save"**
7. Vai su **Deployments** e clicca **"Redeploy"** sull'ultimo deploy

### 4. Il tool è online

Vercel ti fornisce un URL tipo `hotel-screening-xyz.vercel.app` — aprilo da qualsiasi browser.

## Come ottenere la chiave API Anthropic

1. Vai su [console.anthropic.com](https://console.anthropic.com)
2. Accedi o crea un account
3. Vai su **API Keys → Create Key**
4. Copia la chiave e incollala in Vercel come indicato sopra

## Aggiornamenti futuri

Per aggiornare il tool, modifica i file e fai push su GitHub — Vercel rideploya automaticamente.
