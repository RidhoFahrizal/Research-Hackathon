Berdasarkan poster Hackathon PENS 2026, tiga tema tersebut bukan sekadar tiga sektor bisnis, melainkan tiga problem domain yang dapat diselesaikan dengan teknologi. Karena halaman resmi hackathon yang terindeks publik belum menampilkan deskripsi teknis tiap tema, penjelasan di bawah merupakan interpretasi berbasis judul tema dan literatur akademik/industri yang relevan.

## Ringkasan perbandingan

| Tema                                               | Inti masalah                                                                                  | Calon pengguna/pembeli                                 | Data utama                                                         | Bentuk produk                                                        |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------------ | -------------------------------------------------------------------- |
| Digital Campus Worker                              | Meningkatkan produktivitas pekerja dan layanan operasional kampus                             | Rektorat, biro akademik, IT, fasilitas, dosen, teknisi | Tiket layanan, jadwal, aset, ruangan, staf, IoT                    | Campus operations platform, AI copilot, workforce management         |
| Production Survivability in Entertainment Industry | Membuat produksi film, musik, gim, atau konten tetap efisien dan berkelanjutan                | Production house, studio, agensi, kreator              | Anggaran, jadwal, aset, hak cipta, performa konten, biaya produksi | Production risk platform, rights management, AI production assistant |
| Context Graphs in Customer Success and Sales       | Menghubungkan seluruh konteks pelanggan untuk membantu penjualan dan mempertahankan pelanggan | Tim sales, customer success, support, marketing        | CRM, tiket, kontrak, email, meeting, penggunaan produk, transaksi  | Customer intelligence platform, GraphRAG, next-best-action system    |

---

# 1. Digital Campus Worker

### Makna bisnis

Tema ini dapat dipahami sebagai pembangunan sistem digital yang membantu pekerja kampus mengambil keputusan, mengelola tugas, melayani mahasiswa, dan mengoperasikan fasilitas kampus secara lebih efisien.

“Worker” tidak hanya berarti pegawai administrasi. Dalam konteks kampus, cakupannya bisa meliputi:

* staf akademik dan administrasi;
* dosen;
* teknisi laboratorium;
* petugas fasilitas dan pemeliharaan;
* pustakawan;
* petugas layanan mahasiswa;
* tenaga keamanan;
* student worker atau asisten mahasiswa.

EDUCAUSE bersama AIR, NACUBO, dan CUPA-HR melakukan survei terhadap 1.960 responden untuk meneliti dampak AI terhadap pekerjaan di perguruan tinggi. Laporan tersebut menegaskan bahwa AI tidak hanya memengaruhi pembelajaran mahasiswa, tetapi juga operasi institusi, pekerjaan staf, dan pekerjaan dosen. ([EDUCAUSE][1])

UNESCO IITE menganalisis 36 kasus penerapan teknologi digital di pendidikan dari 11 negara. Area yang dibahas meliputi pengelolaan proses pendidikan, infrastruktur, pengembangan profesional, konten, evaluasi, dan personalisasi jalur belajar. ([UNESCO IITE][2])

### Masalah bisnis yang dapat diangkat

Masalah yang umum terjadi di kampus antara lain:

1. Permintaan layanan tersebar di WhatsApp, email, formulir, dan portal berbeda.
2. Tugas tidak otomatis diarahkan kepada staf yang memiliki kompetensi sesuai.
3. Keluhan mahasiswa sulit dilacak sampai selesai.
4. Pemeliharaan ruangan dan peralatan masih bersifat reaktif.
5. Pengetahuan staf senior tidak terdokumentasi.
6. Jadwal dosen, ruangan, teknisi, dan laboratorium saling bertabrakan.
7. Pimpinan kampus tidak memiliki dashboard operasional yang real-time.

Penelitian mengenai IoT untuk smart campus juga menunjukkan bahwa penggunaan teknologi dapat diarahkan pada pemantauan kualitas udara, energi, keamanan, lingkungan, serta pengelolaan aset. Tantangan utamanya adalah interoperabilitas, skalabilitas, penyimpanan data, dan integrasi perangkat dari berbagai vendor. ([arxiv.org][3])

