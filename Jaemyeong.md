# Choi, Jaemyeong's project
## 데이터프로그래밍 응용 수업 과제

**깃허브 사용법**을 익히고, 추후 프로젝트에 대비한다.

깃허브에서 파이썬 크롤러 코드를 짜고 관리 예정

~~~ #!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Wed Sep  6 14:07:11 2017

@author: Jaemyeong
"""

# 네이버TV 댓글 크롤링

from selenium import webdriver
from bs4 import BeautifulSoup

driver = webdriver.Chrome('/Users/guest/Documents/chromedriver')

driver.implicitly_wait(3)
driver.get('http://tv.naver.com/jtbc.youth2/clips')

for i in len(range(1, 100, 1)):
    driver.find_element_by_xpath('//*[@class="item_paging"]').click()

html = driver.page_source
soup = BeautifulSoup(html, 'html.parser')

url = soup.find_all(a, ) '''
