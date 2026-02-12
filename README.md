# lila-sprachschule.de
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lộ Trình Du Học Nghề Đức - Lila</title>

<style>
:root {
  --primary: #6a3fb5;
  --primary-light: #6a3fb5;
  --background: #ffffff;
  --card-bg: #ffffff;
  --text-dark: #1f1f2e;
}

* { box-sizing: border-box; }

html {
  -webkit-text-size-adjust: 100%;
  hyphens: none;
}

body {
  font-family: "Segoe UI", Arial, sans-serif;
  background: var(--background);
  margin: 0;
  padding: 0;
  color: var(--text-dark);
  font-size: 16px;
  overflow-x: hidden;
}

.cost {
  color: var(--primary);
  font-weight: 700;
  white-space: nowrap;
}

.footer strong {
  white-space: nowrap;
}

.node,
.node span,
.node strong {
  word-break: normal;
  overflow-wrap: anywhere;
}

.cover {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 24px;
  background: var(--primary);
  color: white;
}

.brand {
  font-size: 2.3rem;
  font-weight: 700;
  margin-bottom: 15px;
  letter-spacing: 1px;
}

.cover h1 { font-size: 1.5rem; margin-bottom: 10px; }
.cover p { font-size: 1rem; opacity: .9; }

.start-btn {
  margin-top: 30px;
  padding: 14px 26px;
  border: none;
  background: white;
  color: var(--primary);
  border-radius: 30px;
  cursor: pointer;
  font-size: 1rem;
  font-weight: 600;
  box-shadow: 0 8px 22px rgba(0,0,0,0.25);
  transition: all .3s ease;
}

.start-btn:hover { transform: translateY(-2px); }

.section { padding: 30px 16px 60px 16px; }

.node {
  width: 100%;
  padding: 16px 18px;
  margin: 12px 0;
  border-radius: 18px;
  background: var(--card-bg);
  box-shadow: 0 8px 24px rgba(75,46,131,0.08);
  cursor: pointer;
  font-size: 1rem;
  transition: all .3s ease;
  position: relative;
  line-height: 1.55;
}

.node:hover { transform: translateY(-2px); }

