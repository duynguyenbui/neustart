> [!INFO] **Tổng quan**
> Bản tra nhanh ngữ pháp tiếng Đức **A1 → A2**. Mỗi chủ điểm chỉ giữ bản chất, công thức, một ví dụ và một "bẫy" chính; nội dung chi tiết, IPA và bài tập nằm ở các bài học được liên kết cuối mỗi mục.

### 1. Câu cơ bản & Vị trí động từ

Động từ chia là "trái tim" của câu tiếng Đức — vị trí của nó đổi theo loại câu:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    Q{"Loại câu?"}
    Q -->|"Câu trần thuật"| P2["Động từ ở <span style='font-weight:bold'>Vị trí 2</span><br><span style='font-style:italic'>Ich lerne Deutsch.</span>"]
    Q -->|"Trạng ngữ đầu câu"| INV["Vẫn ở <span style='font-weight:bold'>Vị trí 2</span> — chủ ngữ xuống sau động từ<br><span style='font-style:italic'>Heute lerne ich Deutsch.</span>"]
    Q -->|"Ja/Nein-Frage"| P1["Động từ ở <span style='font-weight:bold'>Vị trí 1</span><br><span style='font-style:italic'>Lernst du Deutsch?</span>"]
    Q -->|"W-Frage"| W["W-Wort (1) + Động từ (2) + Chủ ngữ (3)<br><span style='font-style:italic'>Warum lernst du Deutsch?</span>"]
    class Q decision;
    class P2,INV,P1,W node;
```

**Thứ tự trạng ngữ TeKaMoLo:**

```mermaid
flowchart LR
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    T["<span style='font-weight:bold'>Te</span>mporal<br>khi nào"] --> K["<span style='font-weight:bold'>Ka</span>usal<br>tại sao"]
    K --> M["<span style='font-weight:bold'>Mo</span>dal<br>bằng cách nào"]
    M --> L["<span style='font-weight:bold'>Lo</span>kal<br>ở đâu"]
    class T,K,M node;
    class L result;
```

> [!TIP] *Ich fahre [morgen] [wegen des Regens] [mit dem Bus] [zur Arbeit].*

**Phủ định — chọn `kein` hay `nicht`?**

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    V{"Phủ định cái gì?"}
    V -->|"Danh từ (thói quen / sở hữu / không mạo từ)"| KEIN["<span style='font-weight:bold'>kein / keine</span> · chia như ein<br><span style='font-style:italic'>Ich habe kein Auto.</span>"]
    V -->|"Động từ / tính từ / danh từ có der-die-das"| NICHT["<span style='font-weight:bold'>nicht</span> · cuối câu hoặc trước phần bị phủ định<br><span style='font-style:italic'>Ich trinke die Milch nicht.</span>"]
    class V decision;
    class KEIN,NICHT result;
```

> [!CAUTION] **Một câu chỉ một phủ định:** ❌ *Ich habe nicht kein Auto.* — Trả lời câu hỏi phủ định khi thực tế ngược lại → dùng **`doch`**: *Kommst du nicht heute? → **Doch**, ich komme heute!*

**Chi tiết:** [[02_Grammatik/01_A1/03_Der_einfache_Satz_und_die_Verbposition|Câu & Vị trí động từ]] · [[02_Grammatik/01_A1/16_TE_KA_MO_LO__|TeKaMoLo]]

---

### 2. Giống danh từ & Số nhiều

Mọi danh từ đều có giống: `der` (đực) · `die` (cái) · `das` (trung). Nhận biết qua hậu tố — **chỉ là mẹo, không phải quy tắc 100%**:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    G{"Giống danh từ?"}
    G --> DER["<span style='font-weight:bold'>der</span> · Maskulin<br>ngày / tháng / mùa<br><span style='font-style:italic'>-er, -ling, -ismus, -or</span>"]
    G --> DIE["<span style='font-weight:bold'>die</span> · Feminin<br><span style='font-style:italic'>-e, -ung, -heit, -keit, -schaft, -tion, -tät</span>"]
    G --> DAS["<span style='font-weight:bold'>das</span> · Neutrum<br><span style='font-style:italic'>-chen, -lein, -ment, -um</span><br>động từ hóa danh từ: das Essen"]
    class G decision;
    class DER,DIE,DAS node;
