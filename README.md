# Sidebar
side or navigation bar

Sidebar 配置
<code>

              // 显示文字, default: false
              sidebarView.isShowText(true);
              
              // 默认选中 index ； 不默认选中 则为 -1; 当 setViewPager 时, mCurrentItem value set 0
              sidebarView.setDefaultSelectItemOfIndex(-1);
        
              // 点击 item 是否改变 Sidebar 的背景颜色, default: false
              sidebarView.isClickChangeBackgroundColor(false);
               
              // Sidebar 背景颜色, 当 显示动画效果且 index >= 0 时, 失效
              sidebarView.setBaseBackgroundColor(getResources().getColor(R.color.colorPink));
          
              // 选中 Item 的颜色
              sidebarView.setItemSelectedColor(getResources().getColor(R.color.colorWhite));
        
              // 未选中 Item 的颜色
              sidebarView.setItemUnSelectedColor(getResources().getColor(R.color.colorGray));
        
              sidebarView.setItemSelectedTextColor(getResources().getColor(R.color.itemClickColor));
              sidebarView.setItemUnSelectedTextColor(getResources().getColor(R.color.colorCC));

              // 设置textSize, default: 12sp
              sidebarView.setSelectedTextSize(32);
              sidebarView.setUnSelectedTextSize(32);

              // Sidebar 方向, default: horizontal
              sidebarView.orientationIsVertical();
        
              // Sidebar 横向的高度 或者 竖向 item 的宽高
              sidebarView.setSidebarWidth(100);
        
              // 点击 item 是否有动画效果, default：true
              sidebarView.isAnimator(false);
        
              // 点击事件响应已选中 Item, default: false
              sidebarView.isSelectedItemClick(true);
        
              // if isAnimator is true, 点击 Item, Item 偏移量， default: 30
              sidebarView.setAnimatorPadding(30);
        
              // if isAnimator is true, Item 初始偏移量, default：10
              sidebarView.setInitializePadding(10);
        
              // 隐藏 Item， 传值类型为 int[] 数组, 当某个 Item 或者多个 Item 暂时不需要时，设置该项
              sidebarView.setItemGone(new int[]{1});
              
</code>
            
Sidebar 在左侧

<code>

    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@android:color/white"
        android:orientation="horizontal">
        
        <com.github.chengheaven.sidebar.SidebarView
            android:id="@+id/sidebar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
        
        <android.support.v4.view.ViewPager
            android:id="@+id/view_pager"
            android:layout_width="match_parent"
            android:layout_height="match_parent" />
        
    </LinearLayout>
    
</code>

![](https://github.com/chengHeaven/Sidebar/raw/master/images/3.gif)         ![](https://github.com/chengHeaven/Sidebar/raw/master/images/3-1.gif) ![](https://github.com/chengHeaven/Sidebar/raw/master/images/3-2.gif)

将 orientation 的方向改为 vertical , 则 Sidebar 在上方

![](https://github.com/chengHeaven/Sidebar/raw/master/images/2.gif)         ![](https://github.com/chengHeaven/Sidebar/raw/master/images/2-1.gif) ![](https://github.com/chengHeaven/Sidebar/raw/master/images/2-2.gif)
        
Sidebar 在下方布局

<code>

    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@android:color/white">
        
        <com.github.chengheaven.sidebar.SidebarView
            android:id="@+id/sidebar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentBottom="true" />
        
        <android.support.v4.view.ViewPager
            android:id="@+id/view_pager"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_above="@+id/sidebar" />
        
    </RelativeLayout>
    
</code>

![](https://github.com/chengHeaven/Sidebar/raw/master/images/1.gif)         ![](https://github.com/chengHeaven/Sidebar/raw/master/images/1-1.gif) ![](https://github.com/chengHeaven/Sidebar/raw/master/images/1-2.gif)