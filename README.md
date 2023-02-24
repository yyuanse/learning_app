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