```

**Số nhiều luôn dùng `die`**, nhưng đuôi có 5 dạng — phải học theo cặp số ít / số nhiều:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    P{"Số nhiều — luôn die, nhưng thêm đuôi gì?"}
    P --> E["<span style='font-weight:bold'>-e</span> / -e + Umlaut<br>der Tisch, die Tische<br>der Stuhl, die Stühle"]
    P --> N["<span style='font-weight:bold'>-n</span> / -en<br>die Lampe, die Lampen<br>der Student, die Studenten"]
    P --> R["<span style='font-weight:bold'>-er</span> (+ Umlaut)<br>das Buch, die Bücher"]
    P --> K["<span style='font-weight:bold'>không đổi</span><br>der Lehrer, die Lehrer<br>das Mädchen, die Mädchen"]
    P --> S["<span style='font-weight:bold'>-s</span> (từ mượn)<br>das Auto, die Autos"]
    class P decision;
    class E,N,R,K,S node;
```

> [!CAUTION] **Bẫy Dativ số nhiều:** mạo từ `den` **và** danh từ đều thêm `-n` nếu danh từ chưa có `-n`: *mit den Kinder**n***, *in den Häuser**n***.

**Chi tiết:** [[02_Grammatik/01_A1/01_Nomen_und_Artikel|Nomen & Artikel]] · [[02_Grammatik/01_A1/15_Genus_der_Nomen__|Giống danh từ]] · [[02_Grammatik/01_A1/18_Merkhilfen_zum_Genus_der_Nomen__|Mẹo nhận biết giống]] · [[02_Grammatik/01_A1/02_Pluralformen_der_Nomen|Số nhiều]]

---

### 3. Biến cách: Nominativ – Akkusativ – Dativ

Chọn cách theo **câu hỏi đặt được cho danh từ đó**:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    F{"Hỏi bằng câu hỏi nào?"}
    F -->|"Wer / Was?"| N["<span style='font-weight:bold'>Nominativ</span> · chủ thể hành động<br><span style='font-style:italic'>der Mann · ein Buch</span>"]
    F -->|"Wen / Was?"| A["<span style='font-weight:bold'>Akkusativ</span> · vật bị tác động<br><span style='font-style:italic'>den Mann · ein Buch</span>"]
    F -->|"Wem?"| D["<span style='font-weight:bold'>Dativ</span> · người nhận<br><span style='font-style:italic'>dem Mann · dem Sohn</span>"]
    class F decision;
    class N,A,D result;
```

**Bảng mạo từ `der / ein / kein`:**

| Cách | Đực | Trung | Cái | Số nhiều |
| :--- | :--- | :--- | :--- | :--- |
| **Nominativ** | der / ein / kein | das / ein / kein | die / eine / keine | die / — / keine |
| **Akkusativ** | **den / einen / keinen** | das / ein / kein | die / eine / keine | die / — / keine |
| **Dativ** | **dem / einem / keinem** | **dem / einem / keinem** | **der / einer / keiner** | **den…+n** / — / **keinen…+n** |

> [!TIP] **Mẹo:** Akkusativ ("ĂN") chỉ giống đực đổi thành `-n`. Dativ nhớ **M-R-M-N** ("Mẹ Ra Mua Nước"): đực `-m`, cái `-r`, trung `-m`, số nhiều `-n`.

**Đại từ nhân xưng:**

| Ngôi | Nom | Akk | Dat |
| :--- | :--- | :--- | :--- |
| ich | ich | mich | mir |
| du | du | dich | dir |
| er / es | er / es | ihn / es | ihm / ihm |
| sie | sie | sie | ihr |
| wir | wir | uns | uns |
| ihr | ihr | euch | euch |
| sie / Sie | sie / Sie | sie / Sie | ihnen / Ihnen |

**Động từ luôn đi với Dativ** — bẫy kinh điển, không dùng Akkusativ:

| Động từ | Nghĩa | Ví dụ |
| :--- | :--- | :--- |
| helfen | giúp | Ich helfe **dem Mann**. |
| danken | cảm ơn | Ich danke **dir**. |
| gefallen | làm ai thích | Das Buch gefällt **mir**. |
| gehören | thuộc về | Das Auto gehört **meinem Vater**. |
| antworten | trả lời | Ich antworte **dem Lehrer**. |
| glauben | tin | Ich glaube **dir**. |

**Trật tự tân ngữ:**

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    Q{"Trong câu có tân ngữ nào?"}
    Q -->|"2 danh từ"| R1["<span style='font-weight:bold'>Dativ trước Akkusativ</span><br><span style='font-style:italic'>gibt dem Sohn ein Buch</span>"]
    Q -->|"Đại từ + danh từ"| R2["<span style='font-weight:bold'>Đại từ luôn trước danh từ</span><br><span style='font-style:italic'>gibt ihm ein Buch · gibt es dem Sohn</span>"]
    Q -->|"2 đại từ"| R3["<span style='font-weight:bold'>Akkusativ trước Dativ</span><br><span style='font-style:italic'>gibt es ihm</span>"]
    class Q decision;
    class R1,R2,R3 node;
```

