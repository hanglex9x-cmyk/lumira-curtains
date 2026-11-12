# LUMIRA CURTAINS — App quản lý xưởng rèm (bản chính thức)

App quản lý cho xưởng rèm **LUMIRA CURTAINS** (Quảng Oai, Ba Vì, Hà Nội — hotline 0869 060 080):
đơn hàng, báo giá/hóa đơn A5, lệnh sản xuất, kho hàng 2 nhóm (Sản xuất / Hàng nhập),
lịch lắp đặt, thu tiền nhiều lần, lương khoán, hóa đơn điện tử MISA (mô phỏng ghi hồ sơ).

## Kiến trúc (miễn phí, dữ liệu thuộc về xưởng)

- **Frontend**: `index.html` tĩnh trên GitHub Pages — https://hanglex9x-cmyk.github.io/lumira-curtains/
- **Backend**: Google Apps Script Web App (`Code.gs`), chạy trên tài khoản Google của xưởng.
- **Dữ liệu**: Google Sheet "LUMIRA CURTAINS — Dữ liệu quản lý xưởng rèm" (13 tab:
  CAU_HINH, KHACH_HANG, DON_HANG, LENH_SX, KHO_HANG, NHAP_XUAT, LICH_LAP, PHIEU_THU,
  NHAN_SU, LUONG_KHOAN, HOA_DON_MISA, PHAN_QUYEN, LICH_SU).
- Phân quyền theo tab PHAN_QUYEN (Admin / NhanVien / Xem), mọi thao tác ghi được lưu vào LICH_SU.
- Sao lưu Sheet tự động 2h sáng mỗi ngày (trigger `autoBackup`).

## Cập nhật code

- Sửa giao diện: sửa `index.html` rồi tải đè lên repo này (GitHub Pages tự cập nhật sau ~1 phút).
- Sửa backend: dán lại `Code.gs` trong Apps Script của Sheet → Deploy → Manage deployments →
  sửa deployment hiện tại → Version: New version (giữ nguyên link /exec).

Bản quyền thuộc sở hữu của hanglex9x@gmail.com
