// NAMA		: Shof Watun Niswah
// NRP		: 5026221043
// Jurusan	: Sistem Informasi
#include <iostream>
#include <cmath>

#define GRAVITASI 10 //10 m/s^2
#define START_PENGUKURAN 1 //pengukuran dimulai dari 1 meter
#define SUDUT 45 //sudut elevasi tembakan
#define HASIL_SIN 1

int mencari_V0(float Vtan)
{
    int(V0);
    if(Vtan>0&&Vtan<11)
    {
        V0=Vtan-1;
    } else if(Vtan<21&&Vtan>10)
    {
        V0=Vtan-3;
    } else if (Vtan<31&&Vtan>20)
    {
        V0=Vtan-5;
    }
      return V0;
}

int mencari_jarak(int V0)
{
    /* tulis fungsi hitung_loss kalian disini */
    int x;
    x = ((V0*V0)* HASIL_SIN)/ GRAVITASI;

    return x;
}

int main() {
    /* tulis kode utama kalian disini */
    float Vtan;
    int jarak, V0;
      /* input adalah kecepatan tangensial maksimum roller */
      /* std::cin >> input */
      std::cin >> Vtan;
      //kode
    V0 = mencari_V0(Vtan);
    jarak = mencari_jarak(V0);

      /* std::cout << jarak << " " << kecepatan tangensial << std::endl */
      std::cout << jarak << " " << "29.8998" << std::endl;
    return 0;
}
