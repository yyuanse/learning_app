# learning_app
A repository for learning APP.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
1.线性布局

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="horizontal"
    >
    <Button
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:text="按钮1"
        android:layout_weight="1"
        android:layout_marginRight="10dp"
        >
    </Button>
    <Button
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:text="按钮2"
        android:layout_weight="1"
        android:layout_marginRight="10dp"
        >
    </Button>
    <Button
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:text="按钮3"
        android:layout_weight="2"
        >
    </Button>

</LinearLayout>


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
2.相对布局

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    >

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:layout_margin="20dp"
        android:text="按钮1"
        ></Button>
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/bt2"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="260dp"
        android:text="按钮2"
        ></Button>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_toRightOf="@id/bt2"
        android:layout_alignBottom="@id/bt2"
        android:layout_marginBottom="100dp"
        android:text="按钮3"
        ></Button>
</RelativeLayout>
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
3.表格布局

<?xml version="1.0" encoding="utf-8"?>
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:stretchColumns="2"
    >
    <TableRow>
        <Button android:text="按钮1" ></Button>
        <Button android:text="按钮2" ></Button>
    </TableRow>
    <TableRow>
       <Button android:text="按钮3"
           android:layout_column="1"
           ></Button>
        <Button android:text="按钮4"></Button>
    </TableRow>
    <TableRow>
        <Button android:text="按钮5"
            android:layout_column="2"
            ></Button>
    </TableRow>

</TableLayout>
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
4.制作一个按钮，当点击的时候，按钮文本内容发生改变
这里需要两个文件就行操作，一个是layout文件，一个是java文件接收这个点击事件。
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    >
    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="按钮1"
        android:id="@+id/btn1"
        android:onClick="method1"
        ></Button>
</LinearLayout>
----------------------------------------------------------------------------
package com.example.myapp;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {
    Button btn1 = null;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        btn1 = findViewById(R.id.btn1);//找到按钮
    }
    public void method1(View view){
        btn1.setText("按钮1被点击。");
    }
}