**Chi tiết:** [[02_Grammatik/01_A1/04_Der_Akkusativ|Akkusativ]] · [[02_Grammatik/01_A1/05_Der_Dativ|Dativ]] · [[02_Grammatik/01_A1/14_Akkusativ_und_Dativ_im_Vergleich__|So sánh Akk/Dat]] · [[02_Grammatik/01_A1/17_Personalpronomen_im_Akkusativ_und_Dativ__|Đại từ nhân xưng]]

---

### 4. Chia động từ ở thì hiện tại (Präsens)

Công thức: **bỏ đuôi `-en`, lấy thân động từ, thêm đuôi theo ngôi**.

> [!TIP] **Thần chú đuôi: E – ST – T – EN – T – EN** (ich, du, er/sie/es, wir, ihr, sie/Sie).

**3 nhóm cần chỉnh đuôi cho dễ phát âm:**

| Trường hợp | Chỉnh | Ví dụ |
| :--- | :--- | :--- |
| Thân kết thúc `-t, -d, -fn, -chn, -gn` | Thêm `-e-` ở du, er/sie/es, ihr | arbeiten: du arbeit**est**, er arbeit**et** |
| Thân kết thúc `-s, -ß, -z, -x` | du chỉ thêm `-t` | heißen: du heiß**t** |
| Đuôi `-eln, -ern` | ich bỏ `-e-`; wir/sie chỉ thêm `-n` | sammeln: ich **samml**e |

**Động từ mạnh** — đổi nguyên âm **chỉ ở `du` và `er/sie/es`**, các ngôi khác chia bình thường:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    V["Động từ mạnh"] --> A["a &rarr; ä / au &rarr; äu<br><span style='font-style:italic'>fahren &rarr; du fährst</span>"]
    V --> B["e &rarr; i<br><span style='font-style:italic'>sprechen &rarr; du sprichst</span>"]
    V --> C["e &rarr; ie<br><span style='font-style:italic'>sehen &rarr; du siehst</span>"]
    class V,A,B,C node;
```

**4 động từ biến đổi hoàn toàn (bắt buộc thuộc lòng):**

| Ngôi | sein | haben | werden | wissen |
| :--- | :--- | :--- | :--- | :--- |
| ich | **bin** | habe | werde | **weiß** |
| du | **bist** | **hast** | **wirst** | **weißt** |
| er/sie/es | **ist** | **hat** | **wird** | **weiß** |
| wir | **sind** | haben | werden | wissen |
| ihr | **seid** | habt | werdet | wisst |
| sie/Sie | **sind** | haben | werden | wissen |

**Chi tiết:** [[02_Grammatik/01_A1/13_Verbkonjugation_im_Präsens__|Chia động từ]] · [[02_Grammatik/02_A2/12_Unregelmäßige_Verben__|Động từ bất quy tắc]]

---

### 5. Động từ tách (Trennbare Verben)

Động từ tách = **tiền tố + gốc**. Trong câu chính: gốc chia ở vị trí 2, tiền tố bị "đá" **xuống cuối câu**.

```mermaid
flowchart LR
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    INF["<span style='font-weight:bold'>auf|stehen</span>"] --> Q{"Loại câu?"}
    Q -->|"Trần thuật"| S1["Ich <span style='font-weight:bold'>stehe</span> um 6 Uhr <span style='font-weight:bold'>auf</span>."]
    Q -->|"W-Frage"| S2["Wann <span style='font-weight:bold'>stehst</span> du <span style='font-weight:bold'>auf</span>?"]
    Q -->|"Ja/Nein"| S3["<span style='font-weight:bold'>Stehst</span> du heute <span style='font-weight:bold'>auf</span>?"]
    class Q decision;
    class INF,S1,S2,S3 node;
```

> [!TIP] **Phân loại tiền tố:**
> - **Tách:** `ab- an- auf- aus- ein- fern- mit- nach- vor- weg- zu-` → *ankommen, aufstehen, einkaufen*
> - **Không tách:** `be- ver- ent- emp- er- ge- miss- zer-` → *bekommen, verstehen, gefallen*
> - **Tùy từ:** `über- unter- durch-` → *über|setzen* = phiên dịch (tách); *über**sétzen*** = vượt qua (không tách)

> [!CAUTION] **Bẫy:** tiền tố luôn ở **cuối câu**, dù câu dài: *Wir **kaufen** am Wochenende im Supermarkt **ein**.* Trong Perfekt, `ge-` chèn **giữa**: *einkaufen → ein**ge**kauft* (nhưng *verstehen → verstanden*, không có `ge-`).

**Chi tiết:** [[02_Grammatik/01_A1/08_Trennbare_Verben|Động từ tách]]

---

### 6. Modalverben & Imperativ

**Modalverben** — động từ chính luôn ở **dạng nguyên thể, cuối câu**:

```mermaid
flowchart LR
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    S["Chủ ngữ"] --> V["<span style='font-weight:bold'>Modalverb</span><br>chia · vị trí 2"] --> M["Tân ngữ / trạng từ"] --> INF["<span style='font-weight:bold'>Infinitiv</span><br>cuối câu"]
    class S,V,M node;
    class INF result;
