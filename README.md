
# Obed Yudha Pambudi
# 202131082
## Mengubah Citra pada plat motor 

library yang digunakan :
- imutils
- opencv
- numpy
- matplotlib

image = cv2.imread('./plat motor.jpg'): Baris ini membaca gambar dengan nama file 'plat motor.jpg' menggunakan fungsi cv2.imread() dari OpenCV. Anda perlu memastikan bahwa file gambar tersebut berada di direktori yang sama dengan script Anda, atau Anda dapat menyediakan path lengkap jika berada di direktori lain.

b_filter = cv2.bilateralFilter(gray, 11, 17, 17): Baris ini menerapkan filter bilateral pada citra grayscale yang telah Anda konversi sebelumnya. Filter bilateral menggabungkan informasi spasial dan perbedaan intensitas piksel untuk menghasilkan citra yang lebih halus tetapi tetap mempertahankan tepi yang tajam. 

edged = cv2.Canny(b_filter, 30, 200): Baris ini mengaplikasikan operator Canny pada gambar yang telah difilter bilateral sebelumnya. Operator Canny digunakan untuk mendeteksi tepi pada gambar.

plt.imshow(edged, cmap='gray'): Baris ini menggunakan plt.imshow() dari matplotlib untuk menampilkan gambar hasil deteksi tepi. Parameter pertama (edged) adalah gambar yang ingin ditampilkan (dalam hal ini, variabel edged). cmap='gray' digunakan untuk memilih skema warna abu-abu.


