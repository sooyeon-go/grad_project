# Komoran 형태소 분석법을 이용한 model

1. 분석 방법
    사용 library: PyKomoran (Komoran(Java)의 Python Wrapper Class)
    https://pydocs.komoran.kr/api/python/PyKomoran.core.html
    
    기본 FULL model Komoran 객체 사용

    형태소 분석 시 get_morphes_by_tags(sentence, tag_list=None) 함수 사용
    => sentence (str) – 분석할 문장, tag_list (list) – 반환받을 품사 목록 (기본값: 전체 형태소)

0. 사용 함수
    0-1. Pandas
        pandas.read_csv: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html

    0-2. sklearn
        train_test_split: https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html