# Hüseyin Ateş
### Principal AI Systems Architect & Autonomous Code Evolution Researcher
**Istanbul, Turkey** · [GitHub: @HuseyinAts](https://github.com/HuseyinAts) · [Autonomous Systems & Cybernetics Lab]

---

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│ ARAŞTIRMA PARADİGMASI: "PROGRAM SENTETİK BİR BİYOLOJİK ORGANİZMADIR"                                 │
│                                                                                                        │
│ Yazılım mühendisliğinin geleneksel 'statik kaynak kodu' paradigması, insan zihninin bilişsel          │
│ sınırlarına göre tasarlanmış geçici bir arayüzdür. Gerçek sistem dayanıklılığı; insan gözüyle          │
│ okunabilir metin dosyalarında değil, çalışma zamanında (runtime) sürekli polimorfik olarak             │
│ mutasyona uğrayan, dış API'lere sıfır bağımlılıkla kendi kendini izole ortamlarda onaran               │
│ ve kernel seviyesinde hat hızında evrimleşen deterministik matematiksel topolojilerde yatar.           │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 🏛️ BİLİMSEL DANIŞMA KURULU VE KURAMSAL TEMELLER

Bu profil ve bünyesindeki tüm araştırma repoları, bilgisayar bilimleri ve yapay zeka literatürünün 5 temel kuramsal disiplininin doğrudan sentezi üzerine inşa edilmiştir:

```
                  ┌────────────────────────────────────────────────────────┐
                  │              HÜSEYİN ATEŞ ARAŞTIRMA LABORATUVARI        │
                  └───────────────────────────┬────────────────────────────┘
                                              │
         ┌──────────────────┬─────────────────┼──────────────────┬──────────────────┐
         ▼                  ▼                 ▼                  ▼                  ▼
┌─────────────────┐┌─────────────────┐┌────────────────┐┌─────────────────┐┌─────────────────┐
│ Linus Torvalds  ││ Andrej Karpathy ││  Judea Pearl   ││   John Koza     ││ Andreas Zeller  │
│ [Kernel/Sistem] ││ [Nöro-Sembolik] ││  [Nedensellik] ││ [Genetik Prog.] ││ [Hata Onarımı]  │
├─────────────────┤├─────────────────┤├────────────────┤├─────────────────┤├─────────────────┤
│ • eBPF / XDP L4 ││ • A100 LLM Tune ││ • Do-Calculus  ││ • ExprTree GP   ││ • Ochiai SBFL   │
│ • Determinizm   ││ • Cerrahi RAG   ││ • Spektral DAG ││ • Parsimony     ││ • ddmin Delta-D.│
│ • Sıfır Kopyalama││ • Local Swarm   ││ • Do-Intervene ││ • Bloat Kontrol ││ • Overfitting K.│
└─────────────────┘└─────────────────┘└────────────────┘└─────────────────┘└─────────────────┘
```

1. **Sistemler & Donanım Seviyesi İzolasyon (Linus Torvalds Ekolü):** V8 Worker Threads tecriti, Linux cgroups/namespaces sınırlarında Docker sandbox potası ve Linux Kernel XDP/eBPF seviyesinde sıfır-kopyalama ağ savunması.
2. **Nöro-Sembolik Yapay Zeka & Dil Modelleri (Andrej Karpathy Ekolü):** Dış bulut sağlayıcılarına kapalı, yerel GPU kümelerinde (Ollama / vLLM) çalışan ve AST grafından çekilmiş cerrahi bağlamla (Micro-RAG) mutasyon öneren çok-ajanlı sürü zekası.
3. **Nedensel Akıl Yürütme ve Bilgi Geometrisi (Judea Pearl Ekolü):** Statik import korelasyonunu ($P(\text{fail} \mid X)$), müdahaleci nedensellik ($P(\text{fail} \mid \text{do}(X=v))$) seviyesine taşıyan yapısal nedensellik modelleri (SCM) ve spektral graf difüzyonu.
4. **Yapısal Genetik Programlama (John Koza Ekolü):** Sabit sayısal eşik ayarını aşan, programın kontrol akışını ve mantıksal ağacını doğrudan mutasyona uğratan Koza-style boolean ifade ağacı (`ExprTree`) evrimi.
5. **Otomatik Hata Onarımı ve Spektrum Analizi (Andreas Zeller & Claire Le Goues Ekolü):** Çalışan testlerin kapsama matrisinden Ochiai şüphe skorları çıkaran SBFL motoru ve Zeller'in *ddmin (Delta Debugging)* algoritmasıyla minimal cerrahi yamalar üreten anti-overfitting altyapısı.

---

## 🔬 ÇEKİRDEK ARAŞTIRMA PROJELERİ VE MİMARİLERİ

### 1. [TOHUM](https://github.com/HuseyinAts/tohum) — Otonom Kod Evrim Fabrikası & Çok-Dilli Genetik Programlama
> *Runtime'da sıfır dış LLM bağımlılığı; 5 dilde (Rust, TS, JS, Python, Go) AST yutma, Docker potasında izole test-suite fitness ve nedensel graf mutasyonu.*

```
                                  [ HEDEF KOD TABANI ]
                                           │ (5-Dil AST Ingestion)
                                           ▼
┌─────────────────────────────── src/memory/graph.ts ───────────────────────────────┐
│ Saf JS In-Memory / JSON Graf Motoru (File-IMPORTS-File, Func-CALLS-Func, Gene)    │
└──────────────────────────────────────────┬────────────────────────────────────────┘
                                           │
       ┌───────────────────────────────────┴───────────────────────────────────┐
       ▼                                                                       ▼
┌────────────── src/crucible/ ──────────────┐           ┌────────────── src/genome/ ──────────────┐
│ • coverage.ts: Ochiai / Tarantula SBFL    │           │ • graphWeights.ts: w^p Keskinleştirme    │
│ • dockerArena.ts: --network=none Tecrit   │◄─────────►│ • leverageEstimator.ts: Otomatik K      │
│ • patchReducer.ts: ddmin Yama Küçültücü   │           │ • apr.ts: Guard/Delete/Off-By-One APR   │
└───────────────────────────────────────────┘           └─────────────────────────────────────────┘
                                           │
                                           ▼
┌───────────────────────────────── src/core/evoloop.ts ───────────────────────────────┐
│ OODA Evrimsel Karar Döngüsü: Turnuva Seçilimi + Parsimony Baskısı + Plato Dedektörü │
└──────────────────────────────────────────┬──────────────────────────────────────────┘
                                           │ (Plato Anında Cerrahi Tetikleme)
                                           ▼
┌───────────────────────────────── src/swarm/advisor.ts ──────────────────────────────┐
│ Yerel Ollama (Qwen-Coder 8B/14B) Nöro-Sembolik Danışmanı (Sıfır Bulut Bağımlılığı)  │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

#### Ölçülmüş ve Hakemli Ampirik İspatlar (Empirical Benchmarks):
- **Yapısal GP > Literal-Ayar (Koza Üstünlüğü):** Aynı tohum ve ortamda Yapısal GP $\approx 0.876\ [0.850, 0.901]$ vs Sabit İskelet $\approx 0.816\ [0.793, 0.840]$ ayrık güven aralığı ile tescillendi.
- **Oracle Gen Seçimi:** Graf heuristiğindeki seyreltme aşılarak $w^p$ keskinleştirmesiyle $+0.3233$ meanDiff ($t=17.03, p=0$) rekor kazanç elde edildi.
- **Açlık Tavanı Çözümü ($K \ge |\text{leverage-set}|$):** $K=1$'deki $0.6944$ açlık kapağı, otomatik $K \ge 4$ spektral kestirimi ile kırılarak ortalama skor $0.8444$'e yükseltildi.
- **Yerel Model Kalibrasyonu:** Qwen 8B/14B modellerinin gradyansız kriz anlarında deterministik rastgeleliğe $t=9.654$ ($p < 0.001$) ile ezici üstünlük sağladığı belgelendi.

---

### 2. [Kozalak (OSIRIS)](https://github.com/HuseyinAts/kozalak) — Katmanlı Siber Savunma & Tehdit İstihbaratı
> *GUT-AD sözde-biliminden arındırılmış, deterministik L3-L7 katmanlı bot savunması ve adaptif challenge mimarisi.*

- **Katman 1 (Ağ/TLS Parmak İzi):** JA4/JA4+ TLS ClientHello hash analizi ile HTTP/2 çerçeve sırası (SETTINGS, WINDOW_UPDATE) tutarlılık çapraz doğrulaması (Join).
- **Katman 2 & 3 (Davranışsal Entropi):** İstemci tarafı zamanlama aralıkları ($dt$), fare/dokunmatik hareket vektörleri ve lockstep koordinasyon kümelemesi.
- **Katman 4 (Adaptif Kademeli Yanıt):** İkili bloklama yerine risk olasılığına ($P(\text{bot} \mid \mathbf{x})$) göre ölçeklenen yanıt: `Allow` $\to$ `Transparent Token` $\to$ `PoW Step-Up` $\to$ `Block`.

---

### 3. [TEKNOFEST 2025 Eğitim-Eylemci](https://github.com/HuseyinAts/teknofest-2025-egitim-eylemci) — Türkçe LLM & Dilbilgisel AI
> *A100 40GB Tensor Core hızlandırmalı, morfolojik kurallara duyarlı Türkçe Büyük Dil Modeli optimizasyon boru hattı.*

- **A100 Donanım Optimizasyonu:** TF32, Flash Attention 2 ve BF16 karma hassasiyetli matris çarpımları ile 38.0 GB VRAM sınırında tam bellek havuzlaması.
- **Türkçe Morfolojik Kısıt Motoru:** Ünlü uyumu denetimi (Vowel Harmony Engine) ve büyük/küçük İ/ı harf ayrımını koruyan gelişmiş Unicode işleme mimarisi.

---

## 📂 ARAŞTIRMA REPOLARI VE EKOSİSTEM İNDEKSİ

Tüm açık kaynak ve özel depolar, bilgisayar bilimleri uzmanlık alanlarına göre aşağıda sınıflandırılmıştır:

| Alan | Depo Adı | Çekirdek Teknoloji | Mimari Kapsam |
|---|---|---|---|
| **Otonom Kod Evrimi & APR** | 🧬 **[tohum](https://github.com/HuseyinAts/tohum)** | `Rust`, `WASM`, `TS`, `Docker` | Genetik Programlama, SBFL Hata Lokalizasyonu, Causal Graph Weights |
| **Siber Savunma & OSINT** | 🛡️ **[kozalak](https://github.com/HuseyinAts/kozalak)** | `TypeScript`, `Network-Sec`, `WAF` | OSIRIS Katmanlı Bot Savunması, CVE Analizi, JA4+ TLS Denetimi |
| **Büyük Dil Modelleri & NLP** | 🇹🇷 **[teknofest-2025](https://github.com/HuseyinAts/teknofest-2025-egitim-eylemci)** | `Python`, `PyTorch`, `A100` | Türkçe LLM Fine-Tuning, Morfolojik Analiz, Eğitim Ajanı |
| **Büyük Veri & Doğal Dil İşleme**| 📊 **[TrendMiner 2025](https://github.com/HuseyinAts/TrendMiner-_BilisimVadisi2025_Tddi2025)** | `Python`, `Jupyter`, `TDDI` | Bilişim Vadisi Trend Analizi ve Türkçe Metin Madenciliği |
| **Yarışma & Algoritma Sentezi** | 🏛️ **[Acikhack2023](https://github.com/HuseyinAts/Acikhack2023_TrendMiner)** | `Python`, `Machine-Learning` | AçıkHack Doğal Dil İşleme ve Karar Ağaçları |
| **Tarihi Dil Teknolojileri** | 📜 **[Osmanlıca TDDI](https://github.com/HuseyinAts/Osmanli_Acikhack2024_TDDI)** | `Python`, `OCR`, `NLP` | AçıkHack 2024 Osmanlıca Metin Sınıflandırma ve İnce Ayar |
| **Otonom İş Akışları** | 🤖 **[kiro2](https://github.com/HuseyinAts/kiro2)** | `Python`, `Agentic-Workflow` | Otonom Ajan Karar Döngüleri ve Kod Analiz Arayüzü |
| **Konuşma & Ses Tanıma** | 🎙️ **[voice](https://github.com/HuseyinAts/voice)** / **[trses](https://github.com/HuseyinAts/trses)** | `Python`, `Speech-Processing` | Türkçe Akustik Model Analizi ve Ses Tanıma Katmanı |
| **Sosyal Veri Madenciliği** | 🐦 **[TurkceTweet](https://github.com/HuseyinAts/TurkceTweet)** | `Python`, `Dataset`, `NLP` | Türkçe Tweet Duygu Analizi ve Büyük Metin Külliyatı |
| **Dağıtık Hesaplama** | 🐘 **[hadoop](https://github.com/HuseyinAts/hadoop)** | `Java`, `Distributed-Systems` | Apache Hadoop Dağıtık Büyük Veri Mimarisi İncelemesi |

---

## 📊 TEKNİK VE SİSTEMSEL DİSİPLİN

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│ MÜHENDİSLİK MANİFESTOSU:                                                                              │
│                                                                                                        │
│ 1. "Anti-Rigging": Deneyler peşin kabulle kurulmaz. Negatif çıkan her sonuç (örn. treeAdvisor plato   │
│    tavanı veya 1/5 kuralı sigma çöküşü) dürüstçe belgelenir ve literatüre kazandırılır.               │
│ 2. "Zero-Vaporware": Çalışmayan hiçbir teori, matematiksel fantezi veya sözde-bilim koda giremez.      │
│    Her hipotez (örn. K >= leverage-set) çift yönlü paired-t ve sign-flip testleriyle kilitlenir.      │
│ 3. "Air-Gapped Sovereignity": Kritik savunma ve kod üretim hatları asla üçüncü taraf API'lere         │
│    telemetri sızdırmaz; her hesaplama yerel metal üzerinde deterministik olarak icra edilir.           │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

<div align="center">
  <sub>© 2026 Hüseyin Ateş · Otonom Sistemler ve Siber Bağışıklık Mimarisi Laboratuvarı</sub>
</div>
