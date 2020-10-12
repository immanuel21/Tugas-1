# Currency Apps
Aplikasi ini mencakup fungsi perhitungan nilai tukar Satu dolar dianggap senilai Rp.15.000
## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menyentuh tombol hitung
- User mendapat info "INVALID" jika yang dimasukkan beripa text

## How Does it Works

Diawali dari method 'MainWorld' pada class Main.Window.cs, kita mendeklarasikan InitializeComponent(); lalu CurrencyController = new CurrencyController seperti di bawah ini

```csharp
      public MainWindow()
        {
            InitializeComponent();
            CurrencyController = new CurrencyController();
        }
```

Logika perhitungan terdapat pada class `CurrencyControllr.cs ini diawali dengan public string usdToIdr(string nominal) sebagai berikut
Cara kerjanya seperti di bawah ini
```csharp
      public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```