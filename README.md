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





Tapsiriq 1 
```c#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp8
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Username:");
            var ad = Console.ReadLine();
            Console.WriteLine("Password:");
            var soyad = Console.ReadLine();

            Telebe Zamin = new Telebe(ad, soyad);

            if (Zamin.Username == "admin" && Zamin.Password == "admin")
            {
                Console.WriteLine("sisteme daxil oldunuz");
            }
            else
            {
                var a = 0;

                Console.WriteLine("Yeniden yoxlayin:");
                for (int i = 0; i < 4; i++)
                {
                    a = i;
                    Console.WriteLine("Username:");
                    var adtekrar = Console.ReadLine();
                    Console.WriteLine("Password:");
                    var soyadtekrar = Console.ReadLine();

                    Telebe Zamintekrar = new Telebe(adtekrar, soyadtekrar);

                    if (a == 3 && Zamintekrar.Username != "admin" && Zamintekrar.Password != "admin")
                    {
                        Console.WriteLine("Hesabiniz blok olunub zehmet olmasa 012 000 00 00 nomresi ile elaqe saxlayin");
                    }

                    if (Zamintekrar.Username == "admin" && Zamintekrar.Password == "admin")
                    {
                        i = 4;
                        Console.WriteLine("sisteme daxil oldunuz:");
                        Console.WriteLine("Adiniz:Zamin");
                        Console.WriteLine("Soyadiniz:Hesenov");
                    }

                    else
                    {
                        Console.WriteLine("yeniden yoxlayin");
                    }
                }
            }


        }
    }

    class Telebe
    {
        public string Username;
        public string Password;

        public Telebe(string _username, string _password)

        {
            this.Username = _username;
            this.Password = _password;
        }


    }


}
```

