# ☁️ AWS SAA 80/20 Learning Roadmap

**Lộ trình tự học AWS Solutions Architect Associate dành cho .NET Backend Developer.**

Thiết kế theo nguyên lý 80/20: tập trung 20% kiến thức tạo 80% giá trị thực tế. Core trước, certification sau.

> **Đặc điểm**: Agent-powered · Scaffold-based · Hands-on focused · Learning Science integrated

---

## 📌 Tổng Quan

| Mục | Chi tiết |
|-----|----------|
| Đối tượng | .NET Backend Developer muốn học AWS |
| Phương pháp | 80/20 · Scaffold · Active Recall · Spaced Repetition |
| Triết lý | Core First — nền móng vững, chứng chỉ là kết quả tự nhiên |
| Tổng bài | 69 bài (34 + 20 + ~15) |
| Estimated | ~18-20 tuần (Phase 1+2) · Thêm 4-6 tuần nếu thi cert |
| Công cụ | AI Agent (Antigravity / Gemini) + AWS Free Tier |

---

## 🏗️ Kiến Trúc Hệ Thống

```
aws_saa_8020_learning_roadmap/
│
├── .gemini/rules/
│   └── aws-saa-learning.md            ← 🧠 Rule Engine (15 sections)
│                                         Methodology, template, learning science,
│                                         session protocol, progress rules
│
└── aws-saa/
    ├── README.md                       ← 📖 Bạn đang đây
    ├── progress.md                     ← 📊 Progress tracker + streak + budget
    ├── notes.md                        ← 📝 Insights, weak points, session log
    ├── glossary.md                     ← 📖 Từ điển AWS ↔ .NET (xây dần)
    │
    ├── phase-1-core-foundation/        ← Phase 1: 34 bài · 8 tuần
    │   ├── README.md                      Lesson map + dependency graph
    │   └── lessons/                       Bài đã học (auto-saved)
    │       └── bai-XX.md
    │
    ├── phase-2-architect-thinking/     ← Phase 2: 20 bài · 6 tuần
    │   ├── README.md                      Lesson map
    │   └── lessons/
    │
    └── phase-3-cert-booster/           ← Phase 3: ~15 bài · 4-6 tuần
        ├── README.md                      Lesson outline
        └── lessons/
```

---

## 🔄 Cách Hoạt Động

### Just-in-Time Rendering

Hệ thống **không pre-generate** 69 bài. Thay vào đó:

```
Bạn: "bài tiếp theo"
    │
    ▼
Agent đọc progress.md → biết bài hiện tại
    │
    ▼
Agent đọc phase-X/README.md → lấy metadata bài
    │
    ▼
Agent đọc rules → áp dụng methodology + template
    │
    ▼
🔁 Recall Checkpoint (quiz bài cũ)
    │
    ▼
📘 Render bài mới (theory + practice + self-check)
    │
    ▼
Bạn: "hoàn thành" → Agent cập nhật progress + save lesson
```

### Flow một buổi học

```
┌─────────────────────────────────────────────────┐
│  1. Session Start                               │
│     Agent đọc progress → chào + status summary  │
│     Nếu nghỉ >7 ngày → warm-up quiz            │
├─────────────────────────────────────────────────┤
│  2. Recall Checkpoint (từ bài 02 trở đi)        │
│     • 2-3 câu Active Recall bài trước           │
│     • 1-2 câu Spaced Recall bài cũ hơn          │
│     • 1 câu Bridge vào bài mới                  │
├─────────────────────────────────────────────────┤
│  3. Bài học mới                                 │
│     📖 Lý thuyết (storytelling, .NET bridge)    │
│     🧠 Memory Anchor (metaphor/visual)          │
│     💡 Ví dụ thực tế (scenario-driven)          │
│     🔧 Thực hành (step-by-step, cost-aware)     │
│     ✅ Self-Check (active recall)               │
├─────────────────────────────────────────────────┤
│  4. Hoàn thành (CHỈ khi bạn nói "hoàn thành")  │
│     → Self-assessment (1-5 ⭐)                  │
│     → Auto-save lesson → file                   │
│     → Update progress + glossary + notes         │
│     → Preview bài tiếp theo                     │
└─────────────────────────────────────────────────┘
```

