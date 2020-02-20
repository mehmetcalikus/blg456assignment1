Robotik assignment 1

Kodun çalışma mantığı basitçe şu şeklidedir:
Robot hareketine başladıktan sonra yavaş bir hızda sağa dönerek ilerler(dönme hızı 0.1) bu hareketin amacı bir duvar bulmaktır
duvarı bulduktan sonra karşısı dolu olduğu zaman sola döner önünü boşaltır yani duvarı sağına alır daha sonra follow_wall fonksiyonu 
ile düz bir şekilde duvarı takip eder burada uygulanan yöntem en basit şekliyle labirentten çıkma algoritmasıdır.

En büyük sorun olan nan değerleri için duvara uzaklığı tutan değişkenin bir önceki değeri tutularak(pre_region) olası duvara çarpma işleminden
olabildiğince kurtarılmaya çalışılmıştır.

Bazı özel durumlar için örneğin büyük odanın en ortasından başlama durumu gibi pre_region'a herhangi bir değer atanmamış ve bütün region değerleri nan olacağından bu durumun üstesinden gelmek için pre_region'a en başta 10 değerleri atanmıştır ki duvar bulma fonksiyonu çalışmaya başlayabilsin.
	

Mehmet Çalıkuş
150150042