### Ide produk

#### A. CampusOps AI

Satu platform untuk menerima dan mengatur permintaan layanan kampus.

Contoh alur:

1. Mahasiswa melaporkan AC laboratorium rusak.
2. AI mengklasifikasikan laporan sebagai masalah fasilitas.
3. Sistem menentukan lokasi, prioritas, SLA, dan teknisi yang sesuai.
4. Teknisi menerima tugas.
5. Mahasiswa menerima pembaruan status.
6. Pimpinan melihat waktu penyelesaian dan jumlah masalah berulang.

#### B. AI Assistant untuk staf kampus

Sistem yang dapat:

* membuat ringkasan rapat;
* mencari prosedur akademik;
* menyusun balasan email;
* menjawab pertanyaan berdasarkan SOP;
* membuat laporan otomatis;
* menyarankan prioritas pekerjaan.

#### C. Campus Workforce Scheduler

Sistem untuk mengatur:

* jadwal teknisi;
* ketersediaan ruangan;
* jadwal laboratorium;
* shift petugas;
* kapasitas layanan;
* tugas student worker.

### Data minimum

* `service_ticket`
* `category`
* `location`
* `priority`
* `reported_at`
* `assigned_worker`
* `status`
* `resolved_at`
* `resolution_notes`
* `worker_skill`
* `worker_availability`
* `room`
* `asset`
* `maintenance_history`
* `satisfaction_score`

### KPI bisnis

* waktu respons pertama;
* rata-rata waktu penyelesaian;
* persentase tiket sesuai SLA;
* jumlah tiket yang belum selesai;
* tingkat pemanfaatan pekerja;
* tingkat keluhan berulang;
* kepuasan mahasiswa;
* biaya operasional per permintaan.

### Sumber yang perlu dibaca

