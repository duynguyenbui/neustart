> [!info] Tổng quan
> Bản tra cứu lý thuyết tổng hợp về **Thời gian (Zeitformen / Tempora)**, **Động từ khuyết thiếu (Modalverben)** và **Thể giả định / Lịch sự (Konjunktiv II)** từ A1 đến A2. 
> 
> Liên quan: [[02_Grammatik/01_A1/13_Verbkonjugation_im_Präsens__|Präsens]] • [[02_Grammatik/01_A1/10_Perfekt|Perfekt]] • [[02_Grammatik/02_A2/04_Präteritum_Sein_Haben_und_Modalverben|Präteritum]] • [[02_Grammatik/01_A1/09_Modalverben|Modalverben]] • [[02_Grammatik/02_A2/07_Konjunktiv_II|Konjunktiv II]] • [[99_Docs/01_Basisgrammatik|Basisgrammatik]]

---

## 1. Cây quyết định chọn Thì trong 3 giây

Xác định nhanh thì và thể thức theo mục đích nói:

```mermaid
flowchart TD
    classDef start fill:transparent,stroke:#2563eb,stroke-width:2px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;

    START["Bạn muốn diễn đạt điều gì?"]
    Q1{"Hành động diễn ra khi nào?"}
    Q2{"Ngữ cảnh & Loại động từ?"}
    Q3{"Có thái độ hoặc mục đích đặc biệt?"}

    P["PRÄSENS (Thì hiện tại)<br>• Ich lerne Deutsch.<br>• Morgen fliege ich."]
    PERF["PERFEKT (Quá khứ hoàn thành)<br>haben / sein + Partizip II<br>• Ich habe gelernt.<br>• Er ist gekommen."]
    PRAT["PRÄTERITUM (Quá khứ đơn)<br>• Ich war krank.<br>• Ich hatte keine Zeit.<br>• Ich musste arbeiten."]
    MOD["KẾT HỢP MODALVERB<br>Modalverb (Vị trí 2) + Verb nguyên thể (Cuối câu)<br>• Ich kann / muss / will lernen."]
    KONJ["KONJUNKTIV II (Thể giả định)<br>• Könnten Sie mir helfen?<br>• Ich hätte gern einen Kaffee.<br>• Wenn ich reich wäre..."]

    START --> Q1
    START --> Q3

    Q1 -->|"Hiện tại / Thói quen / Tương lai gần"| P
    Q1 -->|"Đã xảy ra trong quá khứ"| Q2

    Q2 -->|"Giao tiếp nói / Chat / Email hàng ngày"| PERF
    Q2 -->|"Văn viết hoặc gặp sein, haben, Modalverben"| PRAT

    Q3 -->|"Khả năng / Bắt buộc / Cho phép / Mong muốn"| MOD
    Q3 -->|"Nhờ vả lịch sự / Gọi món / Giả định ngược thực tế"| KONJ

    class START start;
    class Q1,Q2,Q3 decision;
    class P,PERF,PRAT,MOD,KONJ result;
```

---

## 2. Ba thì thời gian cơ bản (Zeitformen)

| Thì | Công thức cốt lõi | Khi nào dùng? | Ví dụ |
| :--- | :--- | :--- | :--- |
| **Präsens**<br>*(Hiện tại)* | Gốc động từ + **e - st - t - en - t - en** | • Hành động đang xảy ra<br>• Thói quen, sự thật hiển nhiên<br>• **Tương lai chắc chắn** (+ mốc thời gian) | *Ich lerne jetzt Deutsch.*<br>*Jeden Tag trinke ich Kaffee.*<br>*Morgen fliege ich nach Berlin.* |
| **Perfekt**<br>*(Quá khứ nói)* | **haben / sein** (Vị trí 2) + ... + **Partizip II** (cuối câu) | • **95% giao tiếp đời thường**: nói chuyện, chat, email cá nhân về việc đã xong | *Ich habe viel gelernt.*<br>*Er ist nach Hause gekommen.* |
| **Präteritum**<br>*(Quá khứ viết)* | Động từ chia ở cột Präteritum (Vị trí 2) | • Báo chí, sách truyện, văn viết học thuật<br>• **Bắt buộc dùng cho `sein`, `haben`, `Modalverben`** thay cho Perfekt | *Gestern war ich krank.*<br>*Ich hatte keine Zeit.*<br>*Ich musste arbeiten.* |

