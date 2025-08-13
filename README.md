# CCNA Exam Topics — Packet Tracer Labs & Instructor Slides (v7 / 200‑301)

> Bộ sưu tập **lab Packet Tracer (.pka/.pkt)**, **slide giảng viên (.pptx)** và **tài liệu ôn thi** cho lộ trình **CCNA v7** (ITN → SRWE → ENSA → SRWE‑Bridge). Phù hợp cho **tự học**, **dạy học** và **ôn luyện** chứng chỉ **Cisco CCNA 200‑301**.

<p align="left">
  <a href="https://github.com/thongnguyens/ccna-200-301"><img alt="Repo" src="https://img.shields.io/badge/GitHub-ccna--200--301--packet--tracer--labs-black?logo=github"></a>
  <img alt="License" src="https://img.shields.io/badge/license-Educational%20Use-blue"/>
  <img alt="PRs Welcome" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"/>
</p>

---

## Mục lục

* [Tại sao repo này?](#tại-sao-repo-này)
* [Bắt đầu nhanh](#bắt-đầu-nhanh)
* [Cấu trúc thư mục](#cấu-trúc-thư-mục)
* [Cách sử dụng Packet Tracer](#cách-sử-dụng-packet-tracer)
* [Lộ trình học gợi ý](#lộ-trình-học-gợi-ý)
* [Tài liệu & blueprint 200‑301](#tài-liệu--blueprint-200301)
* [Topics (GitHub About)](#topics-github-about)
* [Đóng góp](#đóng-góp)
* [Giấy phép & bản quyền](#giấy-phép--bản-quyền)
* [Ghi công](#ghi-công)
* [Nhật ký thay đổi](#nhật-ký-thay-đổi)

---

## Tại sao repo này?

* ✅ Gom đủ **labs** theo từng học phần (ITN, SRWE, ENSA, SRWE‑Bridge).
* ✅ Có **Instructor Slides** để ôn tập/bổ trợ lý thuyết.
* ✅ Đính kèm **blueprint đề 200‑301** và tài liệu tham khảo.
* ✅ Tên file/thư mục **chuẩn hóa** → dễ tìm, dễ theo dõi tiến độ.
* ✅ Hỗ trợ **học offline** và **giảng dạy**.

> *Gợi ý:* Thêm ảnh/GIF khi làm lab vào thư mục `assets/` để minh họa trong README.

---

## Bắt đầu nhanh

### Yêu cầu

* **Cisco Packet Tracer** 8.x trở lên (mở `.pka`/`.pkt`).
* **Git** (khuyến nghị cài **Git LFS** để theo dõi file lớn `.pptx`/`.pdf`/`.pka`).

### Cài đặt

```bash
# Bật LFS (một lần trên máy)
sudo apt update && sudo apt install -y git-lfs || true
git lfs install

# Bật theo dõi file lớn (khuyến nghị)
git lfs track "*.pka" "*.pkt" "*.pptx" "*.pdf"

echo "*.pka filter=lfs diff=lfs merge=lfs -text" >> .gitattributes
echo "*.pkt filter=lfs diff=lfs merge=lfs -text" >> .gitattributes
echo "*.pptx filter=lfs diff=lfs merge=lfs -text" >> .gitattributes
echo "*.pdf filter=lfs diff=lfs merge=lfs -text"  >> .gitattributes

git add .gitattributes
```

```bash
# Clone repo (nếu chưa ở trong thư mục dự án)
git clone https://github.com/thongnguyens/ccna-200-301.git
cd ccna-200-301-packet-tracer-labs
```

### Sử dụng nhanh

* Mở **Packet Tracer** → `File → Open` một file `.pka`/`.pkt` trong thư mục `labs/` và bắt đầu.
* Mở slide trong `slides/` để ôn lý thuyết trước/đồng thời với lab.

> Nếu bạn *fork* repo, hãy giữ nguyên cấu trúc để CI/Docs hoạt động nhất quán.

---

## Cấu trúc thư mục

```text
ccna-200-301-packet-tracer-labs/
├─ labs/
│  ├─ s1-itn/                # Lab Introduction to Networks (≈ 31 .pka, 2 .pkt)
│  ├─ s2-srwe/               # Lab Switching, Routing & Wireless Essentials (≈ 31 .pka)
│  ├─ s3-ensa/               # Lab Enterprise Networking, Security & Automation (≈ 29 .pka)
│  └─ s4-srwe-bridge/        # Lab tổng hợp SRWE‑Bridge (≈ 7 .pka)
├─ slides/
│  ├─ se1-itn/               # 17 .pptx
│  ├─ se2-srwe/              # 16 .pptx
│  ├─ se3-ensa/              # 14 .pptx
│  └─ se4-srwe-bridge/       # 4  .pptx
├─ docs/
│  └─ 200-301-exam-topics.pdf   # Blueprint chính thức
├─ refs/
│  ├─ ccna-200-301-vol2.pdf
│  └─ ccna-200-301-official-cert-guide.pdf
├─ assets/                      # Ảnh/GIF demo (tùy chọn)
└─ README.md
```

> **Lưu ý:** Không dùng ký tự `/` trong tên thư mục; tuân theo *kebab-case* để tránh lỗi trên IDE/HĐH.

---

## Cách sử dụng Packet Tracer

* **`.pka` (Activity):** có bản mô tả yêu cầu + tiêu chí chấm; dùng tab **Assessment Items / Check Results** để xem điểm.
* **`.pkt` (Topology):** mô phỏng thuần; tự cấu hình theo mô tả trong sơ đồ.
* **Lưu tiến độ:** `Save As` theo quy ước ở trên và commit vào nhánh của bạn.

> *Tip:* Bật `Realtime/Simulation` để quan sát gói tin, hữu ích khi debug ACL/NAT/STP/OSPF.

---

## Lộ trình học gợi ý

1. **S1 – ITN:** mạng căn bản, subnetting, VLAN, router cơ bản.
2. **S2 – SRWE:** switching, STP, EtherChannel, VLAN nâng cao, DHCP.
3. **S3 – ENSA:** OSPF (SS/MD), ACL, NAT/PAT, WAN, QoS, bảo mật căn bản, automation.
4. **S4 – SRWE‑Bridge:** bài tổng hợp, luyện kỹ năng thiết kế & triển khai.
5. Đối chiếu **blueprint 200‑301** trong `docs/` để xác định phần trọng tâm.

---

## Tài liệu & blueprint 200‑301

* **Blueprint:** `docs/200-301-exam-topics.pdf` (đề cương chính thức).
* **Tài liệu tham khảo:** `refs/ccna-200-301-vol2.pdf`, `refs/ccna-200-301-official-cert-guide.pdf`.

> Khuyến nghị song hành: làm lab theo thứ tự module → đọc slide tương ứng → so với blueprint → ghi chú kiến thức còn yếu.

---

## Topics (GitHub About)

Thêm *topics* để repo dễ được tìm thấy. Dùng **GitHub CLI**:

```bash
gh repo edit thongnguyens/ccna-200-301 \
  --add-topic ccna \
  --add-topic cisco \
  --add-topic packet-tracer \
  --add-topic networking \
  --add-topic labs \
  --add-topic itn \
  --add-topic srwe \
  --add-topic ensa \
  --add-topic 200-301 \
  --add-topic study-notes
```

> Hoặc thêm thủ công trong **About → Topics**.

---

## Đóng góp

1. *Fork* repo → tạo nhánh `feat/<ten>` hoặc `docs/<ten>`.
2. Commit theo **Conventional Commits** (ví dụ `feat(labs): add s3-ensa ospf area0`).
3. Với PR thêm lab/slides: mô tả nội dung, cách kiểm thử; đính kèm ảnh/GIF (nếu có).
4. Issues: dùng nhãn `lab`, `slides`, `docs`, `bug`, `good-first-issue`.

### Gợi ý .gitattributes (LFS)

Thêm file `.gitattributes` ở gốc để theo dõi file lớn:

```gitattributes
*.pka filter=lfs diff=lfs merge=lfs -text
*.pkt filter=lfs diff=lfs merge=lfs -text
*.pptx filter=lfs diff=lfs merge=lfs -text
*.pdf  filter=lfs diff=lfs merge=lfs -text
```

---

## Giấy phép & bản quyền

* Repo dùng cho **mục đích giáo dục/cá nhân**. Tên sản phẩm/thương hiệu và tài liệu tương ứng có thể thuộc bản quyền của chủ sở hữu (ví dụ **Cisco**, **Cisco Networking Academy**).
* Nếu bạn là chủ sở hữu nội dung và muốn điều chỉnh việc sử dụng, vui lòng mở **Issue** hoặc liên hệ qua **Email** trong profile.

---

## Ghi công

* **Cisco Networking Academy** – nguồn lab & cảm hứng học liệu.
* Cộng đồng NetAcad/CCNA – chia sẻ kinh nghiệm, mẹo luyện thi.

---

## Nhật ký thay đổi

* **v0.1.0** – Khởi tạo: bổ sung labs S1–S4, slides SE1–SE4, blueprint & tài liệu tham khảo; chuẩn hóa cấu trúc thư mục.
