# รายงานผลการทดลอง

<นางสาวพัชรี  แอแป> <603410155-3>

## Relative Layout

แสดง Control `title` และ `Detail`

```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".RelativeActivity">


    <EditText
        android:id="@+id/editText6"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name" />

    <EditText
        android:id="@+id/editText5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:text="Button" />

</RelativeLayout>
```

แอดทริบิ้วที่แสดงความสัมพันธ์ระหว่าง control ทั้งสอง

```xml
android:layout_below="@id/editText6"  controlให้อยู่ข้างล่าง 
android:layout_below="@id/editText5"  controlให้อยู่ข้างบน
```

## Linear Layout

แสดง Control `to`, `subject`, `tag` และ `message`

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".LinearActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name" />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="horizontal">

        <EditText
            android:id="@+id/editText2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name" />

        <EditText
            android:id="@+id/editText3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name" />

    </LinearLayout>

    <EditText
        android:id="@+id/editText4"
        android:layout_width="match_parent"
        android:layout_height="238dp"
        android:ems="10"
        android:gravity="start|top"
        android:inputType="textMultiLine" />


</LinearLayout>
```

อธิบายความแตกต่างระหว่าง vertical และ horizontal orientation

```
 vertical จัดวางวัตถุแบบตามแนวตั้ง
 horizontal orientation  จัดวางวัตถุแบบตามแนวนอน
```

## Constrant Layout

จงออกแบบและสร้างหน้า Constrant layout สำหรับแสดงข้อมูลนักศึกษา ประกอบไปด้วย รูปโปรไฟล์ รูปพื้นหลัง ชื่อ-นามสกุล รหัสนักศึกษา และเกรดเฉลี่ยรวม

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#B4F3D5D5"
    tools:context=".ConstranActivity">


    <TextView
        android:id="@+id/textView5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="321dp"
        android:layout_marginBottom="200dp"
        android:text="นางสาวพัชรี  แอแป"
        android:textColor="#000000"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintTop_toTopOf="@+id/imageView2"
        tools:ignore="MissingConstraints"
        tools:layout_editor_absoluteX="16dp" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="4dp"
        android:layout_marginLeft="4dp"
        app:layout_constraintStart_toStartOf="@+id/imageView2"
        app:layout_constraintTop_toTopOf="parent"
        app:srcCompat="@drawable/kk" />

    <ImageView
        android:id="@+id/imageView2"
        android:layout_width="185dp"
        android:layout_height="291dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.618"
        app:srcCompat="@drawable/p"
        tools:layout_editor_absoluteX="-8dp"
        tools:ignore="MissingConstraints" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="เกรดเฉลี่ยรวม"
        android:textColor="#001055"
        android:textSize="24sp"
        android:textStyle="bold"
        android:typeface="normal"
        app:fontFamily="sans-serif-thin"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.13"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView5"
        app:layout_constraintVertical_bias="0.111" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="142dp"
        android:layout_height="40dp"
        android:layout_marginBottom="192dp"
        android:text="603410155-3"
        android:textColor="#000000"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.709"
        app:layout_constraintStart_toEndOf="@+id/textView5"
        app:layout_constraintTop_toBottomOf="@+id/imageView"
        app:layout_constraintVertical_bias="0.666" />

    <TextView
        android:id="@+id/textView4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:text="3.24"
        android:textColor="#000000"
        android:textSize="24sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.304"
        app:layout_constraintStart_toEndOf="@+id/textView"
        app:layout_constraintTop_toBottomOf="@+id/textView2" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