> ⚠️ **Progress chỉ được cập nhật khi bạn nói `"hoàn thành"` / `"done"` / `"xong"`.**
> Agent không tự động đánh dấu bài là done.

---

## 📊 3 Phase

### Phase 1 — Core Foundation (34 bài · 8 tuần)

> 8 services cốt lõi. Nắm chắc phase này = 80% giá trị thực tế.

| Module | Bài | Nội dung |
|--------|-----|----------|
| 1. AWS Mental Model | 01-03 | Cloud fundamentals, Global Infrastructure, Account Setup |
| 2. IAM | 04-08 | Users, Policies JSON, Roles, Advanced, LAB |
| 3. EC2 | 09-13 | Instance types, Networking, EBS, Pricing, LAB Deploy .NET |
| 4. VPC | 14-18 | Subnets, Gateways, SG vs NACL, Connectivity, LAB |
| 5. S3 | 19-22 | Buckets, Security, Lifecycle, LAB .NET SDK |
| 6. RDS & DynamoDB | 23-26 | SQL, NoSQL, Selection patterns, LAB |
| 7. Lambda & Messaging | 27-31 | Lambda, API GW, SQS, SNS, LAB Serverless API |
| 8. CloudWatch & Cost | 32-34 | Monitoring, Cost optimization, Architecture Challenge |

### Phase 2 — Architect Thinking (20 bài · 6 tuần)

> Từ "biết dùng service" → "thiết kế hệ thống".

| Module | Bài | Nội dung |
|--------|-----|----------|
| ELB & Auto Scaling | 01-04 | ALB, NLB, ASG, LAB |
| CloudFront & Route 53 | 05-07 | CDN, DNS, LAB |
| ECS/EKS | 08-11 | Docker, Fargate, LAB Deploy .NET |
| Security Deep Dive | 12-14 | KMS, Secrets Manager, WAF |
| Well-Architected | 15-17 | 6 Pillars, DR Strategies |
| Capstone | 18-20 | Design, Implement, Review |

### Phase 3 — Cert Booster (~15 bài · khi quyết định thi)

> Fill gap + luyện đề. Chỉ kích hoạt khi cần.

---

## ⌨️ Lệnh

### Học tập

| Lệnh | Mô tả |
|-------|-------|
| `bài X` / `lesson X` | Render bài số X |
| `bài tiếp theo` / `next` | Bài kế tiếp chưa hoàn thành |
| `hoàn thành` / `done` / `xong` | ✅ Đánh dấu bài done + cập nhật progress |
| `tạm dừng` / `pause` | Lưu vị trí, end session |
| `lab` | Chỉ phần thực hành của bài hiện tại |

### Ôn tập

| Lệnh | Mô tả |
|-------|-------|
| `review bài X` | Ôn bài X bằng Active Recall |
| `quiz` | Quiz mix từ tất cả bài đã học |
| `quiz module X` | Quiz chỉ module X |
| `weekly review` / `ôn tuần` | Tổng ôn cả tuần |
| `weak points` | Xem concepts cần ôn lại |

### Tra cứu

| Lệnh | Mô tả |
|-------|-------|
| `tiến độ` / `progress` | Dashboard tiến độ visual |
| `glossary [term]` | Tra thuật ngữ AWS ↔ .NET |
| `notes` | Xem/thêm ghi chú cá nhân |
| `so sánh A vs B` | So sánh 2 services |
| `vẽ architecture` | Vẽ architecture diagram |

---

## 🧠 Learning Science

Hệ thống tích hợp 11 kỹ thuật dựa trên nghiên cứu khoa học:

