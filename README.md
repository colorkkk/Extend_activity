@[TOC](实验四)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190514114248791.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMjQxNDEy,size_16,color_FFFFFF,t_70)
<?xml version="1.0" encoding="utf-8"?>
<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <com.example.extend_activity.MyPreferenceCategory
        android:title="In-line preferences"
        >
        <CheckBoxPreference
            android:key="pref_sync"
            android:title="Checkbox preference"
            android:summary="This is a checkbox"
            />
    </com.example.extend_activity.MyPreferenceCategory>
    <com.example.extend_activity.MyPreferenceCategory
        android:title="Dialog-based preferences">
        <EditTextPreference
            android:key="pref"
            android:title="Edit text preference"
            android:summary="An example that uses an edit text dialog"
            android:dialogTitle="Enter your favorite animal"
            />
        <ListPreference
            android:key="pref_syncConnectionType"
            android:title="List preference"
            android:summary="An example that uses a list dialog "
            android:dialogTitle="Choose One"
            android:entries="@array/list_entries"
            android:entryValues="@array/list_entries"
            android:defaultValue="@array/list_entries" />
    </com.example.extend_activity.MyPreferenceCategory>
    <com.example.extend_activity.MyPreferenceCategory
        android:title="launch preferences">
        <PreferenceScreen

            android:title="Screen preference"
            android:summary="Show another screen of preferences"
            >
            <CheckBoxPreference
                android:title="Toggle preference"
                android:summary="Preference that is on the next screen but same hierarchy"
                />
        </PreferenceScreen>
        <Preference
            android:title="Intent preference"
            android:summary="Launches an Activity from an Intent">
            <intent android:action="android.intent.action.VIEW"
                android:data="http://www.baidu.com" />
        </Preference>
    </com.example.extend_activity.MyPreferenceCategory>
    <com.example.extend_activity.MyPreferenceCategory
        android:title="Preference attributes">
        <CheckBoxPreference
            android:key="parent"
            android:title="Parent checkbox preference"
            android:summary="This is visually a parent"
            android:disableDependentsState="false"
            />
        <CheckBoxPreference
            android:title="Child checkbox preference"
            android:summary="This is visually a child"
            android:dependency="parent"
            />

    </com.example.extend_activity.MyPreferenceCategory>
</PreferenceScreen>


![在这里插入图片描述](https://img-blog.csdnimg.cn/2019051411435119.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMjQxNDEy,size_16,color_FFFFFF,t_70)


![在这里插入图片描述](https://img-blog.csdnimg.cn/20190514114358814.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMjQxNDEy,size_16,color_FFFFFF,t_70)
