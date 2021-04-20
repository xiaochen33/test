#-*- coding: UTF-8 -*-
#!/usr/bin/python



from appium import webdriver
from time import sleep


desired_caps = {}
# 设备信息
desired_caps['platformName'] = 'Android'
desired_caps['platformVersion'] = '10'
desired_caps['deviceName'] = 'ANP0220421006198'#honor 30
# app信息
desired_caps['appPackage'] = 'org.systems.jmind.metamorph'
desired_caps['appActivity'] = '.MainActivity'
desired_caps['noReset'] = True
desired_caps['newCommandTimeout'] = '500'

# Appium服务器待appium客户端发送新消息的时间。默认为60秒  # 超时时间


driver = webdriver.Remote('http://localhost:4723/wd/hub', desired_caps)
sleep(3)

driver.find_element_by_xpath('//android.widget.FrameLayout[@content-desc="Home"]/android.widget.ImageView').click()
driver.find_element_by_xpath('//hierarchy/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.view.ViewGroup/android.widget.FrameLayout[2]/android.widget.FrameLayout/android.view.ViewGroup/android.view.ViewGroup/androidx.recyclerview.widget.RecyclerView/androidx.recyclerview.widget.RecyclerView/android.view.ViewGroup[1]/android.widget.FrameLayout/android.widget.FrameLayout/android.widget.FrameLayout[3]/android.widget.FrameLayout').click()

 #输入字符

driver.find_element_by_xpath('/hierarchy/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.view.ViewGroup/android.widget.FrameLayout[1]/android.view.ViewGroup/android.widget.FrameLayout[3]/android.view.ViewGroup/androidx.viewpager.widget.ViewPager/androidx.recyclerview.widget.RecyclerView/android.widget.FrameLayout/android.widget.RelativeLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.view.ViewGroup/android.widget.EditText').send_keys(
        "455")
sleep(2)




#点击发送
driver.find_element_by_xpath('/hierarchy/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.view.ViewGroup/android.widget.FrameLayout[1]/android.view.ViewGroup/android.widget.FrameLayout[3]/android.view.ViewGroup/androidx.viewpager.widget.ViewPager/androidx.recyclerview.widget.RecyclerView/android.widget.FrameLayout/android.widget.RelativeLayout/android.widget.LinearLayout/android.widget.FrameLayout[2]/android.view.ViewGroup/android.widget.Button').click()

sleep(1)
#点击页面空白处
driver.find_element_by_xpath('/hierarchy/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.view.ViewGroup/android.widget.FrameLayout[2]/android.widget.FrameLayout/android.view.ViewGroup/android.view.ViewGroup/androidx.recyclerview.widget.RecyclerView/androidx.recyclerview.widget.RecyclerView/android.view.ViewGroup[1]/android.widget.FrameLayout/android.widget.FrameLayout/android.widget.FrameLayout[3]/android.widget.FrameLayout').click()
#返回页面
sleep(1)
driver.find_element_by_xpath('//android.widget.FrameLayout[@content-desc="Hide player controls"]/android.widget.FrameLayout[4]/android.view.ViewGroup/android.widget.ImageButton[1]').click()

#打开小铃铛
driver.find_element_by_xpath('/hierarchy/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.view.ViewGroup/android.widget.FrameLayout[2]/android.widget.FrameLayout/android.view.ViewGroup/android.widget.LinearLayout/android.view.ViewGroup/android.widget.FrameLayout/android.widget.ImageView').click()

driver.swipe(100,700,100,300,10000)  #滑动
#点击clear all 按钮
#driver.find_element_by_xpath('/hierarchy/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.view.ViewGroup/android.widget.FrameLayout[2]/android.widget.FrameLayout/android.widget.LinearLayout/androidx.recyclerview.widget.RecyclerView/android.widget.FrameLayout/android.widget.Button').click()
#点击铃铛返回按钮

sleep(2)
driver.find_element_by_xpath('//android.widget.ImageButton[@content-desc="Navigate up"]').click()

#点击小浮窗
sleep(2)
driver .find_element_by_xpath('//android.widget.FrameLayout[@content-desc="Show player controls"]/android.widget.FrameLayout[3]/android.widget.FrameLayout/android.widget.FrameLayout')
sleep(1)

#放大小浮窗
driver .find_element_by_xpath('//android.widget.FrameLayout[@content-desc="Hide player controls"]/android.widget.FrameLayout[4]/android.view.ViewGroup/android.widget.ImageButton[3]')
sleep(2)

#点击页面空白处
driver.find_element_by_xpath('/hierarchy/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.widget.LinearLayout/android.widget.FrameLayout/android.view.ViewGroup/android.widget.FrameLayout[2]/android.widget.FrameLayout/android.view.ViewGroup/android.view.ViewGroup/androidx.recyclerview.widget.RecyclerView/androidx.recyclerview.widget.RecyclerView/android.view.ViewGroup[1]/android.widget.FrameLayout/android.widget.FrameLayout/android.widget.FrameLayout[3]/android.widget.FrameLayout').click()


#返回页面
sleep(1)
driver.find_element_by_xpath('//android.widget.FrameLayout[@content-desc="Hide player controls"]/android.widget.FrameLayout[4]/android.view.ViewGroup/android.widget.ImageButton[1]').click()
sleep(2)

#点击小浮窗
driver .find_element_by_xpath('//android.widget.FrameLayout[@content-desc="Show player controls"]/android.widget.FrameLayout[3]/android.widget.FrameLayout/android.widget.FrameLayout')

#关闭小浮窗
driver .find_element_by_xpath('//android.widget.FrameLayout[@content-desc="Hide player controls"]/android.widget.FrameLayout[4]/android.view.ViewGroup/android.widget.ImageButton[2]')
