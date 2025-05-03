➤ Bu projede Türkçe Tweet verileri kullanılarak metin temizleme, TF-IDF ve Word2Vec ile metin vektörleştirme işlemleri yapılmıştır.

➤ Amaç
Projenin amacı, Türkçe metin madenciliği tekniklerinin gerçek dünya sosyal medya verileri üzerinde uygulanabilirliğini göstermektir.
Bu veri seti, Türkçe sosyal medya verileri üzerinde:
· Ön işleme (temizleme),
· Stopword kaldırma,
· Noktalama işaretlerini temizleme,
· Küçük harfe dönüştürme,
· Lemmatization,
· Stemming,
· TF-IDF,
· Word2Vec,
· K-means veya benzeri gruplayıcı analizlerin nasıl uygulanabileceğini göstermek amacıyla kullanılmaktadır.

➤ Gerekli Kütüphaneler ve Kurulum
pip install pandas numpy scikit-learn gensim matplotlib nltk
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
import re
import nltk
import string
from nltk.tokenize import sent_tokenize, word_tokenize
from nltk.tokenize import word_tokenize, sent_tokenize
from nltk.corpus import stopwords
from nltk.stem import WordNetLemmatizer, PorterStemmer
from collections import Counter

➤ Modelin Nasıl Oluşturulacağı (Adım Adım)
· Veri Yükleme: TurkishTweets.xlsx dosyası data/ klasöründe yer almalıdır.
· Stopword Temizliği: Türkçe stopword listesi kullanılarak nltk ile yapılır.
· Noktalama Temizliği: Noktalama işaretleri string.punctuation ile temizlenir.
· Lowercasing: Tüm kelimeler küçük harfe dönüştürülür.
· Lemmatization: WordNetLemmatizer kullanılarak kök kelimeye indirgenir, sonuç lemmatized_sentences.csv olarak kaydedilir.
· Stemming: PorterStemmer kullanılarak kelimeler kök haline getirilir, sonuç stemmed_sentences.csv olarak kaydedilir.

➤ Öne Çıkan Kod Özellikleri
· nltk.tokenize ile cümle ve kelime ayrıştırma yapılmıştır.
· nltk.stopwords ile Türkçe sık kullanılan kelimeler filtrelenmiştir.
· str.translate ve string.punctuation kullanılarak noktalama işaretleri temizlenmiştir.
· Lemmatize edilmiş ve stem'lenmiş cümleler ayrı CSV dosyalarına kaydedilmiştir
