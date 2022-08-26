---
title: "日本人英語学習者の文理解における色表象の活性化-言語間比較と習熟度の観点から-"
subtitle: "D2報告会 February 3rd, 2022"
author: "*Masato Terai*"
date: "最終更新: `r Sys.time()`"
output: 
  ioslides_presentation:
    css: bootstrap.css
    widescreen: true
    smaller: false
    font_adjustment: +2 #font size
editor_options: 
  chunk_output_type: console
  markdown: 
    wrap: 72
---

```{r setup, include=FALSE, tidy=TRUE}
knitr::opts_chunk$set(
  echo = TRUE,
  fig.align = 'center'
)
# knitr::opts_knit$set(root.dir = '/tmp')
```

```{=html}
<style>
  slides > slide {
    overflow-x: auto !important;
    overflow-y: auto !important;
  }
  .emphasized {
  font-size: 5em;
}
</style>
```
```{r message=FALSE, warning=FALSE, tidy=TRUE, include=FALSE}
library(tidyverse)
library(lme4)
library(lmerTest)
library(sjPlot)
library(plotly)
library(qqplotr)
library(ggpubr)
library(ggmosaic)
library(kableExtra)
library(fitdistrplus)
```

## 研究の目的

-   外国語においても、母語のように言語表現が示すものを活性化しながら理解を行うかを明らかにする

    -   日本のように外国語として英語を学習する環境
    -   外国語：教室内での記号的な操作による学習（*Dog* = 犬）

# 先行研究

## 身体化認知研究（基盤化された認知）

### 知覚的シンボルシステム（Perceptual Symbol System:PSS）

