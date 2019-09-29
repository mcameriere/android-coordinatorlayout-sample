# android-coordinatorlayout-sample
An AppBarLayout that scrolls when you scroll a sibling NestedScrollView

## Add Library Dependency

com.android.support.design:28.0.0

## Modify the layout

The root element is a CoordinatorLayout.
It contains an AppBarLayout and a sibling NestedScrollView.

    <CoordinatorLayout>

        <AppBarLayout>
            <ToolBar/>
        </AppBarLayout>

        <NestedScrollView>
            <!-- Your scrollable content here... -->
        </NestedScrollView>

    </CoordinatorLayout>

Set layout_behavior and layout_scrollFlags as follows

    <?xml version="1.0" encoding="utf-8"?>
    <androidx.coordinatorlayout.widget.CoordinatorLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        xmlns:app="http://schemas.android.com/apk/res-auto">

        <com.google.android.material.appbar.AppBarLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">

            <androidx.appcompat.widget.Toolbar
                android:layout_width="match_parent"
                android:layout_height="?attr/actionBarSize"
                app:layout_scrollFlags="scroll"/>

        </com.google.android.material.appbar.AppBarLayout>

        <androidx.core.widget.NestedScrollView
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            app:layout_behavior="@string/appbar_scrolling_view_behavior">

            <!-- YOUR CONTENT HERE... -->
            
        </androidx.core.widget.NestedScrollView>

    </androidx.coordinatorlayout.widget.CoordinatorLayout>
