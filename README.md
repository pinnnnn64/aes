# Simulator AES Round 1: Enkripsi dan Dekripsi

plaintext → Pre-round transformation → Round 1 (SubBytes, ShiftRows, MixColumns, AddRoundKey), lalu seluruh prosesnya dibalik sampai plaintext kembali.

## Input

Plaintext (16 karakter ASCII atau 32 digit hex)

Cipher key K₀ (32 digit hex)

K₁ dihitung otomatis lewat key expansion. Klik Acak untuk membuat key baru, Default untuk kembali ke key soal.

Byte diisikan ke matriks 4×4 per kolom: 4 byte pertama = kolom 0, dst. Teks diubah ke hex memakai tabel ASCII. Perubahan input langsung dihitung ulang.

## Blok diagram

Round key

Cipher key K₀

↓

Key expansion ⇒ K₁

**Animasi matriks (hex dan biner)**

## Output

Plaintext (input)

—

Output Pre-round

—

Output Round 1 (ciphertext)

—

Plaintext (hasil dekripsi)

—

## Tabel-tabel

Matriks konstanta

### MixColumns

### InvMixColumns

### ShiftRows / InvShiftRows

Baris 0: tidak bergeser\
Baris 1: kiri 1 byte (inv: kanan 1)\
Baris 2: kiri 2 byte (inv: kanan 2)\
Baris 3: kiri 3 byte (inv: kanan 3)

S-Box (SubBytes)

Inverse S-Box (InvSubBytes)

Nibble kiri byte = baris, nibble kanan = kolom. Sel yang dipakai pada langkah SubBytes atau InvSubBytes akan menyala.

Tabel ASCII (karakter tercetak)

Baris = nibble kiri, kolom = nibble kanan. Karakter plaintext yang dipakai akan menyala.