### Sơ đồ chọn trợ động từ cho Perfekt (haben hay sein?)

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef decision fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;

    V["Chọn trợ động từ cho Perfekt"]
    Q{"Đặc điểm của động từ?"}

    SEIN["Dùng trợ động từ SEIN<br>• Di chuyển có hướng (gehen, fahren, kommen)<br>• Đổi trạng thái (aufstehen, einschlafen)<br>• Đặc biệt (sein, bleiben, werden)<br><i>Er ist nach Hause gegangen.</i>"]
    HABEN["Dùng trợ động từ HABEN<br>• Có tân ngữ Akkusativ (kaufen, essen)<br>• Hành động tại chỗ (arbeiten, schlafen)<br>• 100% Động từ phản thân (sich freuen)<br><i>Ich habe Pizza gegessen.</i>"]

    V --> Q
    Q -->|"Chuyển động / Đổi trạng thái / Đặc biệt"| SEIN
    Q -->|"Tân ngữ Akk / Tại chỗ / Phản thân"| HABEN

    class V node;
    class Q decision;
    class SEIN,HABEN result;
```

> [!tip] Cách tạo nhanh Partizip II
> - Động từ thường: **`ge-`** + gốc + **`-t`** (*gemacht*).
> - Động từ tách: **tiền tố** + **`ge-`** + gốc + **`-t / -en`** (*eingekauft, angekommen*).
> - Động từ không tách (*be-, ver-, er-...*) hoặc đuôi `-ieren`: **KHÔNG có `ge-`** (*verstanden, studiert*).

---

## 3. Chuyên đề Modalverben (Động từ khuyết thiếu)

Modalverben bổ sung thái độ, khả năng hoặc sự bắt buộc cho hành động chính.

### 3.1. Bảng ý nghĩa 6 Modalverben & `möchten`

| Động từ | Bản chất | Ngữ cảnh sử dụng | Ví dụ |
| :--- | :--- | :--- | :--- |
| **`können`** | Khả năng | Có năng lực làm gì hoặc hoàn cảnh cho phép | *Ich **kann** schwimmen.* |
| **`müssen`** | Bắt buộc | Phải làm do luật lệ, quy luật, mệnh lệnh khách quan | *Ich **muss** heute arbeiten.* |
| **`dürfen`** | Được phép | Có sự cho phép từ người khác / luật | *Hier **darf** man parken.* |
| **`sollen`** | Bổn phận | Lời dặn dò, yêu cầu từ người thứ ba (bác sĩ, sếp) | *Der Arzt sagt, ich **soll** schlafen.* |
| **`wollen`** | Quyết tâm | Ý muốn chủ quan mạnh mẽ của bản thân | *Ich **will** die B1-Prüfung bestehen.* |
| **`mögen`** | Thích | Thường đi trực tiếp với danh từ | *Ich **mag** Schokolade.* |
| **`möchten`** | Muốn lịch sự | Dùng gọi món, xin hẹn lịch sự (thay cho `wollen`) | *Ich **möchte** einen Termin.* |

> [!caution] Phân biệt `nicht müssen` vs `nicht dürfen`
> - **`nicht müssen`** = Không bắt buộc (làm hay không tùy ý): *Du musst nicht kommen.*
> - **`nicht dürfen`** = **CẤM TUYỆT ĐỐI** (làm là vi phạm): *Du darfst hier nicht rauchen.*

### 3.2. Khung vị từ (Satzklammer) với Modalverb

Trong câu chính, Modalverb chia ở **Vị trí 2**, động từ chính ở **nguyên thể (Infinitiv) đứng cuối câu**:

```mermaid
flowchart LR
    classDef frame fill:transparent,stroke:#2563eb,stroke-width:2px;
    classDef mid fill:transparent,stroke:#475569,stroke-width:1px;

    S["Chủ ngữ<br><b>Ich</b>"]
    V1["Modalverb (Vị trí 2)<br><b>kann</b>"]
    M["Phần giữa câu (Mittelfeld)<br>heute leider nicht"]
    V2["Động từ nguyên thể (Cuối câu)<br><b>kommen</b>"]

    S --> V1
    V1 --> M
    M --> V2

    class S,M mid;
    class V1,V2 frame;
```

---

## 4. Ma trận biến đổi Modalverben: Hiện tại $\rightarrow$ Quá khứ $\rightarrow$ Giả định

Sự chuyển đổi hình thái của Modalverben qua các thì và thể:

```mermaid
flowchart LR
    classDef pres fill:transparent,stroke:#2563eb,stroke-width:1.5px;
    classDef prat fill:transparent,stroke:#d97706,stroke-width:1.5px;
    classDef konj fill:transparent,stroke:#16a34a,stroke-width:2px;

    P["<b>HIỆN TẠI (Präsens)</b><br>können -> kann<br>müssen -> muss<br>dürfen -> darf<br>sollen -> soll"]
    PR["<b>QUÁ KHỨ (Präteritum)</b><br>konnte<br>musste<br>durfte<br>sollte"]
    K["<b>GIẢ ĐỊNH / LỊCH SỰ (Konjunktiv II)</b><br>könnte<br>müsste<br>dürfte<br>sollte"]

    P -->|"BỎ hết Umlaut"| PR
    PR -->|"THÊM lại Umlaut"| K

    class P pres;
    class PR prat;
    class K konj;
