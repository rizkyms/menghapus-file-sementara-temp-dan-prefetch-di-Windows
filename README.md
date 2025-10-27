# Menghapus file sementara (Temp) dan Prefetch di Windows

### Langkah-langkah:

**1. Buka Notepad**

Salin seluruh isi kode berikut:

@echo off
title Clean Temp & Prefetch Files
color 0A
echo ===============================================
echo       Cleaning TEMP and PREFETCH files...
echo ===============================================

echo.
echo Cleaning User Temp Folder...
del /s /f /q "%temp%\*.*"
for /d %%p in ("%temp%\*.*") do rmdir "%%p" /s /q

echo.
echo Cleaning Windows Temp Folder...
del /s /f /q "C:\Windows\Temp\*.*"
for /d %%p in ("C:\Windows\Temp\*.*") do rmdir "%%p" /s /q

echo.
echo Cleaning Prefetch Folder...
del /s /f /q "C:\Windows\Prefetch\*.*"
for /d %%p in ("C:\Windows\Prefetch\*.*") do rmdir "%%p" /s /q

echo.
echo ===============================================
echo All temporary files have been cleaned!
echo ===============================================
pause
exit


**2. Simpan dengan nama misalnya:**

**Clean_Temp_Prefetch.bat**


Saat menyimpan, ubah Save as type → All Files, dan pastikan nama berakhiran **.bat**
(bukan .txt).

Klik kanan file tersebut → **Run as Administrator**