| Kỹ thuật | Nguyên lý | Cách áp dụng |
|----------|-----------|-------------|
| **Pre-lesson Recall** | Testing Effect | Quiz bài cũ TRƯỚC khi học bài mới |
| **Active Recall** | Retrieval Practice | Hỏi → chờ trả lời → confirm |
| **Spaced Repetition** | SM-2 Algorithm | Ôn lại ở khoảng cách 1→3→7→14 bài |
| **Interleaving** | Interleaving Effect | Mix câu hỏi nhiều bài |
| **Elaborative Interrogation** | Chi et al. | Luôn hỏi "Tại sao?" |
| **Dual Coding** | Paivio 1986 | Diagram + Memory Anchor metaphor |
| **Storytelling** | Stanford Research | Dạy bằng scenario, không liệt kê |
| **Chunking** | Miller's Law | Tối đa 3-4 concepts/bài |
| **Feynman Technique** | Richard Feynman | "Giải thích bằng 3 câu" |
| **Emotion Anchoring** | Emotional Memory | "Tại sao BẠN cần biết?" |
| **.NET Bridge** | Prior Knowledge | Map AWS → .NET concepts quen thuộc |

### Spaced Repetition Schedule

```
Bài N → Self-Check (ngay) → Recall ở N+1 → N+3 → N+7 → N+14 → Module LAB → Phase Review
```

---

## 🎯 Scaffolding — Tại sao thứ tự này?

Mỗi module xây trên module trước:

```
Mental Model → hiểu "tại sao"
    └→ IAM → control permissions (cần account)
        └→ EC2 → compute (cần IAM roles)
            └→ VPC → network architecture (cần EC2 basics)
                └→ S3 → storage (cần IAM policies)
                    └→ RDS/DynamoDB → database (cần VPC private subnet)
                        └→ Lambda/SQS/SNS → serverless (cần IAM roles)
                            └→ CloudWatch/Cost → monitor everything
```

Mỗi module theo pattern: **Theory × 3-4 bài → LAB tổng hợp**

---

## 🚀 Bắt Đầu

### Prerequisites

- [ ] AWS Account (Free Tier)
- [ ] AWS CLI v2 installed
- [ ] .NET SDK 8+
- [ ] AI Agent workspace mở tại thư mục project này

### Bước đầu tiên

```
Bạn: "bài 1"
```

Agent sẽ render Bài 01: Tại sao Cloud? Tại sao AWS? — bài đầu tiên trong lộ trình.

---

## 📁 Các File Quan Trọng

| File | Vai trò | Ghi chú |
|------|---------|---------|
| `.gemini/rules/aws-saa-learning.md` | Rule Engine | 15 sections, governs mọi interaction |
| `progress.md` | Progress tracker | Chỉ update khi nói "hoàn thành" |
| `notes.md` | Knowledge base | Insights, weak points, session log |
| `glossary.md` | Từ điển | AWS ↔ .NET, xây dần |
| `phase-X/README.md` | Lesson map | Metadata + dependency graph |
| `phase-X/lessons/bai-XX.md` | Bài đã học | Auto-saved khi "hoàn thành" |

---

## 📜 Rule Engine (15 Sections)

Rule file (`.gemini/rules/aws-saa-learning.md`) điều khiển toàn bộ hệ thống:

| # | Section | Chức năng |
|---|---------|----------|
| 1 | Lesson Rendering Protocol | Quy trình render bài |
| 2 | Lesson Template | Cấu trúc mỗi bài |
| 3 | Teaching Principles | Scaffolding, .NET Bridge, 80/20, Cost, Accuracy |
| 4 | Q&A Protocol | Cách xử lý câu hỏi |
| 5 | Progress Tracking | **Chỉ update khi có lệnh "hoàn thành"** |
| 6 | Difficulty Adaptation | Tự điều chỉnh độ khó |
| 7 | File References | Map tất cả files |
| 8 | Safety Rules | Security best practices |
| 9 | Learning Science | 11 kỹ thuật khoa học |
| 10 | Session Management | Continuity giữa sessions |
| 11 | Lesson Archiving | Auto-save bài đã học |
| 12 | Notes & Knowledge | Weak points, glossary |
| 13 | Gamification | Streak, milestones, badges |
| 14 | Weekly Review | Protocol ôn tuần |
| 15 | Complete Commands | Bảng lệnh đầy đủ |

---

## License

MIT — Tự do sử dụng và tùy chỉnh cho mục đích cá nhân.
