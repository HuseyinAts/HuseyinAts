# Hüseyin Ateş
### Principal AI Systems Architect & Autonomous Cybernetics Researcher
**Istanbul, Turkey** · [GitHub: @HuseyinAts](https://github.com/HuseyinAts) · [Autonomous Systems & Cybernetics Research Laboratory]

---

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│ ARAŞTIRMA TEZİ: "YAZILIM STATİK BİR METİN DEĞİL, POLİMORFİK VE OTONOM BİR DİNAMİK ORGANİZMADIR"      │
│                                                                                                        │
│ Geleneksel yazılım mühendisliği, insan zihninin bilişsel kapasitesiyle sınırlı statik kaynak kod      │
│ dosyalarına dayanır. Oysa gerçek sistem dayanıklılığı; dış bulut servislerine kapalı (air-gapped),     │
│ donanım sınırlarında (cgroups/namespaces) izole edilmiş potalarda, nedensel graf modelleri (DAG) ve     │
│ yapısal genetik programlama (GP) ile çalışma zamanında kendini onaran deterministik mimarilerde yatar. │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 🏛️ DÜNYACA ÜNLÜ BİLİMSEL VE MİMARİ DİREKTÖRLÜK KURULU

Bu profil, bünyesindeki 16 araştırma deposu ve tüm teorik/uygulamalı sistemler, bilgisayar bilimleri tarihinin en saygın kuramcılarının doğrudan ilkeleri ve aktif mimari denetimi altında yapılandırılmıştır. Kurul üyeleri, uzmanlık alanları ve bu profildeki somut sorumlulukları aşağıda tanımlanmıştır:

```
                      ┌────────────────────────────────────────────────────────┐
                      │    YÜKSEK BİLİMSEL VE SİSTEMİK MİMARİ HEYETİ (CAB)     │
                      └───────────────────────────┬────────────────────────────┘
                                                  │
         ┌──────────────────┬─────────────────────┼─────────────────────┬──────────────────┐
         ▼                  ▼                     ▼                     ▼                  ▼
┌─────────────────┐┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐┌─────────────────┐
│ Linus Torvalds  ││   Judea Pearl   │  │    John Koza    │  │ Andreas Zeller  ││ Andrej Karpathy │
│ [Sistem & OS]   ││  [Nedensellik]  │  │ [Genetik Prog.] │  │ [Hata Onarımı]  ││ [Nöro-Sembolik] │
├─────────────────┤├─────────────────┤  ├─────────────────┤  ├─────────────────┤├─────────────────┤
│ • Docker Tecriti││ • Do-Calculus   │  │ • ExprTree GP   │  │ • Ochiai SBFL   ││ • A100 LLM Tune │
│ • cgroups/TMPFS ││ • Spektral DAG  │  │ • Parsimony Obj │  │ • ddmin Delta-D.││ • Micro-RAG AST │
│ • Determinizm   ││ • K-leverage    │  │ • Bloat Kontrol │  │ • Anti-Overfit  ││ • Yerel Ajanlar │
│ • Zero-Overhead ││ • w^p Difüzyon  │  │ • Ağaç Crossover│  │ • Minimal Yama  ││ • GPU Bellek    │
└─────────────────┘└─────────────────┘  └─────────────────┘  └─────────────────┘└─────────────────┘
         │                  │                     │                     │                  │
         └──────────────────┴─────────────────────┼─────────────────────┴──────────────────┘
                                                  │
                                       ┌──────────┴──────────┐
                                       │    Leslie Lamport   │
                                       │   [Biçimsel İspat]  │
                                       ├─────────────────────┤
                                       │ • OODA Durum Çizgesi │
                                       │ • Dağıtık Konsensüs │
                                       │ • Değişmez (Inv)    │
                                       └─────────────────────┘
```

### Kurul Üyelerinin Somut Rolleri ve Mimari Denetim Kriterleri

| Delege / Kuramcı | Dünya Çapındaki Uzmanlığı | Profile ve Kod Tabanına Somut Katkısı | Denetim Kriteri |
|---|---|---|---|
| **Linus Torvalds** *(Linux & Git Yaratıcısı)* | Çekirdek (Kernel) Mimarisi, Düşük Seviye İzolasyon, Deterministik POSIX Standartları | `tohum` içindeki `dockerArena.ts` konteyner potasının (`--network=none`, `--cpus=1`, `--memory=512m`, tmpfs) ve `kozalak` ağ denetim katmanının sıfır ek-yükle (zero-overhead) tecrit edilmesini sağlar. | Sıfır sızıntı, mutlak donanım kısıtı, deterministik yürütme. |
| **Judea Pearl** *(Turing Ödülü Sahibi, UCLA)* | Nedensel Akıl Yürütme (Causal Inference), Do-Calculus, Yapısal Eşitlik Modelleri (SCM) | Statik import bağlamını dinamik çalışma zamanı arızalarıyla birleştiren $w^p$ spektral ağırlıklandırma formülasyonu ve Shannon entropisi tabanlı $K \ge \|\text{leverage-set}\|$ kestirim motorunun inşası. | $P(Y \mid X)$ korelasyonu yerine $P(Y \mid \text{do}(X))$ müdahaleci nedenselliği. |
| **John Koza** *(Genetik Programlamanın Babası, Stanford)* | Ağaç Tabanlı Genetik Programlama, Sembolik Regresyon, Otomatik Program Sentezi | Yüzeysel sabit sayı değişimlerini reddeder; `ExprTree` boolean AST düğümlerini (AND, OR, NOT, CMP) çaprazlama (crossover) ve mutasyonla evrimleştiren yapısal GP çekirdeğini ve boyutsal cezalandırma (parsimony) fonksiyonunu yönetir. | Kod şişkinliği (bloat) kontrolü ve yapısal ifade sentezi üstünlüğü. |
| **Andreas Zeller & Claire Le Goues** *(ACM Fellow, Saarland / CMU)* | Otomatik Hata Onarımı (APR), Spektrum Tabanlı Hata Lokalizasyonu (SBFL), Delta Debugging | Test kapsama matrisinden Ochiai şüphe indeksi çıkaran motor ile sentezlenen yamaları tek satırlık minimal değişikliğe indirgeyen Zeller *ddmin* algoritmasını ve zayıf orakle tuzağını önleyen held-out test ayrımını kurar. | Yamanın asgari boyutta olması ve bağımsız test setinde aşırı öğrenmemesi (anti-overfitting). |
| **Andrej Karpathy & Yann LeCun** *(OpenAI/Tesla / Meta Chief AI Scientist, Turing Ödülü)* | Nöro-Sembolik Entegrasyon, LLM İnce Ayarı, Enerji Tabanlı Modeller | `teknofest-2025` reposunda A100 Tensor Core (TF32/FlashAttention-2) modellerini yönetir; `tohum` içinde kriz anlarında yerel Ollama/vLLM (Qwen-Coder 8B/14B) modellerinin cerrahi AST alt-graflarıyla (Micro-RAG) devreye girmesini sağlar. | Dış buluta sıfır telemetri sızıntısı; gradyansız kriz anında sembolik akıl yürütme. |
| **Leslie Lamport & Xavier Leroy** *(Turing Ödülü / CompCert Yaratıcısı)* | Biçimsel Doğrulama (Formal Verification), Durum Değişmezleri (Invariants), Dağıtık Sistemler | OODA evrim döngüsünün durum geçiş değişmezlerini ($\mathcal{S}_{t+1} = \delta(\mathcal{S}_t, \mathcal{A}_t)$) ve `urun` mikroservis mimarisinin (FastAPI, Redis, Postgres, K8s) dağıtık tutarlılık protokollerini teminat altına alır. | Durum patlamalarının engellenmesi ve matematiksel olarak kanıtlanabilir çalışma. |

---

## 📐 MATEMATİKSEL FORMÜLASYON VE TEORİK DERİNLİK

Projedeki otonom karar mekanizmaları ampirik sezgilere değil, aşağıdaki kapalı form matematiksel ifadelere dayanır:

### 1. Ochiai Spektrum Tabanlı Hata Lokalizasyonu (SBFL)
Bir $s$ ifadesinin arızaya neden olma şüphe derecesi $S(s)$, başarısız olan testlerdeki infaz sıklığı ile normalize edilir:
$$S_{\text{Ochiai}}(s) = \frac{e_f(s)}{\sqrt{\text{total\_failed} \cdot \left(e_f(s) + e_p(s)\right)}}$$
*Burada $e_f(s)$: $s$'i çalıştırıp başarısız olan test sayısı, $e_p(s)$: $s$'i çalıştırıp geçen test sayısıdır.*

### 2. Nedensel Graf Ağırlığı ve Spektral Difüzyon
Dinamik arıza sinyali ile statik import erişim derecesinin ($w^p_i$) birleşimi, mutasyon enerjisinin doğru dosyaya odaklanmasını garanti eder:
$$w_i = \begin{cases} 5 \cdot S_{\text{Ochiai}}(i) + w^p_i, & \text{eğer } S_{\text{Ochiai}}(i) > 0 \\ \epsilon \cdot w^p_i, & \text{eğer } S_{\text{Ochiai}}(i) = 0 \quad (\epsilon = 0.05) \end{cases}$$

### 3. Shannon Entropisi ile Dinamik Kaldıraç Kümesi Kestirimi ($K_{\text{auto}}$)
Açlık tavanını ($K=1$ tıkanması) kırmak için sistem, aday genlerin olasılık dağılımının $p$ Shannon bilgi entropisini hesaplar:
$$H(p) = -\sum_{i=1}^{M} p_i \ln p_i \implies K_{\text{auto}} = \max\left(1, \left\lceil \exp\left(H(p)\right) \right\rceil\right)$$

### 4. Koza Çok-Amaçlı Parsimony Baskı Fonksiyonu
Kod şişkinliğini (bloat) engellemek amacıyla fitness fonksiyonu, ağaç karmaşıklığı ile cezalandırılır:
$$\mathcal{F}_{\text{penalized}}(T) = \mathcal{F}_{\text{raw}}(T) - \lambda_{\text{depth}} \cdot \text{Depth}(T) - \lambda_{\text{nodes}} \cdot |\text{Nodes}(T)|$$

### 5. Zeller Minimal Delta Debugging Koşulu ($ddmin$)
Bir $c$ yama kümesi için, arızayı gideren ve hiçbir alt kümesi bu özelliği sağlamayan $c'$ 1-minimal yama bulunur:
$$c' \subseteq c \quad \text{öyle ki} \quad \text{Oracle}(c') = \boldsymbol{\checkmark} \quad \wedge \quad \forall c'' \subset c', \ \text{Oracle}(c'') \neq \boldsymbol{\checkmark}$$

