---
title: "��Python��Tesseract����OCRʶ��ͼƬ�е�����"
keywords: ["WeFox", "Ψ������", "OCR", "Tesseract", "Python"]
date: 2018-04-24T10:43:02+08:00
draft: false
tags: ["OCR", "Tesseract", "Python"]
categories: ["Develop"]
---

## ǰ��
### ��������
- Windows 10 64bit
- Python 3.7
- Pycharm

## Tesseract���ذ�װ
TesseractĿǰ��֧�����ĺ���ʶ��ģ������ȵ�Tesseract�Ĺ���[https://github.com/tesseract-ocr](https://github.com/tesseract-ocr)�鿴Դ���˵����

��[����](https://github.com/tesseract-ocr/tesseract/wiki)�и���ϵͳ�����µİ�װ�̳̣�Tesseract֧�ִ󲿷�Linux���а棬Mac OS��Windows������

Windows�汾�İ�װ�����ص�ַ[https://github.com/UB-Mannheim/tesseract/wiki](https://github.com/UB-Mannheim/tesseract/wiki)

���غ�˫����װ����װ����ͼ��λ�õ�ʱ��ǵ���```Additional language data```�й�ѡ�������԰�

![Img](https://raw.githubusercontent.com/Wefox/wefox.github.io/master/docs/img/python_ocr_tesseract_install_1.png)

## ��Pycharm��Tesseract��ͼ��ʶ��
### ����Python��
���ȣ�������Ҫ����������
- Pillow
- Pillow_PIL
- pytesseract

������Ҫ�õ�PIL�⣬��ΪPILֻ֧�ֵ�Python2.7���������õ�Python3������������PIL���Ϻ�֧��Python3��```Pillow_PIL```�����棬�����ʱ���ȵ���```Pillow```���ٵ���```Pillow_PIL```

Pycharm�ĵ��뷽�������֣�һ������Teminal��������

    pip install Pillow
    pip install Pillow_PIL
    pip install pytesseract

����һ�ַ�������```File->Settings->Project->Project Interpreter```������ұߵ�"+"�ţ�Ȼ��˳���������⼴�ɡ�

![Img](https://raw.githubusercontent.com/Wefox/wefox.github.io/master/docs/img/python_ocr_tesseract_install_2.png)

### ģ����
Python-tesseract �ǹ�ѧ�ַ�ʶ��Tesseract OCR�����Python��װ�ࡣ�ܹ���ȡ�κγ����ͼƬ�ļ�(JPG, GIF ,PNG , TIFF��)������ɿɶ������ԡ���OCR�����ڼ䲻�ᴴ���κ����ļ�

PIL��Python Imaging Library���� Python ����õ�ͼ����⣬Image ���� PIL ����һ���ǳ���Ҫ���࣬ͨ�������������ʵ��������ֱ������ͼ���ļ�����ȡ�������ͼ���ͨ��ץȡ�ķ����õ���ͼ�������ַ�����

Python��ͼ��Ĵ���Ƚϳ���������pytesseractʶ����֤�룬Ҫ��װpytesseract�⣬�����Ȱ�װ��������PIL��tesseract-ocr������PILΪͼ����⣬�������tesseract-ocr��Ϊgoogle��ocrʶ�����棬Ҳ�������ǵ�һ���а�װ��EXE�ļ���

### OCRʶ��
��Pycharm���½�һ�����̺�Python�ļ��������м������´���

    import pytesseract
    from PIL import Image
    pytesseract.pytesseract.tesseract_cmd = r"D:\Tools\Tesseract\tesseract.exe"

    image = Image.open('temp.png')
    image.load()
    image.show()
    text = pytesseract.image_to_string(Image.open('temp.png'), lang='chi_sim')
    print(text)

������оͿ��Կ���Ч����

### Reference
https://www.cnblogs.com/wj-1314/p/9428909.html

ת����ע������