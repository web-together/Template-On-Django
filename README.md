# Template-on-Django

django에 이미 만들어진 템플릿 적용시키기

[템플릿 예시](https://colorlib.com/wp/templates/)

적용한 Template : https://colorlib.com/wp/template/unearth/

## 주의사항 : 라이선스!

 - 공짜라고 해서 막 쓸 수 있는 건 아니다
 
## django에 template 적용시키는 순서

1. static 넣기 : static file (img, js, css 등) django의 `static` 폴더에 넣기
2. html 넣기 : `templates` 폴더에 넣기
3. html 상의 경로 맞추기 : django의 static 경로로 맞추기 
4. 만약 안되면? `settings.py` static 경로 설정 / `python manage.py collectstatic`

## Static에 대한 이해

### settings.py의 static 설정

```
# Static files (CSS, JavaScript, Images)
# https://docs.djangoproject.com/en/2.2/howto/static-files/

STATIC_URL = '/static/'
MEDIA_URL = '/products/'

# STATIC_ROOT = os.path.join(BASE_DIR, 'static')

MEDIA_ROOT = os.path.join(BASE_DIR, )

STATICFILES_DIRS = (
  os.path.join(BASE_DIR, 'static/'),
)
```

### `python manage.py collectstatic` 명령어


## 실습

1. [1단계 : 초기 setting](https://github.com/web-together/Template-On-Django/commit/b547c9710594567fcee6edb4e3929e11852587d0)
2. [2단계 : static 파일 넣기](https://github.com/web-together/Template-On-Django/commit/3418481846ad631ab3baac0d79efb90a4f96f76c)
3. [3단계 : html 갖고오기](https://github.com/web-together/Template-On-Django/commit/0d25d5baa12d2cd098b29b214acccefd8d3ac955)
4. [4단계 : 경로 맞추기](https://github.com/web-together/Template-On-Django/commit/824907596506b23f0a84c50e20bd1fec3f034b02)
5. [끝!](https://github.com/web-together/Template-On-Django/commit/e806e38a11fdb0cac575e5b956f0d033f423f267)