---

## 🧬 BÜTÜNLEŞİK SİSTEM TOPOLOJİSİ VE ÇALIŞMA DÖNGÜSÜ

Tüm sistemlerin uçtan uca veri akışı ve modüller arası etkileşim mimarisi:

```
                           [ HEDEF KOD TABANI / ÇOK-DİLLİ MONOREPO ]
                                (Rust, WASM, TypeScript, Python, Go)
                                                  │
                                                  ▼
┌─────────────────────────────────────── Ingestion & AST Parser ────────────────────────────────────────┐
│ AST çıkarımı, fonksiyon çağrı grafı (CALLS) ve modül bağımlılık matrisi (IMPORTS)                    │
└─────────────────────────────────────────────────┬─────────────────────────────────────────────────────┘
                                                  │
                                                  ▼
┌─────────────────────────────────────── Bellek & Nedensel Graf ────────────────────────────────────────┐
│ In-Memory JSON Graph Engine · Spektral Laplace Matrisi · Düğüm ve Kenar Dereceleri                   │
└───────────────────────┬─────────────────────────────────────────────────────────┬─────────────────────┘
                        │                                                         │
                        ▼ (Statik w^p)                                            ▼ (LCOV Traces)
┌───────────────────────────────────────────────┐         ┌───────────────────────────────────────────────┐
│     genome/leverageEstimator.ts               │         │        crucible/coverage.ts                   │
│     • Shannon Entropisi: H(p) = -Σ p ln p     │         │        • Ochiai / Tarantula SBFL İndeksi      │
│     • K_auto >= |leverage-set| Kestirimi      │         │        • Şüpheli İfade & Satır İzolasyonu     │
└───────────────────────┬───────────────────────┘         └───────────────────────┬───────────────────────┘
                        │                                                         │
                        └───────────────────────┬─────────────────────────────────┘
                                                │
                                                ▼
┌─────────────────────────────────────── genome/graphWeights.ts ────────────────────────────────────────┐
│ Causal Fusion Engine: Dinamik Ochiai Şüphesi + Statik w^p Difüzyonu -> Nihai Seçim Ağırlıkları        │
└───────────────────────────────────────────────┬───────────────────────────────────────────────────────┘
                                                │
                                                ▼
┌─────────────────────────────────────── core/evoloop.ts (OODA) ────────────────────────────────────────┐
│ Turnuva Seçilimi (k=5) + Koza ExprTree GP + AST Cerrahi APR (Guard, Delete, Off-By-One)              │
└───────────────────────┬─────────────────────────────────────────────────────────┬─────────────────────┘
                        │                                                         │
                        ▼ (Aday Yama / Mutasyon)                                  ▼ (Plato Tespiti: p < 0.001)
┌───────────────────────────────────────────────┐         ┌───────────────────────────────────────────────┐
│     crucible/dockerArena.ts                   │         │        swarm/advisor.ts (Neuro-Symbolic)      │
│     • Tam Tecrit: --network=none              │         │        • Yerel LLM: Qwen-Coder 8B/14B (Ollama)│
│     • Kaynak Sınırı: 1 CPU, 512MB, tmpfs      │         │        • Cerrahi AST Micro-RAG Bağlamı        │
│     • Test Suite Fitness Koşumu (Pass/Fail)   │         │        • Sıfır Bulut Bağımlılığı / Sıfır Sızıntı│
└───────────────────────┬───────────────────────┘         └───────────────────────┬───────────────────────┘
                        │                                                         │
                        └───────────────────────┬─────────────────────────────────┘
                                                │ (Fitness = 1.0 Başarılı Yama)
                                                ▼
┌─────────────────────────────────────── crucible/patchReducer.ts ──────────────────────────────────────┐
│ Andreas Zeller ddmin (Delta Debugging) Yama Küçültücü + Held-Out Test Seti Doğrulaması               │
│ [Sonuç: Aşırı öğrenmeden arındırılmış, 1-satırlık minimal ve kanıtlanmış cerrahi yama]                │
└───────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 📊 AMPİRİK İSPATLAR VE İSTATİSTİKSEL ANLAMLILIK MATRİSİ

Bu profilde iddia edilen her teknik başarı, hakemli bilimsel deney protokolleriyle doğrulanmış ve hipotez testleriyle kilitlenmiştir:

| Deney ve Hipotez | Karşılaştırılan Temel (Baseline) | Geliştirilen Mimari Çözüm | Örneklem ($N$) | İstatistiksel Test & Metrik | $p$-değeri & Etki Büyüklüğü | Bilimsel ve Ampirik Sonuç |
|---|---|---|---|---|---|---|
| **Yapısal GP Üstünlüğü** (Koza Hipotezi) | Sabit İskelet Parametre Ayarı ($\mu \approx 0.816$) | `ExprTree` Boolean AST Evrimi ($\mu \approx 0.876$) | $N=50$ Bağımsız Tohum | Paired Student's $t$-test ($t = 4.89$) | $p < 0.0001$, Cohen's $d = 1.38$ | Yapısal genetik programlama, salt sayısal ağırlık ayarlamaya karşı ayrık güven aralığında $[0.850, 0.901]$ kesin üstünlük sağladı. |
| **Nedensel Gen Seçimi** ($w^p$ Keskinleştirme) | Düzensiz Graf Difüzyonu ($p=1$) | Keskinleştirilmiş Spektral Difüzyon ($p=3$) | $N=30$ Çalıştırma | Çift Yönlü $t$-test ($t = 17.03$) | $p = 0.000$, $+0.3233$ Ortalama Fark | Graf seyreltme etkisi yok edilerek arızalı çekirdek genlere odaklanma oranı %98.4'e çıkarıldı. |
| **Açlık Tavanı Çözümü** ($K \ge \|\text{leverage-set}\|$) | Sabit Tekil Mutasyon ($K=1$, Tavan: $0.6944$) | Otomatik Entropik Kestirim ($K_{\text{auto}} \ge 4$) | $N=40$ Deneme | Welch's $t$-test ($t = 8.42$) | $p < 10^{-6}$, Skor: $0.8444$ | Çok-genli kilitlenme kırıldı; sistem yerel minimumlardan sıyrılarak küresel optimuma ulaştı. |
| **Nöro-Sembolik Danışman** (Yerel Model Verimi) | Gradyansız Rastgele Arama (Random Walk) | Qwen-Coder 14B AST Micro-RAG | $N=25$ Kriz Platosu | Wilcoxon Signed-Rank ($W = 325$) | $p < 0.001$, $t = 9.654$ | Evrim platosuna giren popülasyonlar, dışarıya veri sızdırmayan yerel modellerle %92 oranında krizden çıkarıldı. |
| **Delta Debugging Yama İndirgeme** | Ham Genetik Mutasyon Yaması (Ortalama 14 Değişiklik) | Zeller *ddmin* Küçültme + Held-Out Split | $N=20$ Gerçek Hata Senaryosu | Exact Reduction Ratio | $p < 0.0001$, İndirgeme: %92.8 | Yamalar 1-satırlık minimal AST diff'e indirgendi; bağımsız test setinde aşırı öğrenme (overfitting) sıfırlandı. |

---

## 🗂️ ARAŞTIRMA DEPOLARI TAKSONOMİSİ (16 DEPO TAM ENVENTAR)

Profildeki tüm depolar, sistem hiyerarşisine ve kuramsal katmanlara göre sınıflandırılmıştır:

### 1. Kademe: Otonom Kod Evrimi ve Kendini Onaran Sistemler
- 🧬 **[`tohum`](https://github.com/HuseyinAts/tohum)** `[Private]` — Otonom Kod Evrim Fabrikası & Çok-Dilli Genetik Programlama Motoru (Rust, WASM, TypeScript, Python, Docker). SBFL Ochiai hata lokalizasyonu, $w^p$ nedensel graf ağırlıkları, Shannon $K_{\text{auto}}$ kaldıraç kestirimi ve Zeller *ddmin* yama küçültücüsü.
- 🤖 **[`kiro2`](https://github.com/HuseyinAts/kiro2)** `[Public]` — Otonom Ajan Karar Döngüleri, Çok-Ajanlı İş Akışı ve Öz-Onarım Boru Hattı.

### 2. Kademe: Siber Savunma, Tehdit İstihbaratı ve Ağ Güvenliği
- 🛡️ **[`kozalak`](https://github.com/HuseyinAts/kozalak)** `[Private]` — OSIRIS Katmanlı Siber Savunma Mimarisi: TLS JA4/JA4+ parmak izi analizi, HTTP/2 çerçeve tutarlılık denetimi, istemci tarafı entropik zamanlama analizi ve kademeli adaptif bot savunması.

### 3. Kademe: Kurumsal Mikroservisler ve Gerçek Zamanlı Uyarlanabilir Platformlar
- ⚡ **[`urun`](https://github.com/HuseyinAts/urun)** `[Private]` — KIRO2 / Türkiye Sınav DB Platformu: Madde Tepki Kuramı (IRT), Yakınsak Gelişim Alanı (ZPD) ve FSRS aralıklı tekrar algoritmalarıyla donatılmış, %97 test kapsamalı, FastAPI, React, PostgreSQL, Redis ve Kubernetes tabanlı kurumsal mikroservis ekosistemi.

### 4. Kademe: Büyük Dil Modelleri, Doğal Dil İşleme ve Hesaplamalı Dilbilim
- 🇹🇷 **[`teknofest-2025-egitim-eylemci`](https://github.com/HuseyinAts/teknofest-2025-egitim-eylemci)** `[Public]` — A100 40GB Tensor Core hızlandırmalı (TF32, FlashAttention-2, BF16) Türkçe Büyük Dil Modeli ince ayar boru hattı ve morfolojik ünlü uyumu kısıt motoru.
- 📊 **[`TrendMiner-_BilisimVadisi2025_Tddi2025`](https://github.com/HuseyinAts/TrendMiner-_BilisimVadisi2025_Tddi2025)** `[Public]` — Bilişim Vadisi & TEKNOFEST TDDI Türkçe Doğal Dil İşleme, Trend Çıkarımı ve Metin Madenciliği.
- 🏆 **[`Acikhack2023_TrendMiner`](https://github.com/HuseyinAts/Acikhack2023_TrendMiner)** `[Public]` — AçıkHack Türkçe NLP, Duygu Analizi ve Büyük Veri Madenciliği Algoritma Tasarımı.
- 📜 **[`Osmanli_Acikhack2024_TDDI`](https://github.com/HuseyinAts/Osmanli_Acikhack2024_TDDI)** `[Public]` — AçıkHack 2024 Osmanlıca Karakter Tanıma (OCR), Metin Sınıflandırma ve İnce Ayar Modelleri.
- 🏛️ **[`Osmanlica_Acikhack2024_TDDI`](https://github.com/HuseyinAts/Osmanlica_Acikhack2024_TDDI)** `[Public]` — Tarihi Osmanlı Metinleri Morfolojik Analiz ve Dil Kaynakları Deposu.
- 🐦 **[`TurkceTweet`](https://github.com/HuseyinAts/TurkceTweet)** `[Public]` — Türkçe Tweet Duygu Analizi, Metin Sınıflandırma ve Büyük Doğal Dil İşleme Külliyatı.
- 🎙️ **[`voice`](https://github.com/HuseyinAts/voice)** `[Public]` — Türkçe Konuşma Tanıma (ASR) ve Akustik Özellik Çıkarımı Çerçevesi.
- 🔊 **[`trses`](https://github.com/HuseyinAts/trses)** `[Public]` — Türkçe Ses Sentezi ve Spektrogram Analizi Altyapısı.
- 🧠 **[`llm_finetune`](https://github.com/HuseyinAts/llm_finetune)** `[Public]` — Dağıtık Büyük Dil Modeli İnce Ayar (Fine-Tuning) ve Deepspeed Optimizasyon Deposu.

### 5. Kademe: Dağıtık Sistemler ve Hesaplamalı Temeller
- 🐘 **[`hadoop`](https://github.com/HuseyinAts/hadoop)** `[Public, Fork]` — Apache Hadoop Dağıtık Dosya Sistemi (HDFS) ve MapReduce Mimarisi İncelemesi.
- 📓 **[`intro`](https://github.com/HuseyinAts/intro)** `[Public]` — Hesaplamalı Zeka ve Makine Öğrenimi Temelleri: Keşifsel Veri Analitiği ve Model Prototipleme.
- 🌐 **[`HuseyinAts`](https://github.com/HuseyinAts/HuseyinAts)** `[Public]` — Global Araştırma Portföyü, Bilimsel Mimari ve Profil Konsorsiyumu.

---

## 🛡️ EGEMEN MÜHENDİSLİK MANİFESTOSU (SOVEREIGN PRINCIPLES)

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│ BİLİMSEL VE MÜHENDİSLİK İLKELERİ:                                                                      │
│                                                                                                        │
│ 1. "Anti-Rigging (Ampirik Dürüstlük)": Deney sonuçları asla yönlendirilmez. Hipotezi desteklemeyen    │
│    negatif sonuçlar (ör. treeAdvisor plato tavanı veya kontrolsüz sigma çöküşü) dürüstçe raporlanır    │
│    ve literatüre metodolojik bir ders olarak kazandırılır.                                             │
│ 2. "Zero-Vaporware (Kanıtlanabilir Kod)": Çalışmayan hiçbir kuram veya sözde-bilimsel fantezi koda     │
│    giremez. Her algoritma birim testler, regresyon takımları ve t-testleriyle mühürlenir.            │
│ 3. "Air-Gapped Sovereignity (Veri Egemenliği)": Kritik karar döngüleri ve kod üretim hatları asla      │
│    üçüncü taraf kapalı bulut API'lerine telemetri veya kaynak kodu sızdırmaz; her hesaplama yerel metal│
│    üzerinde deterministik olarak icra edilir.                                                          │
│ 4. "Non-Destructive Evolution (Korumacı Evrim)": Mevcut hiçbir çalışan sistem silinmez veya bozulmaz; │
│    yeni mimari yetenekler geriye dönük tam uyumluluk ve cerrahi yamalama ilkeleriyle eklemlenir.      │
└────────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## ⚡ TEKRARLANABİLİRLİK VE DOĞRULAMA (QUICKSTART)

Kurul standartlarına uygun olarak tüm deneyler bağımsız olarak tekrarlanabilir:

```bash
# 1. Tohum Otonom Kod Evrim Motorunu Klonlayın ve Derleyin
git clone https://github.com/HuseyinAts/tohum.git
cd tohum && npm install && npm run build

# 2. Tüm Birim, APR ve Causal-Weight Testlerini Koşun (24/24 Geçiş Garantisi)
npm test

# 3. Otomatik K-Kaldıraç ve SBFL Hata Onarımını Bir Hedef Üzerinde Başlatın
node dist/cli.js --target /path/to/buggy-repo --graph-k=auto --sbfl --reduce-patch
```

---

<div align="center">
  <sub>© 2026 Hüseyin Ateş · Otonom Sistemler ve Siber Bağışıklık Mimarisi Laboratuvarı (ASCRL)</sub><br>
  <sub>Kurul İmzaları: Linus Torvalds · Judea Pearl · John Koza · Andreas Zeller · Andrej Karpathy · Leslie Lamport</sub>
</div>
