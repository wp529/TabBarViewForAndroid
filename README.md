# TabBarViewForAndroid
非常简单的为项目设置上TabBar
### 导入步骤
* 下载项目，将tabbarview做为moudle导入
* 在gradle的dependencies添加compile project(':tabbarview')
### 使用步骤
1. 在需要使用TabBar的Activity中的布局文件加入TabBarView标签: 
```
  <com.pzhu.tabbarview.TabBarView
      android:layout_width="match_parent"
      android:layout_height="match_parent">
  </com.pzhu.tabbarview.TabBarView>
```
2. 添加命名空间
  xmlns:app="http://schemas.android.com/apk/res-auto"
3. 在TabBarView中加入子标签
 ```
  <com.pzhu.tabbarview.Page
            android:layout_width="100dp"
            android:layout_height="100dp"
            app:page="com.pzhu.test.fragment.AFragment"
            app:text="首页"
            app:icon_normal="@drawable/tab1"
            app:icon_select="@drawable/tab_click1"
            app:checked="true"
            app:text_color_normal="#777"
            app:text_color_select="#f00"
            />
```
4. 完整代码：
```
  <com.pzhu.tabbarview.TabBarView
        android:layout_width="match_parent"
        android:layout_height="match_parent">
        <com.pzhu.tabbarview.Page
            android:layout_width="100dp"
            android:layout_height="100dp"
            app:page="com.pzhu.tabbartest.fragment.AFragment"
            app:text="首页"
            app:icon_normal="@drawable/tab1"
            app:icon_select="@drawable/tab_click1"
            app:checked="true"
            app:text_color_normal="#777"
            app:text_color_select="#f00"
            />

        <com.pzhu.tabbarview.Page
            android:layout_width="100dp"
            android:layout_height="100dp"
            app:page="com.pzhu.tabbartest.fragment.BFragment"
            app:text="个人中心"
            app:icon_normal="@drawable/tab2"
            app:icon_select="@drawable/tab_click2"
            app:text_color_normal="#777"
            app:text_color_select="#f00" />

    </com.pzhu.tabbarview.TabBarView>
```
### Page里属性解释
```
    text -> tab文字  
    icon_normal -> tab未选中时的图标
    icon_select -> tab选中时的图标
    checked -> 初始化选中项
    text_color_normal -> tab未选中时文字颜色
    text_color_select -> tab选中时文字颜色
    page -> tab对应的fragment tips:fragment包名加类名
```
### 解释
  TabBarView的子节点按顺序从左到右显示
 