```

### Bảng đối chiếu hình thái chia theo ngôi

| Động từ gốc | Hiện tại (Präsens)<br>*(ich / er)* | Quá khứ (Präteritum)<br>*(ich / er)* | Konjunktiv II<br>*(ich / er)* | Sắc thái Konjunktiv II |
| :--- | :--- | :--- | :--- | :--- |
| **`können`** | kann | **konnte** *(đã có thể)* | **könnte** | *liệu có thể...* (thỉnh cầu lịch sự / giả định) |
| **`müssen`** | muss | **musste** *(đã phải)* | **müsste** | *đáng lẽ phải...* (bắt buộc mang tính giả định) |
| **`dürfen`** | darf | **durfte** *(đã được phép)* | **dürfte** | *có lẽ là, chắc là...* (dự đoán dè dặt) |
| **`sollen`** | soll | **sollte** *(đã nên)* | **sollte** | *nên...* (đưa ra lời khuyên tế nhị) |
| **`wollen`** | will | **wollte** *(đã định)* | *(dùng `würde gern`)* | Không dùng *wollte* cho lịch sự vì trùng Präteritum |
| **`mögen`** | mag | **mochte** *(đã thích)* | **möchte** | *muốn một cách lịch sự* (gọi món, xin hẹn) |

> [!tip] Luật vàng chia Modalverb
> Ở cả 3 cột: Ngôi **`ich`** và ngôi **`er/sie/es`** luôn **giống hệt nhau** (*ich kann = er kann; ich musste = er musste; ich könnte = er könnte*).

---

## 5. Thể giả định & Lịch sự (Konjunktiv II)

Konjunktiv II **không phải là thì thời gian**, mà là **thể thức nói giảm - nói tránh, giả định hoặc lịch sự**. Ở A2, tập trung vào **Bộ tứ từ khóa vàng**:

```mermaid
flowchart TD
    classDef node fill:transparent,stroke:#475569,stroke-width:1px;
    classDef result fill:transparent,stroke:#16a34a,stroke-width:2px;

    K["Bộ tứ Konjunktiv II ở A2"]
    W["<b>würden + Infinitiv</b><br>Hầu hết mọi động từ thường<br><i>Ich würde gern reisen.</i>"]
    H["<b>hätte (haben)</b><br>Sở hữu giả định / Gọi món<br><i>Ich hätte gern einen Kaffee.</i>"]
    S["<b>wäre (sein)</b><br>Trạng thái giả định<br><i>Ich wäre gern zu Hause.</i>"]
    M["<b>könnte (können)</b><br>Thỉnh cầu lịch sự / Khả năng<br><i>Könnten Sie mir helfen?</i>"]

    K --> W
    K --> H
    K --> S
    K --> M

    class K node;
    class W,H,S,M result;
```

### Ba ngữ cảnh cốt lõi:
1. **Thỉnh cầu lịch sự & Gọi món:** Thay vì đòi hỏi cộc lốc (*Ich will...*), dùng *„Ich **hätte gern** einen Termin.“* hoặc *„**Könnten** Sie mir helfen?“*.
2. **Giả định trái ngược hiện tại (với „wenn“):** *„Wenn ich reich **wäre**, **würde** ich reisen.“* (Thực tế là chưa giàu).
3. **Lời khuyên tế nhị (với „sollte“):** *„Du **solltest** mehr schlafen.“* (Bạn nên ngủ nhiều hơn).

---

## 6. Năm bẫy tử huyệt cần tránh

| Bẫy sai | Câu sai ❌ | Câu đúng chuẩn ✅ | Giải thích quy tắc |
| :--- | :--- | :--- | :--- |
| **1. Chia cả 2 động từ** | *Ich muss **gehe** nach Hause.* | *Ich muss nach Hause **gehen**.* | Động từ chính luôn ở dạng nguyên thể (Infinitiv) ở cuối câu. |
| **2. Ghép `würde` với Modalverb** | *Ich **würde können** kommen.* | *Ich **könnte** kommen.* | Modalverben đã có dạng Konjunktiv II riêng, tuyệt đối không ghép với `würde`. |
| **3. Dùng `wollte` để nhờ vả** | *Ich **wollte** einen Kaffee.* | *Ich **hätte gern** / **möchte** einen Kaffee.* | `wollte` là quá khứ (*tôi đã định*); lịch sự phải dùng `hätte gern` hoặc `möchte`. |
| **4. Quên bỏ Umlaut ở Präteritum** | *Gestern **müsste** ich arbeiten.* | *Gestern **musste** ich arbeiten.* | `müsste` là giả định; quá khứ sự thật là `musste` (không có dấu hai chấm). |
| **5. Sai vị trí trong mệnh đề phụ** | *..., weil ich **muss** heute arbeiten.* | *..., weil ich heute arbeiten **muss**.* | Trong mệnh đề phụ (`weil, wenn`), Modalverb đã chia đứng ở vị trí chốt chặn cuối cùng. |
