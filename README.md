# P102-11.08.2017

# Tapşırıq 01

- İstifadəçidən USERNAME və PASSWORD daxil etməsi tələb olunur
- İstifadəçi düzgün məlumatı (USERNAME="admin" və PASSWORD="admin") 5 dəfə səhv daxil etsə proqram "Hesabınız blok olunub zəhmət olmasa 012 000 00 00 nömrəsi ilə əlaqə saxlayın" mesajını çıxaracaq

# Tapşırıq 02
```javascript
class Program
    {
        static void Main(string[] args)
        {
            // 1.var objA=new ClassA(); --- "PropA - PropB"
            // 2.var objB=new ClassB(); --- "PropA - PropB - PropA - PropC "
            // 3.var objC=new ClassC(); --- "PropA - PropB - PropC"
        }
    }

    class ClassA
    {
        public string PropA= "PropA";
    }
    class ClassB
    {
        public string PropB="PropB";
    }
    class ClassC
    {
        public string PropC="PropC";
    }
```
Yuxarıdakı variantlara əsasən uyğun nəticələri əldə edin

# Suallar 

1. "Variable" və "Property" arasındakı fərqi izah edin.
2. "Constructor" ve custom method arasındakı fərqi izah edin.
3. var keywordu nədir və hansı hallarda istifadə edilə bilər ?
4. Hər hansı bir class daxilində başqa bir class təyin edilə bilər mi? Səbəblərini izah edin

# Qaynaqlar

- https://mva.microsoft.com/en-us/training-courses/c-fundamentals-for-absolute-beginners-16169?l=Lvld4EQIC_2706218949
- https://www.linkedin.com/learning/c-sharp-essential-training/using-built-in-data-types
- https://www.youtube.com/watch?v=GGXE44ucqCE&list=PLKnjBHu2xXNPkeQtMOJczzEO6LK5OV35K

