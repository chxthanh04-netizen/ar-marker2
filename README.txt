MARKER 2 - WEB AR | LAU CHUONG / LAU TRONG
========================================

1. NOI DUNG
   index.html: AR.js + A-Frame, 3 cap tuong tac
   assets/: thu muc cho model .glb va marker .patt trong tuong lai

2. CHAY THU
   - De mac dinh CONFIG.demoModels = true.
   - Mo bang HTTPS (vi du GitHub Pages) hoac localhost.
   - Tren dien thoai, cho phep camera va quet Hiro marker.
   - Hiro: https://raw.githubusercontent.com/AR-js-org/AR.js/master/data/images/hiro.png
   - Dung ngoi sao? Khong: phai dung dung hinh marker Hiro (khong phai ma QR).

   Neu muon chay tren may tinh: vao thu muc nay bang terminal:
      python -m http.server 8000
   Mo http://localhost:8000 tren trinh duyet cung may.
   Khi xem tren dien thoai tu may chu noi bo, thong thuong can HTTPS,
   vi IP noi bo qua HTTP se khong duoc phep su dung camera.

3. KHI CO MODEL BLENDER
   Cho cac tep vao assets/:
      lau-chuong-trong.glb
      mai-dao.glb
      ngoi-canh-sen.glb

   Trong index.html doi: demoModels: false
   Mot file lau-chuong-trong.glb duoc hien thanh 2 ban sao vi 2 cong trinh
   co kien truc tuong dong. Neu 2 cong trinh co khac biet ro ret,
   co the chuyen sang hai file model rieng.

4. KHI CO MARKER RIENG
   Tao pattern (.patt) bang AR.js Marker Training.
   Doi trong index.html:
     <a-marker id="marker2" preset="hiro" emitevents="true" ...>
   thanh:
     <a-marker id="marker2" type="pattern" url="assets/marker2.patt"
               emitevents="true" smooth="true">

5. NOI DUNG VA DIEU CHINH
   - Sua CONTENT de thay the 3 o thong tin bang van ban chinh xac.
   - Chua xac minh duoc ten chua nguon mau, nen co dau [Bo sung...].
   - Sua CONFIG.hotspotRelative neu cham sang chua dung diem tren file .glb.
   - Nut 'Tro ve' lui mot cap. Nut 'Tro ve mo hinh tong the' o cap 2/3.
   - Khi marker mat/tim lai, cap dang xem duoc giu nguyen.
   - UI HTML de de doc tren dien thoai, hotspot gan theo model bang phep chieu 3D -> 2D.

6. LUU Y
   - Demo model chi la so do minh hoa, KHONG phai kien truc xac thuc.
   - Doi lai model Blender thi can kiem thu hotspot tren thiet bi that.
   - File HTML can mang Internet de tai A-Frame va AR.js tu CDN.
   - AR camera/marker chua duoc kiem thu truc tiep tren dien thoai trong goi mau nay.
