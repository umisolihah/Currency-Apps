# Currency App
apikasi ini mencakup fungsi perhitungan nilai tukar mata uang dari dolar ke rupiah.
satu dolar danggap senilai Rp. 15.000

# Scope & Fungtionalities
- user dapat memasukkan angka
- user dapat menyentuh tombol hitung
- usermendapat info "INVALID" jika yang dimasukkan berupa teks

# How Does it works?
Diawali dari method `MainWindow` pada class MainWindow.xaml.cs, kita mendeklarasikan :

```csharp
public MainWindow()
        {
            InitializeComponent();
            currencyController = new CurrencyController();
        }
```

Logika perhitungan terdapat pada class `CurrencyControll.cs` sebagai berikut :

```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
``` 