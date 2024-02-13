#include <iostream>
#include <string>

using namespace std;

// Fungsi untuk menghitung total bayar berdasarkan jenis buku dan jumlah pinjaman
int hitungTotalBayar(char jenisBuku, int jumlahPinjaman) {
    int tarifSewa;
    switch (jenisBuku) {
        case 'C':
        case 'c':
            tarifSewa = 500;
            break;
        case 'K':
        case 'k':
            tarifSewa = 700;
            break;
        case 'N':
        case 'n':
            tarifSewa = 1000;
            break;
        default:
            tarifSewa = 0; // Jika kode buku tidak valid, maka tarif dianggap 0
            break;
    }
    return tarifSewa * jumlahPinjaman;
}

int main() {
    char lanjut;
    
    do {
        string namaPenyewa;
        char kodeBuku;
        int jumlahPinjaman;

        // Meminta input dari pengguna
        cout << endl << endl;
        cout << "PERPUSTAKAAN KECIL-KECILAN" << endl;
        cout << "-----------------------------" << endl;
        cout << endl << endl;
        cout << "Masukkan nama penyewa buku: ";
        getline(cin >> ws, namaPenyewa);
        cout << "------------------------------------------------------------------" << endl;
        cout << "| Kode | Jenis Buku \t\t                 |     Tarif    |" << endl;
        cout << "------------------------------------------------------------------" << endl;
        cout << "|  C   | CerPen (Kumpulan Cerita Pendek)\t |   500        |" << endl;
        cout << "|  K   | Komik \t\t                         |   700        |" << endl;
        cout << "|  N   | Novel \t\t                         |   1000       |" << endl;
        cout << "------------------------------------------------------------------" << endl;
        cout << "Masukkan kode buku (C untuk CerPen, K untuk Komik, N untuk Novel): ";
        cin >> kodeBuku;
        cout << "Masukkan jumlah pinjaman: ";
        cin >> jumlahPinjaman;

        // Hitung total bayar berdasarkan jenis buku dan jumlah pinjaman
        int totalBayar = hitungTotalBayar(kodeBuku, jumlahPinjaman);

        // Menampilkan hasil
        if (totalBayar > 0) {
            string jenisBukuStr;
            switch (kodeBuku) {
                case 'C':
                case 'c':
                    jenisBukuStr = "Cerita Pendek";
                    break;
                case 'K':
                case 'k':
                    jenisBukuStr = "Komik";
                    break;
                case 'N':
                case 'n':
                    jenisBukuStr = "Novel";
                    break;
                default:
                    jenisBukuStr = "Tidak Valid";
                    break;
            }
            cout << endl << endl;
            cout << "TOTAL PEMBAYARAN PEMINJAN" << endl;
            cout << "-------------------------------------------------" << endl;
            cout << "Nama Penyewa   |\t\t   " << namaPenyewa << endl;
            cout << "Jenis Buku     |\t\t   " << jenisBukuStr << endl;
            cout << "Tarif sewa     |\t\tRp. " << totalBayar << endl;
            cout << "-------------------------------------------------" << endl;
            cout << "Jumlah bayar penyewa buku: \tRp. " << totalBayar << endl;
            cout << endl;
        } else {
            cout << "Kode buku tidak valid atau jumlah pinjaman tidak valid." << endl;
        }

        // Meminta pengguna apakah ingin melanjutkan
        cout << "Ingin menjalankan program dari awal (y/n)? ";
        cin >> lanjut;
        cin.ignore(); // Membersihkan buffer dari karakter newline sebelumnya
    } while (lanjut == 'y' || lanjut == 'Y');

    return 0;
}