-   シミュレーション：周囲の環境、身体、心を通し、獲得された表象の再現（[Barsalou,
    2008](https://bit.ly/3IN8Gn1)）

-   言語理解においても、発話や書き言葉が表す意味を表象するためにシミュレーションを行う（[Barsalou,
    1999](https://bit.ly/3g1wG9M)）

![「イス」の理解プロセス](https://drive.google.com/uc?export=view&id=1wIWTbF2X2MVGODcnUuCJRBqcwbqbG6Ed "「イス」の理解プロセス"){width="80%"}

## 知覚的シンボルシステムの妥当性

-   母語の研究

-   以下の物体の視覚特徴をシミュレーションする

    -   形 e.g., [Zwaan et al. (2002)](https://bit.ly/3qztk4u)

    -   方向 e.g., [Zwaan and Pecher (2012)](https://bit.ly/3oo0nFO)

    -   色 e.g., [Connell & Lynott (2009)](https://bit.ly/3CEGxeU)

## [Connell and Lynott (2009)](https://bit.ly/3CEGxeU)

### 色の表象

-   文理解におけるシミュレーション

-   意味ストループ課題

    -   文章を読んだ直後に提示される単語の色を読み上げる
    -   文章内で暗示された単語の色 = 提示された単語の色 -\>
        読み上げ速度が速くなる

<center>

![](https://drive.google.com/uc?export=view&id=1HVDAfURpTxDLfDzeFTC8H1R3_xbm1KbH){width="60%"}

</center>

## イメージの内容

-   シミュレーションでは複数の色が表象されるか？

    -   茶色のクマ（典型）
    -   白色のクマ (非典型)
    -   黄色のクマ（現実にはあり得ない）

<center>

![](https://drive.google.com/uc?export=view&id=13uK4EHsjihw1Rb-NxEIAOjZwPOkcxuhm){width="60%"}

</center>

## 先行研究の課題

### 母語の研究

-   文脈を先に定義すると一つの色表象しか活性化できない？

    -   [Connell and Lynott (2009)](https://bit.ly/3CEGxeU)

    -   実験で使用された20文のうち、そのほとんどがキーワードの後ろに文脈（16文）

        -   後） *Joe was excited to see **a bear** [in the woods/at the
            North Pole].*

        -   前） *Susan liked it with her [granddaughter/grandmother]
            wore her **hair** up*

## [Sato et al. (2013)](https://bit.ly/3Gh3czl)

### 文-画像判断課題

-   文の途中（動詞を処理する前に）でも言語表現が示す表象は活性化

-   表象は文脈により即座にアップデートされる

    -   「ななが冷蔵庫の中に卵を素早く落とした」
    -   「卵」を処理するまでは割れていない卵
    -   「落とした」を処理すると割れた卵

-   疑問

    -   最初に文脈が定義されている場合はどうなる?

-   **現在**

    <center>

    ![](https://drive.google.com/uc?export=view&id=1MgHdo1NBCMehO9f2rSt1VSman4TAAqez){width="60%"}

    </center>

    <br>

-   **変更後**

    <center>

    ![](https://drive.google.com/uc?export=view&id=1VU9iYDOnHJ4eEijpBtORx9HHATWsk1lw){width="60%"}

    </center>

## 外国語の研究

-   シミュレーションの有無の研究

    -   L2でも知覚運動表象が活性化

        -   e.g., [Buccino et al. (2017)](https://bit.ly/3KSesWq) :
            触りやすさ（触覚）
        -   **高熟達度**の学習者
        -   [粟津・鈴木(2020)](https://bit.ly/3IX53LF)：（動詞）
        -   日本人**低熟達度**の学習者

    -   L2では活性化しない

        -   [Norman and Peleg (2021)](https://bit.ly/3IQbWhJ): 視覚

-   外国語でも母語のような処理を行うか?

    -   習熟度の向上とともにシミュレーションの**程度**や**内容**は母語に近づくか

## 研究課題

1.  母語において、[Connell and Lynott
    (2009)](https://bit.ly/3CEGxeU)の結果は再現できるか

    -   文脈の位置の影響はあるか

2.  外国語においても色表象の活性化は行われているのか

    -   外国語の文理解の際に活性化する色表象は、指示対象一つにつき一つか

3.  外国語の習熟度の高低によって，活性化する色表象の程度・内容は変化するか

# 本研究

## 仮説

1.  **母語**で課題を行う場合、[Connell and Lynott
    (2009)](https://bit.ly/3CEGxeU)が再現できる

    -   文脈が**前**に定義される場合、常に文が示す色と単語の色が一致している場合のみ速度が速い

2.  & 3. 日本人が**英語**で課題を行う場合

    -   習熟度によって、条件間の速度の差は異なる

        -   英語の習熟度が高いと、母語での反応に近づくため、条件間の速度の差が大きくなる

## 研究全体の計画

1.  研究１：**英語母語話者**に*英語*で意味ストループ課題

2.  研究２：**日本人英語学習者**に*日本語*で意味ストループ課題

    =====研究課題１の検証課題=====

3.  研究３：**日本人英語学習者**に*英語*で意味ストループ課題

    =====研究課題2の検証課題=====

# 本実験

## 実験素材

-   二回の予備実験で項目を作成

-   360の文（英語版と日本語版）

    -   実験文：180文（文脈前: 90文、文脈後: 90文）

        -   2（文章の種類） × 3（単語の色の種類）= 6条件

            -   15（キーワード） × 6条件 = 90文

    -   フィラー文：180文（文脈前: 90文、文脈後: 90文）

        -   全ての実験文はこちらの[OSFのページ](https://osf.io/hjrma/?view_only=cfcd339a544e4f7d93c845571014da7d)に掲載

+----------------------+-----------------------+-----------------------+
|                      | 文脈の位置            | 文脈の位置            |
+======================+:=====================:+:=====================:+
| **文章の種類**       | 前                    | 後ろ                  |
+----------------------+-----------------------+-----------------------+
| 典型                 | **In the woods,** Joe | Joe was excited to    |
|                      | was excited to see *a | see *a bear* **in the |
|                      | bear*.                | woods**.              |
+----------------------+-----------------------+-----------------------+
| 非典型               | **At the North        | Joe was excited to    |
|                      | Pole,** Joe was       | see *a bear* **at the |
|                      | excited to see *a     | North Pole**.         |
|                      | bear*.                |                       |
+----------------------+-----------------------+-----------------------+

: 刺激文の例

## 手順

-   [意味ストループ課題](https://youtu.be/oROfQVYQs6c)

    -   Set 1 (文脈**前**の実験文　+ 文脈**後ろ**のフィラー) or
        (文脈**後ろ**の実験文　+ 文脈**前**のフィラー)

    -   [冠詞穴埋め課題](https://youtu.be/5_eoGb-ZicI)（一定の時間を空けるため）

        -   日本人に行う場合、ここを[英単語テスト](https://www.lognostics.co.uk/tools/V_YesNo/V_YesNo.cgi)に変更

    -   Set 2 (文脈**後ろ**の実験文　+ 文脈**前**のフィラー) or
        (文脈**前**の実験文　+ 文脈**後ろ**のフィラー)

-   単語のイメージ判断課題

-   文章のイメージ判断課題

-   アンケート

## 参加者の数の決定

### 検定力分析

-   Cohen (1988)の効果量 *d* をもとに検定力を算出した。

-   効果量を小さく設定（*d* = 0.2）。

-   1人当たりの項目数が180の場合、**44名**で検定力80%を満たす。

```{r, warning=FALSE, echo=FALSE,include=FALSE}
    #install.packages("sjstats", dependencies = T)
    library(sjstats)
    power.sjstats <- sjstats::samplesize_mixed(
    eff.size = 0.2, #effect size
    df.n = NULL, #degree of freedom
    power = 0.8,
    sig.level = 0.05,
    k = NULL, #LEVEL2が参加者で、ここを推定したいからNULLに
    n = 180, #Optionalだが、k = NULLならここは必須, number of observations per cluster groups
    icc = 0.05 #Expected intraclass correlation coefficient for multilevel-model.
    )

    power.sjstats
    power.sjstats$`Total Sample Size`
```

```{r,include=FALSE}
power.sjstats$`Total Sample Size`/ 180 #Required observations / the number of items
```

# 本実験の経過報告（研究１）

## 研究課題1：[Connell & Lynott (2009)](https://bit.ly/3CEGxeU)の追試

### 英語母語話者

-   23名からデータ収集を完了。以下のデータは除外 (2022/02/03現在)

    -   ID 5: システムエラー
    -   ID 16: English as **Primary** speaker
    -   ID 17: Set 2 (保存されていなかった)

# 評価課題の分析

```{r, tidy=TRUE, include=FALSE}
files <- list.files(path = "C:/Users/mtera/Documents/Terai_color/Main_Color/color_Nativespeaker_main_experiment/data/Stroop_Color_Native/", pattern = "EN_main")

setwd("C:/Users/mtera/Documents/Terai_color/Main_Color/color_Nativespeaker_main_experiment/data/Stroop_Color_Native/")

bind_data <- NULL
for (i in 1:length(files)) {
  all_data <- read.table(files[i],sep = "\t", fill = TRUE, quote = "", skip = 1)
  bind_data <- rbind(bind_data, all_data)
}

bind_data <- bind_data[,-1]

colnames(bind_data) <- c("SubjectID", "ItemID","Set","Position","Trials", "Sentence","Type","Sentence.Typicality",
                           "Word","Word.Typicality", "Correct.Answer","Combination","Comprehension.question","Comprehension.answer", "Stroop.responce", "RT.Stroop","Responce.Color","RT.Sentence","Comprehension.responce","RT.comprehension")
```

```{r, tidy=TRUE, include=FALSE}
setwd("C:/Users/mtera/Desktop/")
dat_word_rating <- read.csv("Rating.csv", header = T, encoding = "UTF-8")[,-c(1,2)]
```

```{r, tidy=TRUE, include=FALSE}
  word_rating <- NULL
  header <- names(dat_word_rating[,-1])
    for (i in 1:(length(header))) {
        dat_word_rating %>%
        dplyr::select(ID, i + 1) -> eachdata
        eachdata[,3] <- header[i]
        word_rating <- rbind(word_rating, sapply(eachdata, as.character))
    }
   all_word_data <- as_tibble(word_rating)
   colnames(all_word_data) <- c("ID", "rating", "Item")
   
   all_word_data <- all_word_data %>%
     tidyr::separate(Item, into = c("a", "color", "word"), sep = "\\.") %>%
     dplyr::select(-a)
   
    referencelist.word <- bind_data %>%
        dplyr::filter(SubjectID == 1) %>%
        dplyr::filter(Position == "Post") %>%
        dplyr::filter(Combination == "typical-typical" | Combination == "typical-atypical"| Combination == "typical-unrelated") %>%
        dplyr::select(Word, Word.Typicality, Correct.Answer)
    
    referencelist.word$Word %>%
        stringr::str_to_lower()
    
    colnames(referencelist.word) <- c("word","typicality.of.the.word","The color of the Word")
    
    all_word_data <- all_word_data %>%
        mutate(typ.word = paste(!!!rlang::syms(c("color","word")), sep="-"))
    
   referencelist.word <- referencelist.word %>%
        mutate(typ.word = paste(!!!rlang::syms(c("The color of the Word","word")), sep="-"))
    
    all_word_data.new <- all_word_data %>%
       dplyr::left_join(referencelist.word, by = "typ.word") 
    
    all_word_data.new <- all_word_data.new [,-c(6,8)]
    colnames(all_word_data.new) <- c("SubjectID", "Rating.Score", "Color", "Word", "Color-Word", "Typicality")
```

## 評価値（単語単体）

-   Typicalの評価値はAtypicalよりも高いことが望ましい。

-   Atypicalの評価値はUnrelatedよりも高いことが望ましい。

-   Unrelatedの評価値は1から2が望ましい。

-   **Onion**のみAtypical \> Typical

    -   以下の図では、評価値の平均が2未満の行に色を塗った。

```{r, tidy=TRUE, echo=FALSE}
all_word_data.new$Rating.Score <- as.numeric(all_word_data.new$Rating.Score)
all_word_data.new <- all_word_data.new %>%
  mutate(Typicality = fct_relevel(Typicality, "typical","atypical", "unrelated"))
    

  all_word_data.new %>%
    group_by(Word, `Color-Word`,Typicality) %>%
    summarize(mean = round(mean(Rating.Score), 2), 
              sd = round(sd(Rating.Score),2),
              .groups = "drop") %>%
    arrange(Word,Typicality) %>%
    mutate(mean = as.numeric(mean)) %>%
    mutate(sd = as.numeric(sd)) -> Ratings.new
  
  Ratings.new %>%
    kableExtra::kbl( 
               digits = 2, 
               align = "c", 
                booktabs = T,
               caption = "The rating scores of each words") %>%
    kable_styling(bootstrap_options = c("striped", "hover"),
                full_width = T) %>%
    # cell_spec(color = case_when(
    #   Ratings.new$mean >= 4 ~ "blue",
    #   Ratings.new$mean >=2 & Ratings.new$mean < 4 ~"red",
    #   Ratings.new$mean >=1 & Ratings.new$mean < 2 ~ "yellow")) 
    row_spec(which(Ratings.new$mean < 2 ), background  = "lightblue")
  #参考：https://community.rstudio.com/t/conditional-formatting-with-column-spec-within-a-dplyr-chain/84347/4
    
```

## 評価値（文単位)

### 典型性の評価

-   選択肢は4つ。したがって、平均が**25%**以下の項目は文単位の典型性の妥当性が疑われる

    -   評価値が**低い**順に並び替えた上位5つを表示している。

```{r, tidy=TRUE, include=FALSE}
setwd("C:/Users/mtera/Desktop/")
dat_A_main <- read.csv("sentenceA_main.csv", header = T, encoding = "UTF-8")[,-c(1,2)]
dat_B_main <- read.csv("sentenceB_main.csv", header = T, encoding = "UTF-8")[,-c(1,2)]
```

```{r, tidy=TRUE, include=FALSE}
  sentence_A <- NULL
  header <- names(dat_A_main[,-1])
    for (i in 1:(length(header))) {
        dat_A_main %>%
        dplyr::select(ID, i + 1) -> eachdata
        eachdata[,3] <- header[i]
        sentence_A <- rbind(sentence_A, sapply(eachdata, as.character))
        }

  sentence_B <- NULL
  header <- names(dat_B_main[,-1])
    for (i in 1:(length(header))) {
        dat_B_main %>%
        dplyr::select(ID, i + 1) -> eachdata
        eachdata[,3] <- header[i]
        sentence_B <- rbind(sentence_B, sapply(eachdata, as.character))
        }

  all_sentence_data <- as_tibble((rbind(sentence_A, sentence_B)))

  colnames(all_sentence_data) <- c("ID", "ratings", "sentence")
    
  all_sentence_data$ratings <- as.factor(all_sentence_data$ratings)
  pacman::p_load(forcats)
  fct_list <- c("typical" = "best matched by Picture 1",
                "atypical" = "best matched by Picture 2",
                "both" = "matched by both pictures equally",
                "neither" = "matched by neither picture")
  
  #Picture 1 is always typical object.
  #Picture 2 is always atypical object.
  all_sentence_data <- all_sentence_data %>% 
  dplyr::mutate(ratings = fct_recode(ratings, !!!fct_list))
  
  all_sentence_data$sentence <- gsub("\\.", " ", all_sentence_data$sentence)
 
  #Encoding等の関係でハイフンなどが消えたりしたものを修正
  pacman::p_load(forcats)
  fct_list <- c(
    "Ben popped a piece of popcorn in his mouth and it tasted sour " = "Ben popped a piece of popcorn in his mouth  and it tasted sour ",
    "Ben popped a piece of popcorn in his mouth and it tasted sweet " = "Ben popped a piece of popcorn in his mouth  and it tasted sweet ",
    "The strawberry that Mark bought looked ready to eat " = "The strawberry that Mark bought looked ready to eat ",
    "The strawberry that Mark bought didn't look ready to eat " = "The strawberry that Mark bought didn t look ready to eat ",
    "The teacher pointed to the chameleon lying camouflaged in the grass " = "The teacher pointed to the chameleon lying camouflaged in the grass ",
    "The teacher pointed to the chameleon lying camouflaged in the sand  " = "The teacher pointed to the chameleon lying camouflaged in the sand ",
    "John looked at the steak on his plate " = "John looked at the steak on his plate ",
    "John looked at the steak in the meat-shop " = "John looked at the steak in the meat shop ",
    "Lynn ordered a cake for Valentine's Day " = "Lynn ordered a cake for Valentine s Day ")
  all_sentence_data <- all_sentence_data %>% 
  dplyr::mutate(sentence = fct_recode(sentence, !!!fct_list))
  
  referencelist <- bind_data %>%
    dplyr::filter(SubjectID == 1) %>%
    dplyr::filter(Position == "Post") %>%
    dplyr::filter(Combination == "typical-typical" | Combination == "atypical-atypical") %>%
    dplyr::select(ItemID, Word,Sentence, Sentence.Typicality)
   referencelist$referencelist <- gsub("\\.", " ", referencelist$Sentence)
   referencelist <- tibble(referencelist)[,-3]
   colnames(referencelist) <- c("ItemID","word","typicality.of.the.sentence","sentence")
  
  all_sentence_data.new <- all_sentence_data %>%
     dplyr::left_join(referencelist, by = "sentence") 
  
  all_sentence_data.new <- all_sentence_data.new %>%
    mutate(typ.sen = paste(!!!rlang::syms(c("typicality.of.the.sentence","word")), sep="-")) %>%
    mutate(order = paste(!!!rlang::syms(c("word", "typicality.of.the.sentence")), sep="-"))
 
  #factor方のままだと、因子の数が合わないと怒られるのでcharacterに変更してからmatchさせる 
  all_sentence_data.new$ratings <- as.character(all_sentence_data.new$ratings)
  all_sentence_data.new$typicality.of.the.sentence <- as.character(all_sentence_data.new$typicality.of.the.sentence)
  
  all_sentence_data.new <- all_sentence_data.new  %>%
    mutate(match = if_else(typicality.of.the.sentence == ratings, "1", "0")) 
  
  all_sentence_data.new <- all_sentence_data.new  %>%
    mutate(typicality.of.the.sentence = fct_relevel(typicality.of.the.sentence, "typical","atypical")) %>%
    mutate(ratings = fct_relevel(ratings, "typical","atypical", "both", "neither")) 
```

```{r, tidy=TRUE, echo=FALSE}
  balloon.plot <- all_sentence_data.new %>%
    group_by(typ.sen,ratings,order) %>%
    summarize(n = n(),
              .groups = "drop") %>%
    arrange(n)
```

```{r, echo=FALSE}
  all_sentence_data.new$match <- as.numeric(all_sentence_data.new$match)

  Matchtypicality <- all_sentence_data.new %>%
    group_by(order) %>%
    summarise(mean = round(mean(match), 3)*100, 
              sd = round(sd(match),3),
              .groups = "drop") %>%
    arrange(mean)

  kableExtra::kbl(Matchtypicality[1:5,], 
               digits = 2, 
               align = "c", 
                booktabs = T,
               caption = "The typicalities of each sentences ( % )") %>%
    kable_styling(bootstrap_options = c("striped", "hover"),
                full_width = T) %>%
   row_spec(which(Matchtypicality$mean < 25 ), background  = "lightblue")
```

## 意味ストループ課題

### 全体の正答率

```{r, tidy=TRUE, include=FALSE}
files <- list.files(path = "C:/Users/mtera/Documents/Terai_color/Main_Color/color_Nativespeaker_main_experiment/data/Stroop_Color_Native/", pattern = "EN_main")

setwd("C:/Users/mtera/Documents/Terai_color/Main_Color/color_Nativespeaker_main_experiment/data/Stroop_Color_Native/")

bind_data <- NULL
for (i in 1:length(files)) {
  all_data <- read.table(files[i],sep = "\t", fill = TRUE, quote = "", skip = 1)
  bind_data <- rbind(bind_data, all_data)
}

bind_data <- bind_data[,-1]

colnames(bind_data) <- c("SubjectID", "ItemID","Set","Position","Trials", "Sentence","Type","Sentence.Typicality",
                           "Word","Word.Typicality", "Correct.Answer","Combination","Comprehension.question","Comprehension.answer", "Stroop.responce", "RT.Stroop","Responce.Color","RT.Sentence","Comprehension.responce","RT.comprehension")
```

```{r, tidy=TRUE, include=FALSE}
#Next, load in the data and convert data frame to tibble.  
bind_data <- as_tibble(bind_data) ### Convert to tibble
bind_data$SubjectID <- as.factor(bind_data$SubjectID)
bind_data$ItemID <- factor(bind_data$ItemID)
bind_data$Set <- as.factor(bind_data$Set)
bind_data$Position <- as.factor(bind_data$Position)
bind_data$Pres.Order <- as.numeric(bind_data$Trials)
bind_data$Type <- as.factor(bind_data$Type)
bind_data$Sentence.Typicality <- factor(bind_data$Sentence.Typicality)
bind_data$Word.Typicality <- factor(bind_data$Word.Typicality)
bind_data$Combination <- as.factor(bind_data$Combination)
bind_data$Stroop.res <- factor(bind_data$Stroop.responce)
bind_data$RT.Stroop <- as.numeric(bind_data$RT.Stroop)
bind_data$Comp.res <- as.numeric(bind_data$Comprehension.responce)
head(bind_data) ### Overview of the data
```

```{r, tidy=TRUE,echo=FALSE}
knitr::kable(table(bind_data$Stroop.res),
             col.names = c("Correct / Incorrect", "Raw Frequency"),
             digits = 2,
             align = "c",
             caption = "English") %>%
  kable_styling(bootstrap_options = c("striped", "hover"),
                full_width = T)
```

```{r, tidy=TRUE, include=FALSE}
bind_data %>% 
  filter (!is.na(Comprehension.responce)) %>%
  group_by(SubjectID) %>%
  summarize(Comp.res = mean(Comprehension.responce)) %>% arrange(Comp.res) 
```

```{r, tidy=TRUE, include=FALSE}
bind_data %>%
    filter(Type == "target") %>%
    group_by(Word) %>%
    summarise(mean = mean(RT.Stroop), 
              sd = sd(RT.Stroop),
              .groups = "drop") %>%
    arrange(mean)
```

```{r, tidy=TRUE, include=FALSE}
bind_data %>% 
  filter(Type == "target") -> EN.target
```

## 全体の傾向

```{r echo=FALSE, fig.dim = c(10, 6)}
EN.target %>%
  ggplot(mapping = aes(x = RT.Stroop, y= ..density..)) +
    geom_histogram(alpha = 0.5, bins = 20) +
    geom_density(size = 1.5) +
  scale_x_continuous(breaks = seq(0,4000,500)) +
  coord_cartesian(xlim = c(0,4000)) +
  scale_fill_viridis_d()  +
  labs(y="密度") +
  labs(x="反応速度（ミリセカンド）") +
   labs(title = "反応速度の分布")

```

## 理論的確率分布と観測された確率分布
- ヒストグラム：観測されたデータ
- 赤い線：正規分布における最尤推定で母数を推定した確率密度曲線
```{r, echo=FALSE, warning=FALSE, fig.dim = c(10, 6)}
#From (https://bit.ly/3scVlxV)

set.seed(0)

#それぞれの分布をフィットさせる
norm <- fitdist(EN.target$RT.Stroop,"norm")

plot(norm)
```

## 参加者のデータの概要（個別）

```{r, echo=FALSE, tidy=TRUE, warning=FALSE, message =FALSE,fig.dim = c(10, 6)}

EN.target %>%
  ggplot(aes(x= Trials, y= RT.Stroop, colour = Set)) +
  geom_point() +
  stat_smooth(method = 'loess', level = 0.95) +
  ylim(0,3500) +
  facet_wrap(~SubjectID) +
  scale_fill_viridis_d() +
  labs(y="反応速度（ミリセカンド）") +
  labs(x="試行数") +
  labs(fill = "Set") +
  labs(title = "反応速度と試行数")

```

## データ・クリーニング

-   以下の条件に該当するデータは、以下の分析には含まれていない

    -   不正解の正答 <br>

    -   フィラー項目 <br>

    -   内容理解課題の全体の正答率が**50%未満**の参加者の**すべて**のデータ
        <br>

    -   ストループ課題の全体の正答率が**80%未満**の参加者の**すべて**のデータ
        <br>

    -   正答率・反応速度が、*± 3 median absolute
        deviations*離れている項目 <br>

-   以上の条件は [Horchak and Garrido
    (2020)](https://bit.ly/3zALIdQ)を参考にした

```{r, warning=FALSE, tidy=TRUE,include=FALSE}
bind_data %>%
  filter(!is.na(Comprehension.responce)) %>%
  filter(!is.na(Stroop.responce)) %>%
  group_by(SubjectID) %>%
  summarize(Comp.res = mean(Comprehension.responce), Stroop.res = mean(Stroop.responce), .groups = "drop") %>%
  filter(Comp.res < 0.5 | Stroop.res < 0.8) -> excluded


excluded$SubjectID

bind_data %>%
  filter(Type != "filler") %>%
  filter(RT.Stroop != 0) %>%
  filter(Stroop.res == 1) %>%
  #filter(SubjectID != "5") %>%
  filter(RT.Stroop < 3*mad(RT.Stroop)) %>%
  filter(RT.Stroop > -3*mad(RT.Stroop)) -> EN.model

```

## クリーニング後のデータ
- あくまで暫定的なクリーニング
- 外れ値とエラーの区別が重要 [(新井・Roland, 2016)](https://bit.ly/3sc3EKr)
  -   決定係数を見ながらのクリーニング
```{r, echo=FALSE, tidy=TRUE, warning=FALSE, message =FALSE,fig.dim = c(10, 6)}

EN.model %>%
  ggplot(aes(x= Trials, y= RT.Stroop, colour = Set)) +
  geom_point() +
  stat_smooth(method = 'loess', level = 0.95) +
  ylim(200,1000) +
  facet_wrap(~SubjectID) +
  scale_fill_viridis_d() +
  labs(y="反応速度（ミリセカンド）") +
  labs(x="試行数") +
  labs(fill = "Set") +
  labs(title = "反応速度と試行数")

```

## クリーニング後の分布

```{r, echo=FALSE, fig.dim = c(10, 6)}
EN.model %>%
  ggplot(mapping = aes(x = RT.Stroop, y= ..density..)) +
    geom_histogram(alpha = 0.5, bins = 20) +
    geom_density(size = 1.5) +
    scale_x_continuous(breaks = seq(0,900,50)) +
    coord_cartesian(xlim = c(300,900)) +
    scale_fill_viridis_d()  +
    labs(y="密度") +
    labs(x="反応速度（ミリセカンド）") +
    labs(title = "反応速度の分布（クリーニング後）")

# Fit parameters (to avoid errors, set lower bounds to zero) (https://bit.ly/3unnwNc)
```

## 確率分布を特定
-   観測したデータにワイブル分布とガンマ分布、対数正規分布、正規分布を適合させた
-   書く統計量および情報量基準は、*小さい*指標がよい
-   ワイブル分布もしくは正規分布が観測に対し最も優れた適合を示している
```{r, echo=FALSE, warning=FALSE, fig.dim = c(10, 6)}
#From (https://bit.ly/3scVlxV)

set.seed(0)

#それぞれの分布をフィットさせる
wei <- fitdist(EN.model$RT.Stroop,"weibull") 
gam<-fitdist(EN.model$RT.Stroop,"gamma")
logn<-fitdist(EN.model$RT.Stroop,"lnorm")
norm <- fitdist(EN.model$RT.Stroop,"norm")

#比較（リストで入れる）
pl <- gofstat(list(wei ,gam, logn, norm), fitnames=c("weibull", "gamma",
"lognormal", "norm"))

info <- data.frame(rbind(pl$ks, pl$cvm,pl$ad,pl$aic, pl$bic))
colnames(info) <- c("ワイブル分布", "ガンマ分布", "対数正規分布", "正規分布")
rownames(info) <-c("コルモゴロフ・スミルノフ統計量","クラメール・フォンミーゼス統計量","アンダーソン・ダーリング統計量",
                   "赤池情報量基準", "ベイズ情報量基準")

info %>%
kableExtra::kbl(digits = 3) %>%
  kable_styling(
    bootstrap_options = c("striped"),
                full_width = T) %>%
  column_spec(2, #色を塗る列を指定
              background = "lightblue") %>%
    column_spec(5, #色を塗る列を指定
              background = "lightblue")
```

## 作図（正規分布）
- ヒストグラム：観測されたデータ
- 赤い線：正規分布における最尤推定で母数を推定した確率密度曲線
```{r,echo=FALSE, fig.dim = c(10, 6)}
par("mar"=c(1,1,1,1))

plot(norm)
```

# 反応速度：ストループ課題

## 研究課題1（先行研究の結果は再現できるか）

### 反応速度（英語：実験項目：文脈後）

-   予測

1.  典型的な文 - 典型的な単語の色
2.  非典型的な文 - 非典型的な単語の色
3.  非典型的な文 - 典型的な単語の色
4.  典型的な文 - 非典型的な単語の色
5.  典型的な文 - ありえない単語の色
6.  非典型的な文 - ありえない単語の色

-   エラーバーは測定誤差

    -   クリーニング後のデータ

```{r, tidy=TRUE,echo=FALSE}
pacman::p_load(forcats)

fct_list.two <- c("典型-典型" = "typical-typical",
                  "典型-非典型" = "typical-atypical", 
                  "典型-ありえない" = "typical-unrelated", 
                  "非典型-非典型" = "atypical-atypical",
                  "非典型-典型" = "atypical-typical", 
                  "非典型-ありえない" = "atypical-unrelated")

Post.RT.percon <- EN.model %>%
  mutate(Combination = fct_recode(Combination, !!!fct_list.two)) %>%
  filter(Position == "Post") %>%
  group_by(Combination) %>%
  summarise(n_acc = n(),mean_acc=round(mean(RT.Stroop),2),sd_acc=sd(RT.Stroop),.groups = "drop") %>%
   mutate(se.acc = sd_acc/sqrt(n_acc),
         lower.ci.acc = round (mean_acc - qt(1 - (0.05 / 2), n_acc - 1) * se.acc,2),
         upper.ci.acc = round (mean_acc + qt(1 - (0.05 / 2), n_acc - 1) * se.acc,2)) %>%
  arrange(mean_acc)

kableExtra::kbl(Post.RT.percon,
             col.names = c("condition","N", "mean","SD",
                           "SE", "CI:lower", "CI:upper"),
             digits = 2, 
             booktabs = T,
             align = "c",
             caption = "Target: Reaction Time of the semantic stroop task: Post") %>%
  kable_styling(bootstrap_options = c("striped", "hover"),
                full_width = T) %>%
   row_spec(which(Post.RT.percon$Combination == "typical-unrelated") , background  = "lightblue") %>%
   row_spec(which(Post.RT.percon$Combination == "atypical-unrelated") , background  = "lightblue")
```

## 作図（文脈後）

```{r, echo=FALSE, warning=FALSE, fig.dim = c(10, 4)}
pacman::p_load(forcats)
fct_list <- c("典型的" = "typical",
              "非典型的" = "atypical",
              "ありえない" = "unrelated")

fct_list.two <- c("典型的" = "typical",
              "非典型的" = "atypical")

EN.model %>%
  mutate(Word.Typicality = fct_relevel(Word.Typicality,
                              levels = c("typical", "atypical", "unrelated"))) %>%
  mutate(Sentence.Typicality = fct_relevel(Sentence.Typicality,
                              levels = c("typical", "atypical"))) %>%
  mutate(Word.Typicality = fct_recode(Word.Typicality, !!!fct_list)) %>%
  mutate(Sentence.Typicality = fct_recode(Sentence.Typicality, !!!fct_list.two)) %>%
  filter(Position == "Post") %>%
  group_by(Sentence.Typicality, Word.Typicality) %>%
  summarise(mean = mean(RT.Stroop),
            sd = sd(RT.Stroop),
            n = n(),
            se = sd/sqrt(n),.groups = "drop") %>%
  ggplot(aes(x = Sentence.Typicality, y = mean, fill = Word.Typicality)) +
    geom_col(position = "dodge") +
    geom_errorbar(aes(ymin = mean - se, ymax = mean + se), 
                  position =position_dodge(0.9), width = .2) +
  scale_y_continuous(breaks = seq(0,700,10)) +
  coord_cartesian(ylim = c(500,700))  +
  scale_fill_viridis_d()  +
  labs(y="反応速度（ミリセカンド）") +
  labs(x="文章の典型性") +
  labs(fill = "単語の典型性") +
  labs(title = "条件ごとの反応速度") -> zz

ggplotly(zz)
```

## バイオリンプロット（文脈後）

```{r, echo=FALSE, warning=FALSE, fig.dim = c(10, 6)}
EN.model %>% 
  mutate(Combination = fct_relevel(Combination,
                                   levels = c("typical-typical", "typical-atypical", "typical-unrelated", 
                                              "atypical-atypical", "atypical-typical", "atypical-unrelated"))) %>%
  filter(Position == "Post") %>%
plot_ly(
  x = ~Combination,
  y = ~RT.Stroop,
  split = ~Combination,
  type = 'violin',
  box = list(
    visible = T
  ),
  meanline = list(
    visible = T
  ),
  showlegend = FALSE
) %>%
  layout(xaxis = list(
    title=list(text='文章-単語',
               font=list(size=15, family='Courier', color='black')),
    showgrid = F,
    rangemode = "tozero",
    nticks = 6,
    ticktext = list("典型-典型", "典型-非典型","典型-ありえない", "非典型-非典型", "非典型-典型","非典型-ありえない"),
    tickvals = list("typical-typical", "typical-atypical", "typical-unrelated", 
                    "atypical-atypical", "atypical-typical", "atypical-unrelated")
  )) %>%
  layout(yaxis = list(
    title=list(text='反応速度 (ミリ秒)',
               font=list(size=15, family='Courier', color='black')),
    range = c(200,900),
    showgrid = F,
    rangemode = "tozero",
    nticks = 6
  ))
```

## 研究課題1.1（文脈の位置による違い）

### 反応速度（英語：実験項目：文脈前）

-   クリーニング後

1.  典型的な文 - 典型的な単語の色
2.  非典型的な文 - 非典型的な単語の色
3.  非典型的な文 - 典型的な単語の色
4.  典型的な文 - 非典型的な単語の色
5.  典型的な文 - ありえない単語の色
6.  非典型的な文 - ありえない単語の色

```{r, tidy=TRUE,echo=FALSE, warning=FALSE}
pacman::p_load(forcats)

fct_list.two <- c("典型-典型" = "typical-typical",
                  "典型-非典型" = "typical-atypical", 
                  "典型-ありえない" = "typical-unrelated", 
                  "非典型-非典型" = "atypical-atypical",
                  "非典型-典型" = "atypical-typical", 
                  "非典型-ありえない" = "atypical-unrelated")

Pre.RT.percon <- EN.model %>% 
  mutate(Combination = fct_recode(Combination, !!!fct_list.two)) %>%
  filter(Position == "Pre") %>%
  group_by(Combination) %>%
  summarise(n_acc = n(),mean_acc=round(mean(RT.Stroop),2),sd_acc=sd(RT.Stroop),.groups = "drop") %>%
   mutate(se.acc = sd_acc/sqrt(n_acc),
         lower.ci.acc = round (mean_acc - qt(1 - (0.05 / 2), n_acc - 1) * se.acc,2),
         upper.ci.acc = round (mean_acc + qt(1 - (0.05 / 2), n_acc - 1) * se.acc,2)) %>%
  arrange(mean_acc)

kableExtra::kbl(Pre.RT.percon,
             col.names = c("condition","N", "mean","SD",
                           "SE", "CI:lower", "CI:upper"),
             digits = 2, 
             booktabs = T,
             align = "c",
             caption = "Target: Reaction Time of the semantic stroop task: Post") %>%
  kable_styling(bootstrap_options = c("striped", "hover"),
                full_width = T)  %>%
   row_spec(which(Pre.RT.percon$Combination == "typical-unrelated") , background  = "lightblue") %>%
   row_spec(which(Pre.RT.percon$Combination == "atypical-unrelated") , background  = "lightblue")
```

## 作図（文脈前）

```{r, echo=FALSE, warning=FALSE, message=FALSE,fig.dim = c(10, 4)}
pacman::p_load(forcats)
fct_list <- c("典型的" = "typical",
              "非典型的" = "atypical",
              "ありえない" = "unrelated")

fct_list.two <- c("典型的" = "typical",
              "非典型的" = "atypical")

EN.model %>%
  mutate(Word.Typicality = fct_relevel(Word.Typicality,
                              levels = c("typical", "atypical", "unrelated"))) %>%
   mutate(Sentence.Typicality = fct_relevel(Sentence.Typicality,
                              levels = c("typical", "atypical"))) %>%
  mutate(Word.Typicality = fct_recode(Word.Typicality, !!!fct_list)) %>%
  mutate(Sentence.Typicality = fct_recode(Sentence.Typicality, !!!fct_list.two)) %>%
  filter(Position == "Pre") %>%
  group_by(Sentence.Typicality, Word.Typicality) %>%
  summarise(mean = mean(RT.Stroop),
            sd = sd(RT.Stroop),
            n = n(),
            se = sd/sqrt(n),.groups = "drop") %>%
  ggplot(aes(x = Sentence.Typicality, y = mean, fill = Word.Typicality)) +
    geom_col(position = "dodge") +
    geom_errorbar(aes(ymin = mean - se, ymax = mean + se), 
                  position =position_dodge(0.9), width = .2) +
  scale_y_continuous(breaks = seq(0,700,10)) +
  coord_cartesian(ylim = c(500,700)) +
  scale_fill_viridis_d() +
  scale_fill_viridis_d()  +
  labs(y="反応速度（ミリセカンド）") +
  labs(x="文章の典型性") +
  labs(fill = "単語の典型性") +
  labs(title = "条件ごとの反応速度")-> zzz

ggplotly(zzz)
```

## バイオリンプロット（文脈前）

```{r, echo=FALSE, warning=FALSE, fig.dim = c(10, 6)}
EN.model %>% 
  mutate(Combination = fct_relevel(Combination,
                                   levels = c("typical-typical", "typical-atypical", "typical-unrelated", 
                                              "atypical-atypical", "atypical-typical", "atypical-unrelated"))) %>%
  filter(Position == "Pre") %>%
  plot_ly(
    x = ~Combination,
    y = ~RT.Stroop,
    split = ~Combination,
    type = 'violin',
    box = list(
      visible = T
    ),
    meanline = list(
      visible = T
    ),
    showlegend = FALSE
  ) %>%
  layout(xaxis = list(
    title=list(text='文章-単語',
               font=list(size=15, family='Courier', color='black')),
    showgrid = F,
    rangemode = "tozero",
    nticks = 6,
    ticktext = list("典型-典型", "典型-非典型","典型-ありえない", "非典型-非典型", "非典型-典型","非典型-ありえない"),
    tickvals = list("typical-typical", "typical-atypical", "typical-unrelated", 
                    "atypical-atypical", "atypical-typical", "atypical-unrelated")
  )) %>%
  layout(yaxis = list(
    title=list(text='反応速度 (ミリ秒)',
               font=list(size=15, family='Courier', color='black')),
    range = c(200,900),
    showgrid = F,
    rangemode = "tozero",
    nticks = 6
  ))
```

## 今後の計画

-   データ収集の80%を**5月**までに完了
-   日本人を対象にした実験の前に項目の修正
  -   Localな文法ミス
  -   文脈前の刺激文
    -   It didn't **looked** ready to eat when Mark bought the strawberry.
    -   Sarah stopped in front of a tree and **pick** a leaf off. 
    -   Sarah sat on the ground and **pick** a leaf up. 
  -   フィラー項目
    -   The **door** was being opened all day.
      -   この項目は分析から除外予定

1.  英語母語話者を対象に実験

    -   残り**24**名

2.  日本人を対象に日本語で実験

    -   残り**44**名

3.  日本人を対象に英語で実験

    -   残り**44**名

-   メインの分析（一般化線形混合効果モデル）

    -   ランダム構造の設計

## 新井学, & Roland, D. (2016). 言語理解研究における眼球運動データ及び読み時間データの統計分析. 統計数理, *64*(2), 201-231.
-   粟津俊二, & 鈴木明夫. (2020).
    第二言語低熟達者による第二言語文理解の身体性. 認知科学, *27*(4),
    554--566.引用文献
-   

-   Barsalou, L. W. (1999). Perceptual symbol systems. *Behavioral and
    Brain Sciences, 22*(4), 577--660.

-   Barsalou, L. W. (2008). Grounded cognition. *Annual Review of
    Psychology, 59*, 617-645.

-   Buccino, G., Marino, B. F., Bulgarelli, C., & Mezzadri, M. (2017).
    Fluent speakers of a second language process graspable nouns
    expressed in L2 like in their native language. *Frontiers in
    psychology, 8*, 1306.

-   Connell, L., & Lynott, D. (2009). Is a bear white in the woods?
    Parallel representation of implied object color during language
    comprehension. *Psychonomic Bulletin & Review, 16*(3), 573--577.

-   Horchak, O. V., & Garrido, M. V. (2020). Dropping bowling balls on
    cakees: Representations of object state-changes during sentence
    processing. *Journal of Experimental Psychology: Learning, Memory,*
    *and Cognition 47*(5), 838--857.

-   Norman, T., & Peleg, O. (2021). The reduced embodiment of a second
    language. *Bilingualism: Language and Cognition*, 1--11.

-   Sato, M., Schafer, A., J., & Bergen, B., K. (2013). One word at a
    time: Mental representations of object shape change incrementally
    during sentence processing. *Language and Cognition, 5*(4), 345-373.

-   Zwaan, R. A., & Pecher, D. (2012). Revisiting mental simulation in
    language comprehension: Six replication attempts. *PloS one, 7*(12),
    e51382.

-   Zwaan, R. A., Stanfield, R. A., & Yaxley, R. H. (2002). Language
    comprehenders mentally represent the shapes of objects.
    *Psychological Science, 13*(2), 168--171.
