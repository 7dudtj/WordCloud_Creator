# :cloud:WordCloud_Creator

- 워드클라우드 생성기
- 핵심 단어 시각화

---

## :zap:What is Word Cloud Creator?

<p align="center">
  <img width="600" src="https://user-images.githubusercontent.com/67851701/194755503-27fb1f3f-9d6a-46b9-ab82-6ab7e148c373.png">  
</p>

핵심 키워드에 대하여 사람들은 어떠한 생각을 하고 있을까요?  
핵심 키워드는 오늘날 어떠한 이미지를 가지고 있으며, 어떠한 키워드와 관련이 있을까요?  

**Word Cloud Creator**는 주어진 핵심 키워드에 대한 워드클라우드를 생성합니다!  
Word Cloud Creator를 통해 누구나 쉽고 빠르게 워드클라우드를 생성할 수 있으며  
핵심 키워드에 대한 직관적인 시각화가 가능합니다!  

---

## :slot_machine:How it works?

**Word Cloud Creator**는 다음과 같은 방식으로 작동합니다.  

1. 주어진 키워드를 네이버에 검색합니다.  
2. 검색된 뉴스들의 제목들을 크롤링합니다.  
3. Komoran 한국어 형태소 분석기를 이용하여 수집한 데이터를 분석합니다.  
4. Mask Image 위에 분석된 결과들을 시각화합니다.  
5. Word Cloud가 완성되었습니다!  

---

## :rainbow:How to use?

1. **Word Cloud Creator**를 clone하고, requirements를 설치합니다.  
```
git clone https://github.com/7dudtj/WordCloud_Creator.git
cd WordCloud_Creator
pip install -r requirements.txt
```
2. Mask Image로 사용하고자 하는 이미지를 Mask 폴더에 저장합니다.  
3. WordCloud.ipynb 파일에서 User setting variables(사용자 설정 변수)를 설정합니다.  
```
headers = {'User-Agent': '...'}
keyword = '...'
numbers = ...
FONT_PATH = "..."
mask = np.array(Image.open('...'))
```
4. WordCloud.ipynb 파일을 실행합니다.
5. 생성된 워드클라우드 이미지는 Image 폴더에 저장됩니다.  
뉴스 제목 크롤링 데이터는 Data 폴더에 저장됩니다.  

---

## :book:Comments from developer

* Mask, Data, Image 폴더에 샘플 5개가 들어있습니다.  
* 같은 키워드로 생성하더라도, 생성 시점에 따라 결과는 다르게 나올 수 있습니다.  
* konlpy 라이브러리 이용을 위해서는 JDK가 설치되어있어야 합니다.  
* 애플 실리콘을 사용하는 중 konlpy 라이브러리에서 버그가 발생할 경우, Oracle JDK를 설치하고 Java 환경변수를 Oracle JDK로 설정하면 버그가 해결될 수 있습니다.  

---

## :copyright:Copyleft / End User License
<details>
<summary>
내용 보기
</summary>
<div markdown="1">
<img align="right" src="http://opensource.org/trademarks/opensource/OSI-Approved-License-100x137.png">

The class is licensed under the [MIT License](http://opensource.org/licenses/MIT):

Copyright &copy; 2022 [7dudtj](https://github.com/7dudtj).

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
  </div>
  </details>

