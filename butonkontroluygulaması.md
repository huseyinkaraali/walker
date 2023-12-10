1. **ButtonControlPanel Sınıfı Oluşturma
   - `ButtonControlPanel` sınıfı, `JFrame` sınıfından türetilmiştir. Bu sınıf, bir GUI penceresini temsil eder.
   - `buttons` adında bir 2D `JButton` dizisi oluşturulur. Bu matris, 4x4 düğmeyi temsil eder.
   - `activeButton` adında bir `JButton` nesnesi oluşturulur. Bu, şu anda etkin olan düğmeyi temsil eder.
   - `graphqlSchema`, `activeColor`, `passiveColor`, `activeIcon`, ve `passiveIcon` gibi sınıfın özellikleri başlatılır.

2. **Pencere Ayarları Yapma
   - Pencerenin başlığı "Button Control Panel" olarak ayarlanır.
   - Kapatma işlemi için `setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE)` kullanılır.
   - Pencerenin boyutu 400x400 piksel olarak ayarlanır.
   - Düğmelerin düzeni 4x4 bir `GridLayout` ile ayarlanır.

3. **Düğmeleri Oluşturma ve Pencereye Ekleme
   - Bir iç içe döngü kullanılarak 4x4 düğme matrisi oluşturulur.
   - Her bir düğme `createButton` metodunu kullanarak oluşturulur ve pencereye eklenir.

4. **Etkin Düğme Başlatma
   - `activeButton` değişkeni, matrisin sol üst köşesindeki düğme ile başlatılır.
   - `updateButtonStatus` metodunu kullanarak bu düğmenin durumu güncellenir.

5. **Düğme Oluşturma Metodu (`createButton`)
   - `createButton` metodu, bir düğme oluşturur ve bu düğmeye bir `ActionListener` ekler.
   - Düğmenin arka plan rengi ve ikonu (`passiveColor` ve `passiveIcon`) başlangıçta ayarlanır.
   - Düğme tıklanırsa, `actionPerformed` metodunu tetikleyen bir `ActionListener` eklenir.
   - Eğer bir önceki etkin düğme (`activeButton`) varsa, durumu güncellenir.
   - Tıklanan düğme etkin düğme (`activeButton`) olur ve durumu güncellenir.

6. **Düğme Durumu Güncelleme Metodu (`updateButtonStatus`)
   - `updateButtonStatus` metodu, bir düğmenin durumunu günceller.
   - Etkin düğme (`activeButton`) belirtilen düğme olur.
   - Etkin düğmenin arka plan rengi, ikonu ve metni (`graphqlSchema`) güncellenir.
   - Diğer tüm düğmelerin durumu pasif hale getirilir.

7. **Ana Metod (`main`)
   - `main` metodu, Swing arayüzü üzerinde işlem yapılması için `SwingUtilities.invokeLater` kullanarak bir `Runnable` başlatır.
   - Bu, `ButtonControlPanel` sınıfından bir nesne oluşturarak GUI'yi başlatır.

8. **Uygulamanın Çalıştırılması
   - `main` metodu tarafından oluşturulan `ButtonControlPanel` nesnesi, kullanıcıya görünen bir pencere oluşturur ve programı başlatır.