* [EDUCAUSE — The Impact of AI on Work in Higher Education](https://www.educause.edu/research/2026/the-impact-of-ai-on-work-in-higher-education) — laporan survei penggunaan AI dalam pekerjaan perguruan tinggi. ([EDUCAUSE][1])
* [UNESCO IITE — Analytical Report on the Use of Advanced ICT/AI for Digital Transformation of Education](https://iite.unesco.org/publications/analytical-report-on-the-use-of-advanced-ict-ai-for-digital-transformation-of-education/) — 36 studi kasus transformasi digital pendidikan. ([UNESCO IITE][2])
* [An IoT System for a Smart Campus](https://arxiv.org/abs/2403.15395) — integrasi IoT untuk lingkungan, energi, dan fasilitas kampus. ([arxiv.org][3])
* [Smart Campus in Higher Education: A Systematic Review](https://www.mdpi.com/2076-3417/16/14/7277) — tinjauan sistematis mengenai IoT, AI, big data, dan distributed computing dalam smart campus. ([mdpi.com][4])

---

# 2. Production Survivability in Entertainment Industry

### Makna bisnis

Istilah “production survivability” bukan istilah baku yang memiliki satu definisi universal. Dalam konteks hackathon, istilah tersebut paling masuk akal ditafsirkan sebagai:

> kemampuan bisnis hiburan untuk tetap memproduksi, mendistribusikan, dan menghasilkan pendapatan secara berkelanjutan meskipun menghadapi biaya tinggi, persaingan perhatian, perubahan teknologi, dan risiko hak cipta.

“Entertainment industry” dapat mencakup:

* film dan serial;
* musik;
* gim;
* animasi;
* live event;
* konten digital;
* iklan dan branded content;
* virtual influencer;
* creator economy.

World Economic Forum menyatakan bahwa generative AI sedang mengubah cara konten dibuat, didistribusikan, dan dikonsumsi. Namun, penerapannya memerlukan tata kelola yang transparan, berorientasi manusia, dan memperhatikan dampak terhadap tenaga kerja kreatif. ([World Economic Forum][5])

Deloitte memperkirakan studio besar masih akan berhati-hati menggunakan AI untuk menghasilkan konten utama. Dalam prediksinya, kurang dari 3% anggaran produksi akan dialokasikan untuk AI content creation, sedangkan sekitar 7% pengeluaran operasional dapat bergeser ke alat AI untuk kontrak, manajemen talenta, perizinan, pemasaran, lokalisasi, dan dubbing. Deloitte juga menilai model video generatif masih menghadapi masalah konsistensi karakter, durasi cerita, kualitas, dan risiko hak kekayaan intelektual. ([Deloitte Insights][6])

Untuk Indonesia, Kemenekraf yang mengutip data BPS melaporkan bahwa ekonomi kreatif mempekerjakan sekitar 27,4 juta pekerja pada 2025, atau sekitar 18,7% dari total tenaga kerja nasional. ([Kemenekraf/Bekraf RI][7])

### Masalah bisnis yang dapat diangkat

1. Produksi film atau konten sering melebihi anggaran.
2. Jadwal produksi terlambat karena perubahan skrip, lokasi, talent, atau aset.
3. Studio sulit memprediksi apakah sebuah konten akan diterima audiens.
4. Hak cipta, lisensi, dan persetujuan penggunaan wajah atau suara tidak terdokumentasi dengan baik.
5. Kreator kesulitan membuat banyak variasi konten untuk berbagai platform.
6. Proses dubbing dan subtitle membutuhkan waktu serta biaya.
7. Konten berkualitas belum tentu memperoleh distribusi dan monetisasi yang baik.
8. Penggunaan AI dapat mempercepat produksi, tetapi menimbulkan masalah etika, orisinalitas, dan kepemilikan karya.

### Ide produk

#### A. Production Risk Copilot

Sistem untuk mendeteksi risiko produksi sejak tahap pra-produksi.

Input:

* anggaran;
* jadwal;
* jumlah adegan;
* jumlah lokasi;
* jumlah kru;
* ketergantungan pada aktor tertentu;
* kebutuhan VFX;
* jumlah revisi;
* biaya perangkat dan rendering.

Output:

* prediksi pembengkakan biaya;
* risiko keterlambatan;
* adegan paling mahal;
* sumber daya yang berpotensi menjadi bottleneck;
* alternatif jadwal dan anggaran.

#### B. AI Rights and Provenance Manager

Sistem untuk mencatat:

* siapa pemilik aset;
* sumber gambar, suara, musik, atau video;
* lisensi yang digunakan;
* masa berlaku lisensi;
* persetujuan talent;
* apakah suatu aset dibuat oleh AI;
* model AI yang digunakan;
* riwayat perubahan aset.

#### C. Content Localization Platform

Platform untuk membantu production house:

* membuat subtitle;
* melakukan dubbing;
* mengadaptasi dialog;
* menyesuaikan konten dengan bahasa lokal;
* memeriksa konsistensi istilah;
* mempertahankan gaya karakter.

#### D. Audience-to-Production Intelligence

Sistem yang menghubungkan data audiens dengan keputusan produksi:

* genre;
* durasi tontonan;
* retention;
* completion rate;
* komentar;
* sentiment;
* demografi;
* platform distribusi;
* biaya akuisisi audiens.

### Data minimum

* metadata proyek;
* skrip dan scene;
* anggaran;
* jadwal;
* data kru;
* daftar aset;
* hak cipta dan lisensi;
* data penggunaan AI;
* biaya produksi;
* performa penayangan;
* data engagement;
* pendapatan;
* data subtitle dan dubbing.

### KPI bisnis

* deviasi anggaran;
* deviasi jadwal;
* biaya per menit konten;
* jumlah revisi;
* persentase aset yang memiliki provenance;
* waktu lokalisasi;
* completion rate;
* retention rate;
* revenue per title;
* return on production cost;
* biaya akuisisi audiens;
* emisi atau konsumsi energi produksi.

### Sumber yang perlu dibaca

* [World Economic Forum — Media, Entertainment and Sport](https://www.weforum.org/publications/industries-in-the-intelligent-age-white-paper-series/media-entertainment-and-sport/) — dampak dan tata kelola generative AI pada industri media dan hiburan. ([World Economic Forum][5])
* [Deloitte — Generative AI and Hollywood](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2025/tmt-predictions-hollywood-cautious-of-genai-adoption.html) — biaya, kesiapan teknologi, risiko IP, dan adopsi AI di studio. ([Deloitte Insights][6])
* [Tsiavos & Kitsios — The Digital Transformation of the Film Industry](https://doi.org/10.1016/j.telpol.2025.103021) — systematic literature review mengenai AI di sepanjang value chain industri film. ([sciencedirect.com][8])
* [Yousefimehr et al. — A Systematic Review for 2019–2025 on Deep Learning Models in the Film Production Industry](https://doi.org/10.1016/j.entcom.2025.101076) — membahas scriptwriting, video generation, video editing, dan music generation. ([ScienceDirect][9])
* [Qi et al. — AI for Sustainable Cultural Industries](https://doi.org/10.3390/su18126117) — penggunaan AI untuk menilai keberlanjutan industri film dan budaya. ([doi.org][10])

---

# 3. Context Graphs in Customer Success and Sales

### Makna bisnis

CRM tradisional biasanya menyimpan data dalam tabel:

* customer;
* contact;
* deal;
* ticket;
* invoice;
* contract.

Namun, data tersebut sering terpisah. Context graph menghubungkan entitas, aktivitas, keadaan, dan hubungan bisnis dalam bentuk graf.

Contoh:

```text
Account
 ├── memiliki Contact
 ├── menggunakan Product
 ├── memiliki Contract
 ├── membuat Support Ticket
 ├── menghadiri Meeting
 ├── mengalami Penurunan Usage
 └── memiliki Risiko Churn
```

Knowledge graph dapat digunakan untuk membangun “360-degree view” pelanggan dengan menggabungkan data internal perusahaan dan data eksternal. Tantangan pentingnya adalah entity resolution, pemetaan skema, dan penyamaan definisi antara data dari berbagai sistem. ([Wiley Online Library][11])

Paper *Context Graphs for Proactive Enterprise Agents* mengusulkan graf relasional yang berubah mengikuti kondisi entitas dan hubungan bisnis. Sistem tersebut memakai:

* delta detection;
* proactivity scoring;
* ranking berdasarkan urgensi dan relevansi;
* LLM untuk menjelaskan alasan rekomendasi.

Dalam tiga studi kasus generik, paper tersebut melaporkan Precision@5 sebesar 0,83, false-positive rate 0,11, dan penurunan waktu menemukan informasi dari 47 menit menjadi kurang dari 30 detik. Hasil ini merupakan hasil eksperimen paper, bukan jaminan performa untuk semua perusahaan. ([arxiv.org][12])

Paper SIGIR 2024 mengenai RAG dan knowledge graph untuk customer service melaporkan peningkatan MRR sebesar 77,6% dibanding baseline. Saat diterapkan pada tim customer service LinkedIn, paper tersebut melaporkan penurunan median waktu penyelesaian isu sebesar 28,6%. ([arxiv.org][13])

Gartner melaporkan bahwa 51% pelanggan yang disurvei bersedia menggunakan asisten GenAI untuk berinteraksi dengan layanan pelanggan. Gartner juga menilai layanan pelanggan akan bergerak dari respons reaktif menuju pencegahan masalah dan penciptaan nilai secara proaktif. ([gartner.com][14])

### Masalah bisnis yang dapat diangkat

1. Data sales, marketing, support, billing, dan product usage terpisah.
2. Satu pelanggan dapat memiliki banyak nama atau ID di sistem yang berbeda.
3. Sales tidak mengetahui masalah yang sedang dialami customer setelah pembelian.
4. Customer success terlambat mengetahui tanda-tanda churn.
5. Manajer sales tidak mengetahui siapa pengambil keputusan sebenarnya.
6. Informasi penting tersembunyi dalam email, meeting, tiket, dan dokumen.
7. AI memberikan rekomendasi tanpa bukti dan tanpa penjelasan.

### Struktur data yang ideal

#### Node

* `Account`
* `Contact`
* `Opportunity`
* `Contract`
* `Product`
* `Feature`
* `SupportTicket`
* `Meeting`
* `Invoice`
* `Campaign`
* `Goal`
* `UsageEvent`

#### Edge

* `works_at`
* `contacts`
* `uses`
* `owns`
* `renewed`
* `blocked_by`
* `mentioned_in`
* `related_to`
* `influenced_by`
* `attended`
* `has_sentiment`
* `has_risk`

Setiap hubungan sebaiknya memiliki:

* timestamp;
* sumber data;
* tingkat keyakinan;
* status;
* riwayat perubahan;
* siapa yang membuat atau memvalidasi hubungan tersebut.

### Ide produk

#### A. Customer Health Graph

Sistem yang menghitung kesehatan pelanggan berdasarkan:

* penurunan penggunaan produk;
* tiket support yang meningkat;
* pembayaran terlambat;
* rendahnya engagement;
* tidak adanya meeting;
* perubahan stakeholder;
* komentar negatif;
* kontrak yang mendekati masa perpanjangan.

#### B. Next-Best-Action Engine

Sistem memberikan rekomendasi:

* hubungi customer;
* tawarkan training;
* eskalasi tiket;
* tawarkan fitur tertentu;
* kirim studi kasus;
* lakukan renewal conversation;
* libatkan account executive atau customer success manager.

Rekomendasi harus disertai alasan, misalnya:

> “Risiko churn meningkat karena penggunaan fitur utama turun 42% selama empat minggu, terdapat tiga tiket terbuka, dan kontrak akan berakhir dalam 60 hari.”

#### C. Sales Account Intelligence

Sistem membantu sales mengetahui:

* siapa stakeholder utama;
* siapa champion;
* siapa pengambil keputusan;
* hubungan antarperusahaan;
* peluang cross-sell;
* riwayat interaksi;
* risiko deal;
* next step yang belum dilakukan.

### KPI bisnis

* conversion rate;
* win rate;
* forecast accuracy;
* sales cycle length;
* renewal rate;
* churn rate;
* net revenue retention;
* expansion revenue;
* waktu penyelesaian tiket;
* customer health precision;
* recall prediksi churn;
* tingkat rekomendasi yang diterima;
* tingkat jawaban AI yang memiliki sumber bukti.

### Sumber yang perlu dibaca

* [Chaudhri et al. — Knowledge Graphs: Introduction, History, and Perspectives](https://doi.org/10.1002/aaai.12033) — dasar knowledge graph dan customer 360. ([Wiley Online Library][11])
* [Xu et al. — Retrieval-Augmented Generation with Knowledge Graphs for Customer Service Question Answering](https://doi.org/10.1145/3626772.3661370) — implementasi KG + RAG untuk customer service. ([arxiv.org][13])
* [Kumar — Context Graphs for Proactive Enterprise Agents](https://arxiv.org/abs/2607.07721) — context graph untuk rekomendasi proaktif dalam enterprise. ([arxiv.org][12])
* [Henna & Kalliadan — Enterprise Analytics Using Graph Database and Graph-Based Deep Learning](https://arxiv.org/abs/2108.02867) — graph analytics untuk CRM B2B dan prediksi sales. ([arxiv.org][15])
* [Gartner — Three Trends Shaping Customer Service](https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-identifies-three-trends-that-will-shape-the-future-of-customer-service) — data adopsi AI dan pergeseran layanan pelanggan ke pendekatan proaktif. ([gartner.com][14])

---

# Rekomendasi tema untuk tim kamu

Dengan latar belakangmu di backend, PostgreSQL, data engineering, machine learning, dan arsitektur AI, urutan yang paling cocok menurut saya:

1. **Context Graphs in Customer Success and Sales**
   Paling kuat untuk menunjukkan kemampuan data engineering, knowledge graph, GraphRAG, entity resolution, prediksi churn, dan sistem rekomendasi.

2. **Digital Campus Worker**
   Lebih mudah divalidasi karena kamu berada di lingkungan kampus. Kamu dapat melakukan wawancara langsung dengan staf, dosen, teknisi, atau mahasiswa. Data sintetis juga mudah dibuat.

3. **Production Survivability in Entertainment Industry**
   Sangat menarik secara bisnis, tetapi membutuhkan pemahaman produksi media, hak cipta, distribusi, audiens, dan workflow kreatif. Tema ini lebih cocok jika anggota tim memiliki latar belakang multimedia, desain, film, musik, atau game.

Jika tujuan utama adalah memenangkan hackathon dengan prototipe yang kuat, saya merekomendasikan **Context Graph untuk customer success dan sales**, tetapi dengan ruang lingkup sempit: satu jenis bisnis, tiga sumber data, dan satu output utama berupa rekomendasi tindakan yang dapat dijelaskan.

[1]: https://www.educause.edu/research/2026/the-impact-of-ai-on-work-in-higher-education?utm_source=chatgpt.com "The Impact of AI on Work in Higher Education"
[2]: https://iite.unesco.org/publications/analytical-report-on-the-use-of-advanced-ict-ai-for-digital-transformation-of-education/?utm_source=chatgpt.com "Analytical Report on the Use of Advanced ICT/AI for Digital Transformation of Education"
[3]: https://arxiv.org/abs/2403.15395?utm_source=chatgpt.com "An IoT system for a smart campus: Challenges and solutions illustrated over several real-world use cases"
[4]: https://www.mdpi.com/2076-3417/16/14/7277?utm_source=chatgpt.com "Smart Campus in Higher Education: A Systematic Review ..."
[5]: https://www.weforum.org/publications/industries-in-the-intelligent-age-white-paper-series/media-entertainment-and-sport/?utm_source=chatgpt.com "Industries in the Intelligent Age White Paper Series"
[6]: https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2025/tmt-predictions-hollywood-cautious-of-genai-adoption.html?utm_source=chatgpt.com "Generative AI and Hollywood"
[7]: https://ekraf.go.id/news-en/indonesias-creative-economy-shows-strong-promise-bps-sector-employs-274-million-workers?utm_source=chatgpt.com "Indonesia’s Creative Economy Shows Strong Promise, BPS: Sector Employs 27.4 Million Workers"
[8]: https://www.sciencedirect.com/science/article/pii/S0308596125001181?utm_source=chatgpt.com "The digital transformation of the film industry: How Artificial ..."
[9]: https://www.sciencedirect.com/science/article/pii/S1875952125001569?utm_source=chatgpt.com "A systematic review for 2019–2025 on deep learning models in the film production industry"
[10]: https://doi.org/10.3390/su18126117?utm_source=chatgpt.com "AI for Sustainable Cultural Industries: A Screenplay-Aware ..."
[11]: https://doi.org/10.1002%2Faaai.12033?utm_source=chatgpt.com "Knowledge graphs: Introduction, history, and perspectives - Chaudhri - 2022 - AI Magazine"
[12]: https://arxiv.org/abs/2607.07721?utm_source=chatgpt.com "Context Graphs for Proactive Enterprise Agents"
[13]: https://arxiv.org/abs/2404.17723?utm_source=chatgpt.com "Retrieval-Augmented Generation with Knowledge Graphs for Customer Service Question Answering"
[14]: https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-identifies-three-trends-that-will-shape-the-future-of-customer-service?utm_source=chatgpt.com "Press Release: Gartner Identifies Three Trends That Will Shape The Future of Customer Service"
[15]: https://arxiv.org/abs/2108.02867?utm_source=chatgpt.com "Enterprise Analytics using Graph Database and Graph-based Deep Learning"
