---
author_profile: true
sidebar: 
  nav: main

layout: home
permalink: /
hidden: true
# header:
#   overlay_color: "#5e616c"
#   overlay_image: /assets/images/mm-home-page-feature.jpg

# excerpt:
feature_row_left_retrospect:
  - image_path: /assets/images/회고.png
    # alt: "customizable"
    title: "2022 회고"
    excerpt: "기간별로 학습한 내용과 <br>느꼈던 감정들에 대해 <br>정리했습니다."
    url: "https://sjuhan123.github.io/TIL/categories/#cs50:~:text=BACK%20TO%20TOP%20%E2%86%91-,2022%2D%ED%9A%8C%EA%B3%A0,-%EC%BD%94%EB%93%9C%EC%8A%A4%EC%BF%BC%EB%93%9C%20%ED%94%84%EB%A6%AC%EC%BD%94%EC%8A%A4%20~%202022"
    btn_class: "btn--primary"
    btn_label: "Read more"

feature_row_left_bookstudy:
  - image_path: /assets/images/서적공부.png
    # alt: "customizable"
    title: "JS 참고서"
    excerpt: "JS 참고서를 읽고 <br>내용을 정리했습니다."
    url: "https://sjuhan123.github.io/TIL/categories/#cs50:~:text=1-,javascript,-%EC%BD%94%EC%96%B4%20%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%20%2D%20%EB%8D%B0%EC%9D%B4%ED%84%B0"
    btn_class: "btn--primary"
    btn_label: "Read more"
feature_row_left_algorithm:
  - image_path: /assets/images/알고리즘.png
    # alt: "customizable"
    title: "Algorithm"
    excerpt: "알고리즘 문제를 풀고 <br>어떤 방식으로 풀었는지 <br>정리 했습니다."
    url: "https://sjuhan123.github.io/TIL/categories/#cs50:~:text=BACK%20TO%20TOP%20%E2%86%91-,Algorithm,-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%A8%B8%EC%8A%A4%20Lv.0"
    btn_class: "btn--primary"
    btn_label: "Read more"
---
{% include feature_row id="feature_row_left_retrospect" type="left" %}
{% include feature_row id="feature_row_left_bookstudy" type="left" %}
{% include feature_row id="feature_row_left_algorithm" type="left" %}