#include <stdio.h>

int main() {
	
	//Dizinin boyutunu ve gerekli diğer değişkenleri tanımlıyoruz
    int n, aranan, i, dizi[100];
    int bulundu = 0;
    
    // Dizinin boyutunu kullanıcıdan istiyoruz
    printf("Dizinin boyutunu girin: ");
    scanf("%d", &n);
    
    // Dizinin elemanlarını kullanıcıdan alıyoruz
    for (i = 0; i < n; i++) {
        printf("\nDizinin %d. elemanini girin: ", i+1);
        scanf("%d", &dizi[i]);
    }
    
    // Aranacak olan elemanı kullanıcıdan istiyoruz
    printf("\nAranacak olan elemani girin: ");
    scanf("%d", &aranan);
    
    // Linear Search algoritmasını kullanarak dizide arama yapıyoruz
    for (i = 0; i < n; i++) {
    	
        if (dizi[i] == aranan) {
            bulundu = 1;
            break;
        }
        
    }
    
    // Aranan elemanın dizide olup olmadığını ekrana yazdırıyoruz
    if (bulundu) {
        printf("\n%d, dizide bulundu.", aranan);
    } 
	
	else {
        printf("\n%d, dizide bulunamadi.", aranan);
    }
    
    
    
    return 0;
}
