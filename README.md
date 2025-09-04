[OKU- READ ME.txt](https://github.com/user-attachments/files/22129074/OKU-.READ.ME.txt)
Hey! This is My First Web Scraping Project!

I built this project with Python to pull book data from the web. I learned how to get the titles and prices of books from a simple website and save them neatly in my MySQL database. At the end of the project, I even managed to export all the data into a file that can be opened in Excel. I think this is a great starter project to show what's possible with Python.

#### **What's Inside?**

-   **Web Data Pulling**: I used the `requests` and `Beautiful Soup` libraries to grab the site's HTML code and find the specific info I needed (titles, prices).
-   **Database Saving**: I saved all the data I pulled into a MySQL database in a special table I created. This keeps all the data organized and ready whenever I need it.
-   **Excel-Friendly Output**: I exported all the info from the database into a CSV file, which makes it super easy to open and analyze in Excel.

#### **Let's Get Started!**

If you want to try this project on your own computer, here's what you'll need:

-   **Python 3.x**
-   **MySQL Server & MySQL Workbench**

#### **Setup**

1.  **Install Libraries**: Open your command line and run these commands:
    ```bash
    pip install requests
    pip install beautifulsoup4
    pip install mysql-connector-python
    ```
2.  **Prep Your Database**:
    -   Open MySQL Workbench.
    -   Run these commands to set up your database and table:
        ```sql
        CREATE DATABASE IF NOT EXISTS deneme_db;
        USE deneme_db;
        CREATE TABLE IF NOT EXISTS kitaplar (
            id INT AUTO_INCREMENT PRIMARY KEY,
            baslik VARCHAR(255),
            fiyat VARCHAR(20)
        );
        ```
3.  **Customize the Code**:
    -   Open the `Web_Scraping.py` file.
    -   Find the MySQL connection part and update the `password` field with your own MySQL password:
        ```python
        db_connection = mysql.connector.connect(
            host="localhost",
            user="root",
            password="YOUR_MYSQL_PASSWORD", # Replace with your password
            database="deneme_db"
        )
        ```

#### **How to Run It**

1.  In your command line, navigate to the folder where you saved the file.
2.  Type this command and hit "Enter":
    ```bash
    python Web_Scraping.py
    ```
    That's it! The script will automatically pull the data and save it to your database.

#### **Exporting Data to Excel**

Once the script is done, you can easily export the data to a CSV file using the **"Table Data Export Wizard"** in MySQL Workbench.

###### Merhaba! Bu, İlk Web Kazıma Projem!

Bu projeyi, web'den kitap verilerini çekmek için Python'la hazırladım. Basit bir web sitesindeki kitapların başlıklarını ve fiyatlarını alıp, düzenli bir şekilde MySQL veritabanıma kaydettim. Projenin sonunda da tüm veriyi Excel'de açabileceğin bir dosyaya aktardım. Bence bu, Python'la neler yapılabileceğini gösteren harika bir başlangıç projesi.

#### **Neler Var?**

-   **Web'den Veri Çekme**: `requests` ve `Beautiful Soup` kütüphanelerini kullanarak sitenin HTML kodunu almayı ve istediğim bilgileri (başlıklar, fiyatlar) bulmayı öğrendim.
-   **Veritabanına Kaydetme**: Çektiğim verileri bir MySQL veritabanına, özel olarak oluşturduğum bir tabloya kaydettim. Bu sayede veriler her zaman el altında ve düzenli.
-   **Excel Dostu Çıktı**: Veritabanındaki tüm bilgileri, daha kolay analiz edebilmek için CSV formatında dışa aktardım. Artık bu dosyayı Excel'de açıp istediğim gibi inceleyebilirim.

#### **Hadi Başlayalım!**

Bu projeyi kendi bilgisayarında denemek istersen, işte ihtiyacın olanlar:

-   **Python 3.x**
-   **MySQL Sunucusu ve MySQL Workbench**

#### **Kurulum**

1.  **Kütüphaneleri Yükle**: Komut satırını aç ve şu komutları çalıştır:
    ```bash
    pip install requests
    pip install beautifulsoup4
    pip install mysql-connector-python
    ```
2.  **Veritabanını Hazırla**:
    -   MySQL Workbench'i aç.
    -   Şu komutları çalıştırarak veritabanı ve tabloyu oluştur:
        ```sql
        CREATE DATABASE IF NOT EXISTS deneme_db;
        USE deneme_db;
        CREATE TABLE IF NOT EXISTS kitaplar (
            id INT AUTO_INCREMENT PRIMARY KEY,
            baslik VARCHAR(255),
            fiyat VARCHAR(20)
        );
        ```
3.  **Kodu Kendine Göre Ayarla**:
    -   `Web_Scraping.py` dosyasını aç.
    -   MySQL bağlantı kısmını bul ve `password` alanına kendi MySQL şifreni yaz:
        ```python
        db_connection = mysql.connector.connect(
            host="localhost",
            user="root",
            password="SENIN_MYSQL_SIFREN", # Burayı kendi şifrenle değiştir
            database="deneme_db"
        )
        ```

#### **Nasıl Çalıştırılır?**

1.  Komut satırında dosyanın olduğu klasöre git.
2.  Şu komutu yaz ve "Enter"a bas:
    ```bash
    python Web_Scraping.py
    ```
    Hepsi bu kadar! Kodun verileri otomatik olarak çekip veritabanına kaydedecek.

#### **Veriyi Excel'e Aktarmak**

Kod çalıştıktan sonra, MySQL Workbench'teki **"Table Data Export Wizard"** özelliğiyle verileri kolayca bir CSV dosyasına aktarabilirsin.

---