```

**Chọn modalverb theo ý muốn diễn đạt:**

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    M{"Ý muốn diễn đạt?"}
    M -->|"Khả năng"| KO["können<br><span style='font-style:italic'>Ich kann schwimmen.</span>"]
    M -->|"Bắt buộc"| MU["müssen<br><span style='font-style:italic'>Ich muss arbeiten.</span>"]
    M -->|"Cho phép / cấm"| DU["dürfen<br><span style='font-style:italic'>Hier darf man nicht rauchen.</span>"]
    M -->|"Lời khuyên"| SO["sollen<br><span style='font-style:italic'>Du sollst mehr schlafen.</span>"]
    M -->|"Muốn"| WO["wollen<br><span style='font-style:italic'>Ich will gehen.</span>"]
    M -->|"Muốn (lịch sự)"| MO["möchten<br><span style='font-style:italic'>Ich möchte einen Tee.</span>"]
    class M decision;
    class KO,MU,DU,SO,WO,MO result;
```

> [!TIP] **2 quy tắc vàng:** `ich = er/sie/es` và **không có đuôi** (*ich kann = er kann*). Số ít đổi nguyên âm: können→a, müssen→u, dürfen→a, wollen→i (sollen, möchten giữ nguyên).

| Ngôi | können | müssen | dürfen | wollen | sollen | möchten |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| ich | kann | muss | darf | will | soll | möchte |
| du | kannst | musst | darfst | willst | sollst | möchtest |
| er/sie/es | kann | muss | darf | will | soll | möchte |
| wir | können | müssen | dürfen | wollen | sollen | möchten |
| ihr | könnt | müsst | dürft | wollt | sollt | möchtet |
| sie/Sie | können | müssen | dürfen | wollen | sollen | möchten |

**Imperativ** — câu mệnh lệnh:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    IMP["Imperativ"] --> DU["<span style='font-weight:bold'>du</span>: bỏ -st, bỏ du<br><span style='font-style:italic'>Mach!</span> · <span style='font-style:italic'>Fahr!</span> (bỏ Umlaut)<br><span style='font-style:italic'>Sprich!</span> (giữ e &rarr; i)<br>thêm -e nếu gốc tận -t/-d/-m/-n: <span style='font-style:italic'>Warte!</span>"]
    IMP --> IHR["<span style='font-weight:bold'>ihr</span>: chia như ihr, bỏ ihr<br><span style='font-style:italic'>Macht!</span>"]
    IMP --> SIE["<span style='font-weight:bold'>Sie</span>: Động từ + Sie<br><span style='font-style:italic'>Machen Sie!</span>"]
    class IMP,DU,IHR,SIE node;
```

**Chi tiết:** [[02_Grammatik/01_A1/09_Modalverben|Modalverben]] · [[02_Grammatik/01_A1/11_Imperativsatz|Imperativ]]

---

### 7. Giới từ (Präpositionen)

**Luôn đi với Akkusativ (FUDOGBE):** `für, um, durch, ohne, gegen, bis, entlang` → *für **den** Vater, ohne Zucker.*

**Luôn đi với Dativ:** `mit, nach, aus, bei, von, zu, seit` → *mit **dem** Zug, nach **der** Arbeit.*

**Phân biệt `nach` / `zu` / `in` — 3 cách nói "đến":**

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    Q{"Nói 'đến' — đi đâu?"} -->|"Thành phố / quốc gia / về nhà"| N["<span style='font-weight:bold'>nach</span> · không mạo từ<br><span style='font-style:italic'>nach Berlin, nach Hause</span>"]
    Q -->|"Người / bác sĩ / trường / cơ quan"| Z["<span style='font-weight:bold'>zu</span> · zum/zur + mạo từ<br><span style='font-style:italic'>zum Arzt, zur Schule</span>"]
    Q -->|"Vào bên trong nơi chốn"| I["<span style='font-weight:bold'>in</span> · mạo từ + cách<br><span style='font-style:italic'>ins Kino, in die Stadt</span>"]
    class Q decision;
    class N,Z,I result;
```

**Giới từ hai chiều** — chọn cách theo câu hỏi:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    W["<span style='font-weight:bold'>9 Wechselpräpositionen</span><br>an, auf, in, über, unter, vor, hinter, neben, zwischen"] -->|"Wo? (vị trí)"| D["<span style='font-weight:bold'>Dativ</span><br>Das Buch liegt <span style='font-weight:bold'>im</span> Regal."]
    W -->|"Wohin? (chuyển động)"| A["<span style='font-weight:bold'>Akkusativ</span><br>Ich lege das Buch <span style='font-weight:bold'>in das</span> Regal."]
    class W node;
    class D,A result;
