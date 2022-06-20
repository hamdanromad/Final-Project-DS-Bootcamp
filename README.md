# Final-Project-DS-Bootcamp
Final Project from Data Science Bootcamp Rakamin Academy.

Stage 1
1. Pengecekan deskripsi statistik data
    ● Data terdiri dari 12330 baris
    ● Semua kolom memiliki nilai yang lengkap atau tidak memiliki null/missing values (Non-Null Count < jumlah baris)
    ● Sepertinya tidak ada issue yang mencolok pada tipe data untuk setiap kolom (sudah sesuai)
    
2. Pengecekan distribusi setiap features terhadap variabel target

    Berdasarkan Statistical Summary :
        ● Kolom 'SpecialDay' ternyata bernilai boolean/binary.
        ● Seluruh kolom yang ada skew ke kanan (long-right tail).
        ● Kolom dengan skew kanan yang paling mendekati normal ada pada kolom : 'ExitRates', 'Region'.
        ● Data dinominasi (proporsi lebih dari 50% dari jumlah baris data) oleh Returning_Visitor (`VisitorType`), artinya proporsi dari visitor lama jauh lebih banyak           dari visitor baru (New_Visitor) dan others, serta pada kolom Weekend, Revenue, Browser_Cats, SpecialDays_Cats, dan OperatingSystems_Cats juga dinominasi oleh            satu nilai.
        ● Tidak ada issue kardinalitas (jumlah unique values) yang cukup tinggi.
    
    Berdasarkan Boxplot :
        ● Mayoritas data memiliki outlier yang sangat menyimpang kecuali pada kolom 'Region'.

    Berdasarkan Distribution Plot :
        ● Kolom 'ExitRates' dan 'Region' tampak sudah mendekati distribusi normal.
        ● Seperti dugaan kita ketika melihat boxplot di atas, kolom lainnya selain 'ExitRates' dan 'Region' lumayan skewed, terutama kolom 'Administrative_Duration',             'Informational', 'Informational_Duration', 'ProductRelated', 'ProductRelated_Duration', 'PageValues' (Berarti ada kemungkinan kita perlu melakukan sesuatu              pada kolom2 tersebut nantinya)
        ● Kolom 'SpecialDay' sejatinya adalah biner, sehingga tidak perlu terlalu diperhatikan bentuk distribusinya
