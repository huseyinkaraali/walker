#include <stdio.h>

int binarySearch(int dizi[], int sol, int sag, int aranan) {

    if (sag >= sol) {
        
        int orta = sol + (sag - sol) / 2;
        
        // Aranan eleman ortada mı?
        if (dizi[orta] == aranan) {

            return orta;
        }
        
        // Aranan eleman sol tarafda mı?
        if (dizi[orta] > aranan) {
            return binarySearch(dizi, sol, orta - 1, aranan);
        }
        
        // Aranan eleman sağ tarafda mı?
        return binarySearch(dizi, orta + 1, sag, aranan);
    }
    
    // Eleman dizide yok
    return -1;
}

int main() {

    int dizi[] = {4, 8, 3, 84, 47, 76, 9, 24, 68};
    int n = sizeof(dizi) / sizeof(dizi[0]);
    int aranan = 8;
    
    int sonuc = binarySearch(dizi, 0, n - 1, aranan);
    
    if (sonuc == -1) {
        printf("%d, dizide bulunamadı.", aranan);
    } 
    
    else {
        printf("%d, dizinin %d. indeksinde bulundu.", aranan, sonuc);
    }
    
    return 0;
}