```

**Giới từ thời gian:**

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    T{"Thời điểm?"} -->|"Giờ"| U["um<br><span style='font-style:italic'>um 7 Uhr</span>"]
    T -->|"Thứ / ngày / buổi"| AM["am<br><span style='font-style:italic'>am Montag, am 1. Mai</span><br>ngoại lệ: in der Nacht"]
    T -->|"Tháng / mùa"| IM["im<br><span style='font-style:italic'>im Juli, im Sommer</span>"]
    T -->|"Khoảng thời gian"| VB["von…bis<br><span style='font-style:italic'>von 8 bis 17 Uhr</span>"]
    T -->|"Từ mốc tương lai"| AB["ab<br><span style='font-style:italic'>ab morgen</span>"]
    T -->|"Trong…nữa"| IN["in<br><span style='font-style:italic'>in zwei Wochen</span>"]
    class T decision;
    class U,AM,IM,VB,AB,IN result;
```

> [!CAUTION] **Bẫy:** học theo **câu hỏi**, không học máy móc theo động từ: *Ich gehe im Park spazieren* (Wo? → Dat) nhưng *Ich gehe in den Park* (Wohin? → Akk).

**Chi tiết:** [[02_Grammatik/01_A1/06_Lokale_Präpositionen|Giới từ nơi chốn]] · [[02_Grammatik/01_A1/07_Temporale_Präpositionen|Giới từ thời gian]]

---

### 8. Perfekt

Công thức: **Chủ ngữ + `haben`/`sein` (vị trí 2) + … + Partizip II (cuối câu)**.

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    V["Chọn trợ động từ"] -->|"Chuyển động / đổi trạng thái / đặc biệt"| SEIN["<span style='font-weight:bold'>sein</span><br>gehen, fahren, kommen, bleiben, werden"]
    V -->|"Có tân ngữ Akk / phản thân / tại chỗ"| HABEN["<span style='font-weight:bold'>haben</span><br>essen, kaufen, lesen, arbeiten, sich freuen"]
    class V node;
    class SEIN,HABEN result;
```

**Cách tạo Partizip II** — quyết định qua 2 bậc:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    START["<span style='font-weight:bold'>Động từ nguyên thể</span><br>lernen, trinken, einkaufen, verstehen"] --> Q1{"Có <span style='font-weight:bold'>tiền tố tách</span>?<br><span style='font-style:italic'>auf-, ein-, an-, mit-…</span>"}
    Q1 -->|"Có"| SEP["<span style='font-weight:bold'>ge- CHÈN GIỮA</span><br>ein|kaufen &rarr; ein<span style='font-weight:bold'>ge</span>kauft"]
    Q1 -->|"Không"| Q1B{"Tiền tố <span style='font-weight:bold'>không tách</span> / -ieren?<br><span style='font-style:italic'>be-, ver-, ent-, er-, ge-…</span>"}
    Q1B -->|"Có"| NOGE["<span style='font-weight:bold'>KHÔNG có ge-</span><br>verstehen &rarr; verstanden<br>studieren &rarr; studiert"]
    Q1B -->|"Không (đơn)"| GE["<span style='font-weight:bold'>ge- + gốc</span><br>machen &rarr; ge<span style='font-weight:bold'>macht</span>"]
    SEP & NOGE & GE --> Q2{"<span style='font-weight:bold'>Quy tắc hay bất quy tắc?</span>"}
    Q2 -->|"Quy tắc &rarr; đuôi <span style='font-weight:bold'>-t</span>"| REG["gemacht · gekauft · eingekauft"]
    Q2 -->|"<span style='font-weight:bold'>BẤT QUY TẮC</span> &rarr; đuôi <span style='font-weight:bold'>-en</span> (gốc đổi)"| IRR["getrunken · gegangen<br>angekommen · verstanden"]
    class Q1,Q1B,Q2 decision;
    class START,SEP,NOGE,GE,REG node;
    class IRR result;
```

**Chi tiết:** [[02_Grammatik/01_A1/10_Perfekt|Perfekt]]

---
### 9. Sở hữu, phản thân & Động từ + giới từ

**Possessivartikel** chia như `ein/kein`. Gốc theo người sở hữu: mein- (tôi), dein- (bạn), sein- (anh ấy/nó), ihr- (cô ấy/họ), unser- (chúng tôi), euer- (các bạn), Ihr- (Ngài).

| Cách | Đực | Trung | Cái | Số nhiều |
| :--- | :--- | :--- | :--- | :--- |
| Nom | mein | mein | meine | meine |
| Akk | meinen | mein | meine | meine |
| Dat | meinem | meinem | meiner | meinen |

