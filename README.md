## PhotoTouchView ##
> 该库是一个Android图片查看缩放控件,在[PinchImageView](https://github.com/boycy815/PinchImageView)基础上进一步封装,主要功能:
> 
> - 网络和本地图片查看,支持双指手势,单双击事件
> - 支持单图及多图查看
> - 一键保存到本地相册

## 引用 ##
最新版本号[![](https://jitpack.io/v/ChenZhen-ZH/PhotoTouchView.svg)](https://jitpack.io/#ChenZhen-ZH/PhotoTouchView)
### Gradle ###

Project.gradle

    allprojects {
    	repositories {
        	jcenter()
        	maven { url "https://jitpack.io" }
    	}
	}

app.gradle

    compile 'com.github.ChenZhen-ZH:PhotoTouchView:v0.8.1'

### Maven ###
	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
==
	<dependency>
	    <groupId>com.github.ChenZhen-ZH</groupId>
	    <artifactId>PhotoTouchView</artifactId>
	    <version>v0.8.1</version>
	</dependency>

## 使用 ##
1. 在布局xml中加入该自定义控件

        <com.unco.photoliarary.PhotoTouchView
        android:id="@+id/photo_view"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>

2. java代码中传入图片集合即可

		mTouchView = (PhotoTouchView) findViewById(R.id.photo_view);
    	mTouchView.showImages(imageList);

## 扩展功能 ##
1. 保存当前图片到本地相册

    	mTouchView.saveCurrentImage(new SaveImageCall() {
                @Override
                public void onSucce() {//保存成功
                    Toast.makeText(PhotoTouchActivity.this, "保存成功", Toast.LENGTH_SHORT).show();
                }

                @Override
                public void onFault() {//保存失败
                    Toast.makeText(PhotoTouchActivity.this, "保存失败,请稍后再试", Toast.LENGTH_SHORT).show();
                }
            });

## 效果图 ##

![](http://i.imgur.com/f03lEmW.jpg)

## 关于作者 ##

- 新浪微博:[@Chen丶振](http://weibo.com/724132180 )
- Email:18620156376@163.com



我会慢慢完善这个控件,加入更多的易用的API.大家有任何建议或者发现Bug都可以提Issues,也可以给我发邮件.