.main-node {
  font-weight: 700;
  font-size: 1.15rem;
  color: var(--primary);
  background: linear-gradient(135deg,#ffffff,#f3effc);
}

.clickable-title { font-weight: 700; color: var(--primary); }

.hint {
  font-size: 0.75rem;
  color: #aaa;
  font-weight: 400;
  margin-left: 6px;
}

.children {
  margin-left: 14px;
  max-height: 0;
  overflow: hidden;
  transition: max-height .45s ease, opacity .3s ease;
  opacity: 0;
}

.children.open {
  max-height: 3000px;
  opacity: 1;
}

.node[onclick]::after {
  content: "›";
  position: absolute;
  right: 18px;
  top: 50%;
  transform: translateY(-50%) rotate(0deg);
  font-size: 1.2rem;
  color: var(--primary);
  transition: transform .3s ease;
}

.node.active::after {
  transform: translateY(-50%) rotate(90deg);
}

.footer {
  text-align: center;
  padding: 40px 15px;
  font-size: 0.9rem;
  color: #777;
  background: #ffffff;
}

@media (max-width: 768px) {
  body { font-size: 15px; }
  .brand { font-size: 1.8rem; }
  .cover h1 { font-size: 1.25rem; }
  .node { font-size: 0.95rem; }
}
</style>

<script>
function toggle(id) {
  var el = document.getElementById(id);
  var parentNode = el.previousElementSibling;

  if (el.classList.contains("open")) {
    el.classList.remove("open");
    parentNode.classList.remove("active");
  } else {
    var siblings = el.parentElement.querySelectorAll(":scope > .children");
    siblings.forEach(function(sib){
      sib.classList.remove("open");
      if(sib.previousElementSibling){
        sib.previousElementSibling.classList.remove("active");
      }
    });

    el.classList.add("open");
    parentNode.classList.add("active");
  }
}

function start() {
  document.getElementById("mainContent").scrollIntoView({behavior: "smooth"});
}
</script>
</head>

<body>

<div class="cover">
  <div class="brand">Lila Sprachschule</div>
  <h1>LỘ TRÌNH DU HỌC NGHỀ TẠI ĐỨC - 2026</h1>
  <p>Hệ thống tư vấn & triển khai Ausbildung tại Đức – since 2011</p>
  <button class="start-btn" onclick="start()">Xem chi tiết</button>
</div>

<div id="mainContent" class="section">

<div class="node main-node" onclick="toggle('giaiDoanVN')">
I. Giai đoạn tại Việt Nam
</div>
<div class="children" id="giaiDoanVN">

  <div class="node" onclick="toggle('hocTieng')">
    <span class="clickable-title">Học tiếng Đức (Tối thiểu B1)</span>
    <span class="hint">Chạm để mở</span>
  </div>
  <div class="children" id="hocTieng">
    <div class="node">A1 – <span class="cost">15.000.000 VND</span> (3.5 tháng)</div>
    <div class="node">A2 – <span class="cost">17.000.000 VND</span> (3.5 tháng)</div>
    <div class="node">B1 – <span class="cost">19.000.000 VND</span> (3.5 tháng)</div>
    <div class="node">B2 – <span class="cost">21.000.000 VND</span> (4 tháng)</div>
    <div class="node">Tổng học tiếng A1 + A2 + B1: <span class="cost">51.000.000 VND</span></div>
  </div>

  <div class="node" onclick="toggle('hopDong')">
    <span class="clickable-title">Ký hợp đồng nghề – <span class="cost">4.000 EUR</span></span>
    <span class="hint">Chạm để mở</span>
  </div>
  <div class="children" id="hopDong">
    <div class="node">Lần 1: <span class="cost">2.000 EUR</span> – Khi ký hợp đồng lần đầu</div>
    <div class="node">Lần 2: <span class="cost">2.000 EUR</span> – Sau khi nhận visa (áp dụng cho học viên xử lý hồ sơ tại Lila). Trường hợp ngoài cần hoàn thiện khi có hợp đồng scan và trước khi nhận hợp đồng gốc.</div>
    <div class="node" onclick="toggle('hocPhiDuc')">
      <span class="clickable-title">Học phí tại Đức – <span class="cost">1.600 EUR / 4 tháng</span> (400 EUR/tháng)</span>
      <span class="hint">Chạm để mở</span>
    </div>
    <div class="children" id="hocPhiDuc">
      <div class="node">Khóa học tiếng Đức tại Đức (củng cố chuyên ngành, nâng cao giao tiếp thực tế)</div>
      <div class="node">Khóa tiền nghề (chuẩn bị, làm quen với ngành nghề mà học viên lựa chọn trước khi bước vào Ausbildung chính thức)</div>
    </div>

    <div class="node" onclick="toggle('chungMinh')">
      <span class="clickable-title">Chứng minh tài chính</span>
      <span class="hint">Chạm để mở</span>
    </div>
    <div class="children" id="chungMinh">
      <div class="node">Mỗi tháng <span class="cost">1.091 EUR</span> x 4 tháng (ở thời điểm hiện tại, mức chứng minh tài chính có thể thay đổi trong tương lai)</div>
      <div class="node">Tổng: <span class="cost">4.364 EUR</span> – Mỗi tháng rút về tại Đức 1.091 EUR sử dụng cho chi tiêu cá nhân (sinh hoạt phí)</div>
    </div>

    <div class="node" onclick="toggle('sinhHoat')">
      <span class="clickable-title">Sinh hoạt phí 4 tháng – <span class="cost">1.800 EUR</span></span>
      <span class="hint">Chạm để mở</span>
    </div>
    <div class="children" id="sinhHoat">
      <div class="node">Nhà ở: <span class="cost">350 EUR/tháng</span></div>
      <div class="node">Ăn uống: <span class="cost">80 – 150 EUR/tháng</span></div>
    </div>

  </div>

</div>

<div class="node main-node" onclick="toggle('hocNghe')">
II. Giai đoạn tại Đức
</div>
<div class="children" id="hocNghe">

  <div class="node"><strong>Khóa tiếng Đức – khóa tiền nghề tại Đức. Thời gian nhập học: 01/04/2026.</strong></div>
  <div class="node"><span class="clickable-title">Chương trình bao gồm:</span> khóa học tiếng Đức trình độ B1 hoặc B2 (tùy năng lực đầu vào của học viên) kết hợp với khóa tiền nghề tại Đức.</div>
  <div class="node"><span class="clickable-title">Tổng thời gian đào tạo:</span> 4 tháng liên tục tại Đức trước khi bước vào Ausbildung chính thức.</div>
  <div class="node"><span class="clickable-title">Nội dung tiếng Đức:</span> củng cố ngữ pháp, mở rộng từ vựng chuyên ngành, luyện nghe – nói trong môi trường làm việc thực tế, chuẩn bị cho yêu cầu giao tiếp trong doanh nghiệp.</div>
  <div class="node"><span class="clickable-title">Nội dung khóa tiền nghề (Vorbereitungskurs):</span> làm quen với ngành nghề đã ký hợp đồng, thực hành tình huống thực tế, định hướng tác phong làm việc, kỷ luật lao động và văn hóa doanh nghiệp tại Đức.</div>
  <div class="node">Sau khi hoàn thành 4 tháng tiếng Đức + tiền nghề, học viên đủ điều kiện chuyển tiếp vào chương trình Ausbildung bắt đầu từ 01/09/2026 (tùy bang).</div>

  <div class="node" onclick="toggle('khoaNghe')">
    <span class="clickable-title">Khóa học nghề tại Đức</span>
    <span class="hint">Chạm để mở</span>
  </div>
  <div class="children" id="khoaNghe">
      <div class="node">Thời gian học nghề bắt đầu: 01/09/2026 (Hessen đến 30/09)</div>

      <div class="node" onclick="toggle('luong')">
        <span class="clickable-title">Mức lương tham khảo</span>
        <span class="hint">Chạm để mở</span>
      </div>
      <div class="children" id="luong">
        <div class="node">Năm 1: <span class="cost">1.250 EUR</span> (Tham chiếu theo năm 2025)</div>
        <div class="node">Năm 2: <span class="cost">1.294 EUR</span> (Tham chiếu theo năm 2025)</div>
        <div class="node">Năm 3: <span class="cost">1.462 EUR</span> (Tham chiếu theo năm 2025)</div>
      </div>
  </div>

</div>

<div class="node main-node" onclick="toggle('tongChiPhi')">
III. Tổng chi phí
</div>
<div class="children" id="tongChiPhi">
  <div class="node">Phí dịch vụ: <span class="cost">4.000 EUR</span></div>
  <div class="node">Học phí tại Đức: <span class="cost">1.600 EUR / 4 tháng</span> (400 EUR/tháng)</div>
  <div class="node">Chứng minh tài chính: <span class="cost">4.364 EUR</span></div>
  <div class="node">Tổng EUR: <span class="cost">9.964 EUR</span></div>
  <div class="node">+ Tổng học tiếng A1 + A2 + B1: <span class="cost">51.000.000 VND</span></div>
</div>

</div>

<div class="footer">
<strong>lila-deutsch.com</strong><br>
<strong>vertrieb.lilasprachschule@gmail.com</strong><br>
<strong>0961 679 869</strong>
</div>

</body>
</html>