> [!CAUTION] `euer` rớt `-e-` khi thêm đuôi: *euer Hund* → *eu**re** Katze*.

**Reflexivverben** — đại từ phản thân:

| Ngôi | Akk | Dat |
| :--- | :--- | :--- |
| ich / du | mich / dich | mir / dir |
| er / sie / es | **sich** | **sich** |
| wir / ihr | uns / euch | uns / euch |
| sie / Sie | **sich** | **sich** |

**Chọn Akkusativ hay Dativ cho đại từ phản thân?**

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    R{"Đã có tân ngữ Akk khác?"}
    R -->|"Không"| A["<span style='font-weight:bold'>Akkusativ</span><br><span style='font-style:italic'>Ich wasche mich.</span>"]
    R -->|"Có (bộ phận cơ thể / vật)"| D["<span style='font-weight:bold'>Dativ</span><br><span style='font-style:italic'>Ich wasche mir die Hände.</span>"]
    class R decision;
    class A,D result;
```

**Động từ + giới từ** — hỏi/trả lời phân biệt Người vs Vật:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    OBJ["Đối tượng"] --> P["<span style='font-weight:bold'>Người</span><br>Hỏi: Giới từ + wen/wem<br>Trả lời: Giới từ + đại từ<br><span style='font-style:italic'>auf wen? &rarr; auf meinen Freund</span>"]
    OBJ --> S["<span style='font-weight:bold'>Vật</span><br>Hỏi: Wo(r) + giới từ<br>Trả lời: Da(r) + giới từ<br><span style='font-style:italic'>worauf? &rarr; darauf</span>"]
    class OBJ,P,S node;
```

| Động từ + giới từ | Cách | Ví dụ |
| :--- | :--- | :--- |
| warten auf | Akk | Ich warte **auf den Bus / darauf**. |
| sich freuen auf / über | Akk | auf = mong (tương lai) · über = vui (đã xảy ra) |
| sich interessieren für | Akk | Er interessiert sich **für Musik**. |
| denken an | Akk | Ich denke **an dich**. |
| sprechen mit / über | Dat / Akk | mit dem Chef · über das Projekt |
| träumen von | Dat | Sie träumt **von einem Haus**. |

**Chi tiết:** [[02_Grammatik/02_A2/01_Possessivartikel|Sở hữu]] · [[02_Grammatik/02_A2/03_Reflexive_Verben_und_Reflexivpronomen|Phản thân]] · [[02_Grammatik/02_A2/02_Verben_mit_Präpositionen|Động từ + giới từ]]

---

### 10. Präteritum, Mệnh đề phụ & Liên từ

**Präteritum** — ưu tiên cho `sein`, `haben`, Modalverben trong kể chuyện / văn viết:

| Ngôi | sein | haben | können | müssen |
| :--- | :--- | :--- | :--- | :--- |
| ich | war | hatte | konnte | musste |
| du | warst | hattest | konntest | musstest |
| er/sie/es | war | hatte | konnte | musste |
| wir | waren | hatten | konnten | mussten |
| ihr | wart | hattet | konntet | musstet |
| sie/Sie | waren | hatten | konnten | mussten |

**Nebensatz** — liên từ phụ thuộc kéo động từ chia **xuống cuối**:

```mermaid
flowchart TD
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    Q{"Mệnh đề nào đứng trước?"}
    Q -->|"Hauptsatz"| A["…, <span style='font-weight:bold'>weil/dass/wenn/als</span> + chủ ngữ + … + <span style='font-weight:bold'>ĐỘNG TỪ CUỐI</span><br><span style='font-style:italic'>Ich bleibe zu Hause, weil ich krank bin.</span>"]
    Q -->|"Nebensatz"| B["<span style='font-weight:bold'>Weil/…</span> + … + động từ cuối, + <span style='font-weight:bold'>động từ chính NGAY SAU dấu phẩy</span><br><span style='font-style:italic'>Weil ich krank bin, bleibe ich zu Hause.</span>"]
    class Q decision;
    class A,B result;
```

| Liên từ | Dùng | Ví dụ |
| :--- | :--- | :--- |
| weil | nguyên nhân | …weil ich in Deutschland arbeiten **möchte**. |
| dass | "rằng" sau sagen/denken/wissen | Er sagt, dass er morgen **kommt**. |
| wenn | khi/nếu (hiện tại/tương lai, lặp lại) | **Wenn** es regnet, **bleibe** ich zu Hause. |
| als | khi (1 lần trong quá khứ) | **Als** ich 10 war, **lebte** ich auf dem Land. |

**Liên từ nối 2 câu chính:**

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    C["Liên từ"] --> ADUSO["<span style='font-weight:bold'>Vị trí 0</span> · không đảo<br>aber, denn, und, sondern, oder<br><span style='font-style:italic'>…, aber ich habe gelernt.</span>"]
    C --> ADV["<span style='font-weight:bold'>Vị trí 1</span> · đảo ngữ<br>deshalb, trotzdem, dann, sonst<br><span style='font-style:italic'>…, deshalb gehe ich zum Arzt.</span>"]
    class C,ADUSO,ADV node;
```

> [!CAUTION] **denn vs weil:** `denn` không đảo, động từ vị trí 2 (*denn ich bin müde*); `weil` kéo động từ về cuối (*weil ich müde bin*).

**Chi tiết:** [[02_Grammatik/02_A2/04_Präteritum_Sein_Haben_und_Modalverben|Präteritum]] · [[02_Grammatik/02_A2/05_Nebensatz_Weil_Dass_Wenn_Als|Mệnh đề phụ]] · [[02_Grammatik/02_A2/06_Satzstellung_mit_Hauptsatzverbindungen|Liên từ nối câu chính]]

---

### 11. Chia đuôi tính từ & So sánh

Tính từ đứng trước danh từ phải thêm đuôi — chọn đuôi theo mạo từ đứng trước:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    ADJ["Tính từ trong câu"] --> Q1{"Đứng ngay trước danh từ?"}
    Q1 -->|"Không (sau sein / werden / bleiben)"| PRED["<span style='font-weight:bold'>NGUYÊN MẪU — không đuôi</span><br><span style='font-style:italic'>Der Hund ist klein.</span>"]
    Q1 -->|"Có"| Q2{"Cái gì đứng ngay trước tính từ?"}
    Q2 -->|"der / die / das<br>(mạo từ xác định)"| W["<span style='font-weight:bold'>CHIA YẾU</span><br>• Nom Sg (M/F/N) & Akk Sg (F/N): <span style='font-weight:bold'>-e</span><br>• Còn lại (Akk M, mọi Dativ, mọi Plural): <span style='font-weight:bold'>-en</span><br><span style='font-style:italic'>der alte Mann · die schöne Frau · den alten Mann · die alten Bücher</span>"]
    Q2 -->|"ein / mein / kein / Ihr...<br>(mạo từ không xác định / sở hữu)"| M["<span style='font-weight:bold'>CHIA HỖN HỢP</span><br>• Nom Sg: M <span style='font-weight:bold'>-er</span> · F <span style='font-weight:bold'>-e</span> · N <span style='font-weight:bold'>-es</span><br>• Akk Sg: M <span style='font-weight:bold'>-en</span> · F <span style='font-weight:bold'>-e</span> · N <span style='font-weight:bold'>-es</span><br>• Mọi Dativ & mọi Plural (keine/meine): <span style='font-weight:bold'>-en</span><br><span style='font-style:italic'>ein alter Mann · eine wichtige Prüfung · mit einem neuen Auto</span>"]
    Q2 -->|"không mạo từ"| S["<span style='font-weight:bold'>CHIA MẠNH</span> (tính từ lấy đuôi der/die/das)<br>• Nom: M <span style='font-weight:bold'>-er</span> · F <span style='font-weight:bold'>-e</span> · N <span style='font-weight:bold'>-es</span> · Pl <span style='font-weight:bold'>-e</span><br>• Akk: M <span style='font-weight:bold'>-en</span> · F <span style='font-weight:bold'>-e</span> · N <span style='font-weight:bold'>-es</span> · Pl <span style='font-weight:bold'>-e</span><br>• Dat: M/N <span style='font-weight:bold'>-em</span> · F <span style='font-weight:bold'>-er</span> · Pl <span style='font-weight:bold'>-en</span><br><span style='font-style:italic'>kalter Tee · frische Milch · mit gutem Wein</span>"]
    class Q1,Q2 decision;
    class ADJ,W,M,S node;
    class PRED result;
```

**Bảng tra nhanh đuôi tính từ (Nominativ – Akkusativ – Dativ):**

| Cách | Giống | Sau mạo từ xác định<br>(*der / die / das*) | Sau mạo từ không xác định<br>(*ein / mein / kein...*) | Không mạo từ<br>(*ohne Artikel*) |
| :--- | :--- | :--- | :--- | :--- |
| **Nominativ** | Đực (M)<br>Cái (F)<br>Trung (N)<br>Số nhiều (Pl) | der alt**e**<br>die klein**e**<br>das neu**e**<br>die alt**en** | ein alt**er**<br>eine klein**e**<br>ein neu**es**<br>keine alt**en** | alt**er**<br>klein**e**<br>neu**es**<br>alt**e** |
| **Akkusativ** | Đực (M)<br>Cái (F)<br>Trung (N)<br>Số nhiều (Pl) | den alt**en**<br>die klein**e**<br>das neu**e**<br>die alt**en** | einen alt**en**<br>eine klein**e**<br>ein neu**es**<br>keine alt**en** | alt**en**<br>klein**e**<br>neu**es**<br>alt**e** |
| **Dativ** | Đực (M)<br>Cái (F)<br>Trung (N)<br>Số nhiều (Pl) | dem alt**en**<br>der klein**en**<br>dem neu**en**<br>den alt**en** (+n) | einem alt**en**<br>einer klein**en**<br>einem neu**en**<br>keinen alt**en** (+n) | alt**em**<br>klein**er**<br>neu**em**<br>alt**en** (+n) |

> [!TIP] **Tính từ đứng sau động từ thì KHÔNG chia đuôi** (không kèm danh từ): *Der Hund ist klein. · Das Auto ist neu.*

> [!TIP] **2 luật vàng (Nominativ/Akkusativ):** Akkusativ **Maskulin → luôn `-en`** bất kể mạo từ (*einen freien Vormittag*, *jeden Tag*, *nächsten Montag*); Nominativ/Akkusativ **Feminin → luôn `-e`** bất kể mạo từ (*eine kurze Rückmeldung*, *nächste Woche*). Chỉ Neutrum trần (`ein`) mới cần `-es`.

> [!TIP] **Mẹo:** mạo từ càng "mạnh" thì tính từ càng "yếu". `der` đã cho biết giống → tính từ chỉ cần `-e`/`-en`; `ein` thiếu thông tin → tính từ phải gánh đuôi `-er/-es`.

**So sánh:**

| Kiểu | Công thức | Ví dụ |
| :--- | :--- | :--- |
| Bằng | `so + Adj + wie` | so groß **wie** du |
| Hơn | `Adj + -er + als` | schneller **als** das Fahrrad |
| Nhất | `am + Adj + -sten` | **am** höchst**en** |

| Bất quy tắc | Komparativ | Superlativ |
| :--- | :--- | :--- |
| gut | besser | am besten |
| viel | mehr | am meisten |
| gern | lieber | am liebsten |
| hoch | höher | am höchsten |
| nah | näher | am nächsten |

> [!CAUTION] **Có danh từ theo sau thì phải chia đuôi:** *der größ**ere** Mann*, *das best**e** Bild* — và **không dùng `am`** trước danh từ: ❌ *am beste Freund* → ✅ *der beste Freund*.

**Chi tiết:** [[02_Grammatik/02_A2/08_Adjektivendungen|Chia đuôi tính từ]] · [[02_Grammatik/02_A2/09_Komparativ_und_Superlativ|So sánh]] · [[02_Grammatik/02_A2/10_Adjektivendungen_im_Komparativ_und_Superlativ|So sánh + chia đuôi]]

---

### 12. Konjunktiv II & Nominalisierung

**Konjunktiv II** — giả định, mong muốn, lịch sự:

| Động từ | ich | du | er/sie/es | wir | ihr | sie/Sie |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| würde + Infinitiv | würde | würdest | würde | würden | würdet | würden |
| haben → hätte | hätte | hättest | hätte | hätten | hättet | hätten |
| sein → wäre | wäre | wärst | wäre | wären | wärt | wären |
| können → könnte | könnte | könntest | könnte | könnten | könntet | könnten |

**3 cách dùng chính:**

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    K{"Mục đích nói?"}
    K -->|"Yêu cầu lịch sự"| P["<span style='font-style:italic'>Könnten Sie mir helfen?</span>"]
    K -->|"Ước muốn"| W["<span style='font-style:italic'>Ich hätte gern einen Tee.</span>"]
    K -->|"Lời khuyên"| A["<span style='font-style:italic'>Du solltest mehr schlafen.</span>"]
    class K decision;
    class P,W,A result;
```

**Nominalisierung** — biến động từ thành danh từ: **viết hoa nguyên thể + `das`**:

```mermaid
flowchart LR
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;
    V["lesen"] --> N["<span style='font-weight:bold'>das Lesen</span><br>việc đọc"] --> E["Dùng như danh từ thường<br>chủ ngữ / tân ngữ / sau giới từ"]
    class V,E node;
    class N result;
```

*Das Lesen hilft mir. · Ich hasse **das Warten**. · Beim (bei dem) Autofahren darf man nicht telefonieren.*

> [!TIP] Chỉ số ít, không có số nhiều: ✅ *das Lesen* · ❌ *die Lesen*.

**Chi tiết:** [[02_Grammatik/02_A2/07_Konjunktiv_II|Konjunktiv II]] · [[02_Grammatik/02_A2/13_Nominalisierung_Verben_als_Substantive__|Nominalisierung]]
