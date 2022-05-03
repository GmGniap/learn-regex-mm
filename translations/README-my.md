<p align="center">
    <br/>
    <a href="https://github.com/ziishaned/learn-regex">	
        <img src="https://i.imgur.com/bYwl7Vf.png" alt="Learn Regex">
    </a>
</p>

## Translations:

* [English](README.md)
* [German](translations/README-de.md)
* [Español](translations/README-es.md)
* [Français](translations/README-fr.md)
* [Português do Brasil](translations/README-pt_BR.md)
* [中文版](translations/README-cn.md)
* [日本語](translations/README-ja.md)
* [한국어](translations/README-ko.md)
* [Turkish](translations/README-tr.md)
* [Greek](translations/README-gr.md)
* [Magyar](translations/README-hu.md)
* [Polish](translations/README-pl.md)
* [Русский](translations/README-ru.md)
* [Tiếng Việt](translations/README-vn.md)
* [فارسی](translations/README-fa.md)
* [עברית](translations/README-he.md)
* [မြန်မာ](translations/README-my.md)


## Regular Expression ဆိုတာ ?

<p>
    <a href="https://gum.co/learn-regex">
        <img src="https://img.shields.io/badge/-Download%20PDF%20-0a0a0a.svg?style=flat&colorA=0a0a0a" alt="Download PDF">
    </a>
</p>

> Regular expression ဆိုတာကတော့ စာသားထဲမှာ ရှိတဲ့ တိကျသော ပုံစံ patten ကို ရှာဖွေရာတွင် အသုံးပြုသော စကားလုံးများ (သို့) သင်္ကေတများ စသည့် အစုအဖွဲ့ကို ဆိုလိုပါတယ်။

Regular expression ဆိုသည်မှာ ရှာဖွေလိုသော စာကြောင်းတစ်ကြောင်းထဲတွင် ဘယ်ဘက်မှ ညာဘက်သို့ ကိုက်ညီမှု ရှိအောင် ရှာဖွေသွားသော pattern တစ်ခု ဖြစ်ပါတယ်။ Regular expression တွေကို စာကြောင်းထဲက စကားစုများကို အစားထိုးရန် ၊ စာရင်းအင်းဖောင် များကို စီစစ်ရန် ၊ ကိုက်ညီသော pattern အပေါ် အခြေတည်၍ စာကြောင်းထဲမှ စကားရပ်ကို ထုတ်နှုတ်ရန် - ရည်ရွယ်ချက်များစွာဖြင့် အသုံးပြုကြပါတယ်။ "Regular expression" ဆိုတဲ့ ရှည်လျားလှတဲ့ အသုံးအနှုန်း အစား အတိုကောက်အနေနဲ့ "regex" (သို့) "regexp" လို့လဲ ခေါ်ဝေါ်သုံးစွဲကြပါတယ်။

သင့်အနေဖြင့် Application တစ်ခုကို ရေးနေပြီး အဆိုပါ App အသုံးပြုသူများအတွက် username ကို ရွေးချယ်ရာမှာ စံသတ်မှတ်ချက် rules များကို သင့်အနေဖြင့် သတ်မှတ်လိုသည် ဟု မြင်ယောင်ကြည့်ပါ။ အဆိုပါ username တွင် letters,numbers,underscores နှင့် hyphens များ ပါဝင်ခွင့် ပြုမည်။ သို့သော် username ကို ဖတ်ရဆိုးစေသည့် စကားလုံးအရေအတွက် ရှည်လျားစွာမပါဝင်စေရန် စာလုံးရေ ကို ကန့်သတ်ချင်သည်။ ကျွန်တော်တို့အနေဖြင့် အောက်ပါ Regular Expression ကို username အား စီစစ်ရန် အသုံးပြုနိုင်သည်။

<br/><br/>
<p align="center">
  <img src="../img/regexp-en.png" alt="Regular expression">
</p>

အထက်ပါ regular expression သည် `john_doe`, `jo-hn_doe` နှင့် `john12_as` စသည့် စာသားများကို လက်ခံသည်။ သို့သော် `Jo` ဆိုသည်နှင့် ကိုက်ညီမည် မဟုတ်။ ဘာကြောင့်လဲဆိုသော် အဆိုပါ စာသားတွင် uppercase စာလုံးပါဝင်သည့်အဖြင့် စာလုံးအရေအတွက်မှာလဲ ၃ လုံးမပြည့်သောကြောင့် ဖြစ်သည်။

## Table of Contents

- [Basic Matchers](#1-basic-matchers)
- [Meta Characters](#2-meta-characters)
  - [The Full Stop](#21-the-full-stop)
  - [Character Sets](#22-character-sets)
    - [Negated Character Sets](#221-negated-character-sets)
  - [Repetitions](#23-repetitions)
    - [The Star](#231-the-star)
    - [The Plus](#232-the-plus)
    - [The Question Mark](#233-the-question-mark)
  - [Braces](#24-braces)
  - [Capturing Groups](#25-capturing-groups)
      - [Non-Capturing Groups](#251-non-capturing-groups)
  - [Alternation](#26-alternation)
  - [Escaping Special Characters](#27-escaping-special-characters)
  - [Anchors](#28-anchors)
    - [The Caret](#281-the-caret)
    - [The Dollar Sign](#282-the-dollar-sign)
- [Shorthand Character Sets](#3-shorthand-character-sets)
- [Lookarounds](#4-lookarounds)
  - [Positive Lookahead](#41-positive-lookahead)
  - [Negative Lookahead](#42-negative-lookahead)
  - [Positive Lookbehind](#43-positive-lookbehind)
  - [Negative Lookbehind](#44-negative-lookbehind)
- [Flags](#5-flags)
  - [Case Insensitive](#51-case-insensitive)
  - [Global Search](#52-global-search)
  - [Multiline](#53-multiline)
- [Greedy vs Lazy Matching](#6-greedy-vs-lazy-matching)

## 1. Basic Matchers

Regular expression သည် စကားလုံး pattern တစ်ခုသာ ဖြစ်ပြီး ကျွန်တော်တို့အနေနဲ့ စာသားတစ်ကြောင်းထဲတွင် ကိုက်ညီမှုကို ရှာရန် အသုံးပြုသည်။ ဥပမာ - regular expression တစ်ခုဖြစ်သည် `the` သည် စာလုံးအနေဖြင့် - `t` ,ဆက်လျက် `h`,ဆက်လျက် `e` ဆိုသည့် အဓိပ္ပါယ်ဖြစ်သည်။

<pre>
"the" => The fat cat sat on <a href="#learn-regex"><strong>the</strong></a> mat.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/dmRygT/1)

regular expression `123` သည် စကားစု `123` နှင့် ကိုက်ညီသည်။ regular expression သည် input စကားစုကို regular expression အတွင်းရှိ စကားလုံးတစ်လုံးချင်းဆီနှင့် တစ်လုံးချင်းတစ်လုံး တိုက်ဆိုင်စစ်ဆေးသည်။ Regular expression များသည် ယေဘုယျအားဖြင့် case-sensitive အမှားအယွင်းမရှိရပါ။ ဥပမာ- regular expression `The` သည် စကားစု `the` နှင့် ကိုက်ညီလိမ့်မည် မဟုတ်ပါ။

<pre>
"The" => <a href="#learn-regex"><strong>The</strong></a> fat cat sat on the mat.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/1paXsy/1)

## 2. Meta Characters

Meta စာလုံးများ ဆိုသည်မှာ regular expression ကို တည်ဆောက်သည့်အရာများ ဖြစ်သည်။ Meta စာလုံးများအနေဖြင့် ၎င်းတို့ဘာသာ ရပ်တည်နိုင်ခြင်းမရှိသောလည်း အရေးပါသည့်နည်းလမ်းများအနေဖြင့် အသုံးဝင်သည်။ အချို့သော meta character များသည် ထူးခြားသည့် အဓိပ္ပါယ် ရှိပြီး ၎င်းတို့ကို square brackets [] ထဲတွင် ရေးသည်။ Meta စာလုံးများမှာ အောက်ပါအတိုင်း ဖြစ်သည်။ 

|Meta စာလုံးများ|အဓိပ္ပါယ်ဖွင့်ဆိုချက်|
|:----:|----|
|.|line break လိုင်းခြားခြင်း မှလွဲ၍ အခြား မည်သည့် စာလုံးတစ်လုံးတည်းနှင့်မဆို ကိုက်ညီသည်။.|
|[ ]|Character class. Square brackets အတွင်းရှိ ပါဝင်သည့် မည်သည့်စာလုံးနှင့်မဆို ကိုက်ညီသည်။|
|[^ ]|ဆန့်ကျင်ဘက် character class. Square brackets အတွင်းတွင် မပါဝင်သည့် မည်သည့်စာလုံးနှင့်မဆို ကိုက်ညီသည်။|
|*|ပါဝင်မှုလုံးဝ မရှိခြင်း - သုည (သို့) အကြိမ်ရေများစွာ ပါဝင်သော စာလုံးနှင့် ကိုက်ညီသည်။|
|+|တစ်ကြိမ် (သို့) တစ်ကြိမ်အထက် အကြိမ်ရေများစွာ ပါဝင်သော စာလုံးနှင့် ကိုက်ညီသည်။|
|?|တွဲလျက်စာလုံးကို Optional(အခြေအနေအလိုက်) အဖြစ် ပြောင်းလဲပေးသည်။|
|{n,m}|Braces. အနည်းဆုံး "n" အကြိမ်ရေ မှ အများဆုံး "m" အကြိမ်ရေအတွင်း ပါဝင်သော စာလုံးနှင့် ကိုက်ညီသည်။|
|(xyz)|Character group. xyz စာလုံးအစီအစဥ်အတိုင်း ကိုက်ညီသည်။|
|&#124;|Alternation. သင်္ကေတ၏ အရှေ့ (သို့) အနောက်ရှိ စာလုံး တစ်ခုခုနှင့် ကိုက်ညီစေသည်။|
|&#92;| Escape. တွဲလျက်စကားလုံး ကို ချွင်းချက် ဖြစ်စေသည်။ အထူးစာလုံးများနှင့်အတူ တွဲလျက်သုံးသည်။ <code>[ ] ( ) { } . * + ? ^ $ \ &#124;</code>|
|^|စာကြောင်းအစ နှင့် ကိုက်ညီသည်။|
|$|စာကြောင်းအဆုံး နှင့် ကိုက်ညီသည်။|

## 2.1 The Full Stop

Full stop `.` သည် meta စာလုံး၏ အရိုးရှင်းဆုံး ဥပမာဖြစ်သည်။ meta စာလုံးဖြစ်သော `.` သည် မည်သည့် စာလုံးတစ်လုံးနှင့်မဆို ကိုက်ညီသည်။ ၎င်းသည် return (သို့) newline တစ်ကြောင်းဆင်းသည့် character များနှင့်တော့ ကိုက်ညီမည် မဟုတ်။ ဥပမာ အားဖြင့် regular expression `.ar` ဆိုသည်မှာ မည်သည့် စာလုံး မဆို - နောက်တွင် `a`,ဆက်လျက် `r` ရှိသည်ဟု ဆိုလိုသည်။

<pre>
".ar" => The <a href="#learn-regex"><strong>car</strong></a> <a href="#learn-regex"><strong>par</strong></a>ked in the <a href="#learn-regex"><strong>gar</strong></a>age.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/xc9GkU/1)

## 2.2 Character Sets

Character sets များကို character classes များဟုလဲ ခေါ်သည်။ character sets များကို ဖော်ပြရန်အတွက် Square brackets [] များကို အသုံးပြုသည်။ character set အတွင်းတွင် hyphen အသုံးပြုခြင်းအားဖြင့် characters အပိုင်းအခြား ကို ဖော်ပြသည်။ (ဥပမာ - [A-Z] ဆိုသည်မှာ A မှ Z အထိ character များအားလုံး ပါဝင်သည့် အဓိပ္ပါယ် ဖြစ်သည်။) regular expression `[Tt]he` ဆိုသည်မှာ uppercase `T` (သို့) lowercase `t` ကြိုက်ရာဖြစ်နိုင်ပြီး နောက်ဆက်တွဲ စာလုံး `h`,ဆက်လျက် `e` ပါဝင်သည်ဟု ဆိုလိုသည်။

<pre>
"[Tt]he" => <a href="#learn-regex"><strong>The</strong></a> car parked in <a href="#learn-regex"><strong>the</strong></a> garage.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/2ITLQ4/1)

character set အတွင်းရှိ period တစ်ခုကို literal period ဟု ခေါ်သည်။ regular expression `ar[.]` သည် lowercase `a`,နောက်တွင် `r`,ဆက်လျက် period `.` စာလုံး ရှိသည်ဟု ဆိုလိုသည်။ 

<pre>
"ar[.]" => A garage is a good place to park a c<a href="#learn-regex"><strong>ar.</strong></a>
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/wL3xtE/1)

### 2.2.1 Negated Character Sets

ယေဘုယျအားဖြင့် caret သင်္ကေတ `^` သည် စာကြောင်းအစ ကို ရည်ညွှန်းသော်လည်း ၎င်းကို square bracket [] အတွင်းတွင် ရေးသော်အခါ ၎င်းသည် character set ၏ ဆန့်ကျင်ဘက် ကို ဆိုလိုကြောင်း ဖြစ်သွားသည်။ ဥပမာ - regular expression `[^c]ar` သည် `c` စာလုံးမှ လွဲ၍ အခြားမည်သည့်စာလုံး တစ်လုံးလုံး၏ နောက်တွင် `a`,ဆက်လျက် `r` ရှိသည်ဟု ဆိုလိုသည်။

<pre>
"[^c]ar" => The car <a href="#learn-regex"><strong>par</strong></a>ked in the <a href="#learn-regex"><strong>gar</strong></a>age.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/nNNlq3/1)

## 2.3 Repetitions

meta စာလုံးများဖြစ်သည့် `+`, `*` (သို့) `?` များကို subpattern တစ်ခု အကြိမ်မည်မျှ ဖြစ်နိုင်သည်ကို ဖော်ပြရာတွင် အသုံးပြုသည်။ ၎င်း meta စာလုံးများသည် ခြားနားသော အခြေအနေအမျိုးမျိုးတွင် ကွဲပြားစွာ လုပ်ဆောင်သည်။

### 2.3.1 The Star

ကြယ်ပွင့်သင်္ကေတ `*` သည် သုည (သို့) သုညထက်ပိုသည့် အကြိမ်အရေအတွက်ကို ကိုက်ညီစေသည်။ regular expression `a*` ဆိုသည်မှာ lowercase `a` လုံးဝ မပါသည်ဖြစ်စေ(သို့) အကြိမ်ကြိမ် ပါသည်ဖြစ်စေ ကိုက်ညီစေမည်။ အကယ်၍ ၎င်းသည် character set (သို့) class အနောက်တွင် တွဲလျက်ပါခဲ့သော အဆိုပါ character set တစ်ခုလုံး၏ အကြိမ်ကြိမ်ပါဝင်မှုကို ရှာဖွေမည်။ ဥပမာ - regular expression `[a-z]*` ဆိုသည်မှာ စာတစ်ကြောင်းတွင် ပါဝင်သည် lowercase အသေးစာလုံးများအားလုံးကို ဆိုလိုသည်။ 

<pre>
"[a-z]*" => T<a href="#learn-regex"><strong>he</strong></a> <a href="#learn-regex"><strong>car</strong></a> <a href="#learn-regex"><strong>parked</strong></a> <a href="#learn-regex"><strong>in</strong></a> <a href="#learn-regex"><strong>the</strong></a> <a href="#learn-regex"><strong>garage</strong></a> #21.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/7m8me5/1)

ကြယ်ပွင့်သင်္ကေတ `*` ကို meta စာလုံးဖြစ်သည့် `.` နှင့် တွဲဖက်အသုံးပြုပြီး မည်သည့်စကားစုကိုမဆို ကိုက်ညီစေရန် `.*` ဟု သုံးနိုင်သည်။ ကြယ်ပွင့်သင်္ကေတ `*` ကို whitespace စာလုံး `\s` နှင့် တွဲသုံးပြီး ကွက်လပ်နေရာလွတ်များကို ရှာဖွေရန် သုံးသည်။ ဥပမာ - `\s*cat\s*` expression သည် သုည(သို့)ထက်ပိုသော ကွက်လပ်များပါဝင်ပြီး နောက်တွင် `c`,ဆက်လျက် `a`,ဆက်လျက် `t`,နောက်တွင် သုည(သို့) ထပ်ပိုသော ကွက်လပ်များ ပါသည်ဟု ဆိုလိုသည်။

<pre>
"\s*cat\s*" => The fat<a href="#learn-regex"><strong> cat </strong></a>sat on the con<a href="#learn-regex"><strong>cat</strong></a>enation.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/gGrwuz/1)

### 2.3.2 The Plus

အပေါင်းသင်္ကေတ `+` သည် တစ်ခု (သို့) ထက်ပိုသော စာလုံးအရေအတွက်နှင့် ကိုက်ညီသည်။ ဥပမာ - regular expression `c.+t` သည် `c` စာလုံးသေး,နောက်တွင် အနည်းဆုံး စာလုံးတစ်လုံး (သို့) တစ်လုံးထက်ပိုသော စာလုံးများ, ထို့နောက်တွင် `t`စာလုံးသေး ပါဝင်သည်ဟု ဆိုလိုသည်။ ၎င်းအနေဖြင့် `t` သည် စာကြောင်း နောက်ဆုံး `t` ဖြစ်ကြောင်း ဖော်ပြရန် လိုအပ်သည်။

<pre>
"c.+t" => The fat <a href="#learn-regex"><strong>cat sat on the mat</strong></a>.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/Dzf9Aa/1)

### 2.3.3 The Question Mark

regular expressions တွင် မေးခွန်းသင်္ကေတ`?` သည် တွဲလျက်စာလုံးကို optional ဖြစ်စေရန် ပြုလုပ်ပေးသည်။ အဆိုပါသင်္ကေတသည် သုည (သို့) တစ်ခုထက်ပိုသော တွဲလျက်စာလုံးနှင့် ကိုက်ညီစေသည်။ ဥပမာအားဖြင့် regular expression `[T]?he` သည် Optional စာလုံးကြီး `T` နောက်တွင် စာလုံးသေး `h`,ဆက်လျက် စာလုံးသေး `e`ရှိသည်ဟု ဆိုလိုသည်။

<pre>
"[T]he" => <a href="#learn-regex"><strong>The</strong></a> car is parked in the garage.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/cIg9zm/1)

<pre>
"[T]?he" => <a href="#learn-regex"><strong>The</strong></a> car is parked in t<a href="#learn-regex"><strong>he</strong></a> garage.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/kPpO2x/1)

## 2.4 Braces

regular expressions တွင် တွန့်ကွင်း {} braces(quantifiers ဟုလဲ ခေါ်။) ကို စာလုံး (သို့) စကားစုများ၏ ထပ်ခါတလဲလဲ ဖြစ်နိုင်သော အကြိမ်အရေအတွက်ကို ဖော်ပြရာတွင် အသုံးပြုသည်။ ဥပမာအားဖြင့် regular expression `[0-9]{2,3}` ဆိုသည်မှာ အနည်းဆုံး ဂဏန်း ၂ လုံးမှ အများဆုံး ၃ လုံးအတွင်းရှိသည့် 0-9 ကိန်းဂဏန်းများနှင့် ကိုက်ညီသည်။

<pre>
"[0-9]{2,3}" => The number was 9.<a href="#learn-regex"><strong>999</strong></a>7 but we rounded it off to <a href="#learn-regex"><strong>10</strong></a>.0.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/juM86s/1)

ကျွန်တော်တို့ အနေဖြင့် ဒုတိယဂဏန်းကို ချန်လှပ်ထားခဲ့နိုင်သည်။ ဥပမာ - regular expression
`[0-9]{2,}` ဆိုသည်မှာ ဂဏန်းနှစ်လုံး (သို့) နှစ်လုံးထက်များသော အရေအတွက်နှင့် ကိုက်ညီသည်။ အကယ်၍ ကျွန်တော်တို့အနေဖြင့် comma `,` ကို ဖယ်ရှားခဲ့ပါက regular expression `[0-9]{3}` ဆိုသည်မှာ အတိအကျ ဂဏန်း ၃ လုံးနှင့် ကိုက်ညီသည်ဟု ဆိုလိုသည်။

<pre>
"[0-9]{2,}" => The number was 9.<a href="#learn-regex"><strong>9997</strong></a> but we rounded it off to <a href="#learn-regex"><strong>10</strong></a>.0.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/Gdy4w5/1)

<pre>
"[0-9]{3}" => The number was 9.<a href="#learn-regex"><strong>999</strong></a>7 but we rounded it off to 10.0.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/Sivu30/1)

## 2.5 Capturing Groups

Capturing Group ဆိုသည်မှာ `(...)` parentheses အတွင်း ရေးထားသော subpatterns အစုအဖွဲ့ကို ဆိုလိုသည်။ ယခင်ကဆွေးနွေးခဲ့သည့်အတိုင်း regular expression များတွင် ကျွန်တော်တို့အနေဖြင့် စာလုံးတစ်လုံးနောက်တွင် quantifier တစ်ခုထည့်ပါက ၎င်းသည် စာလုံးကို ထပ်ခါထပ်ခါ ဖော်ပြမည်။ သို့သော် capturing group တစ်ခုနောက်တွင် quantifier တစ်ခု ထည့်သောအခါ ၎င်းသည် capturing group တစ်ခုလုံးကို ထပ်ခါတလဲလဲ ဖော်ပြမည် ဖြစ်သည်။ ဥပမာ- regular expression `(ab)*` ဆိုသည်မှာ "ab" စကားစုကို သုည (သို့) သုညထက်ပိုသော အကြိမ်အရေအတွက်ဖြင့် ဖော်ပြမည်ဖြစ်သည်။ `|` meta စာလုံးကိုလဲ capturing group အတွင်းတွင် ထည့်သွင်း အသုံးပြုနိုင်သည်။ ဥပမာ - regular expression `(c|g|p)ar` ဆိုသည်မှာ စာလုံးသေး `c` (သို့) `g` (သို့) `p` နောက်တွင် `a`,ဆက်လျက် `r` ရှိမည် ဖြစ်သည်။

<pre>
"(c|g|p)ar" => The <a href="#learn-regex"><strong>car</strong></a> is <a href="#learn-regex"><strong>par</strong></a>ked in the <a href="#learn-regex"><strong>gar</strong></a>age.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/tUxrBG/1)

capturing groups များသည် တူညီမှုကို ရှာနိုင်ရုံသာမက မိခင်ပရိုဂရမ်ဘာသာတွင် ပြန်လည်အသုံးပြုရန် စာလုံးများကိုလဲ မှတ်သားနိုင်သည်။မိခင်ပရိုဂရမ်ဘာသာ ဆိုသည်မှာ Python (သို့) JavaScript (သို့) regular expressions ကို အသုံးပြုနိုင်သည့် အခြား မည်သည့် language ကိုမဆို ဆိုလိုသည်။

### 2.5.1 Non-Capturing Groups

A non-capturing group is a capturing group that matches the characters but 
does not capture the group. A non-capturing group is denoted by a `?` followed by a `:` 
within parentheses `(...)`. For example, the regular expression `(?:c|g|p)ar` is similar to 
`(c|g|p)ar` in that it matches the same characters but will not create a capture group.

<pre>
"(?:c|g|p)ar" => The <a href="#learn-regex"><strong>car</strong></a> is <a href="#learn-regex"><strong>par</strong></a>ked in the <a href="#learn-regex"><strong>gar</strong></a>age.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/Rm7Me8/1)

Non-capturing groups can come in handy when used in find-and-replace functionality or 
when mixed with capturing groups to keep the overview when producing any other kind of output. 
See also [4. Lookaround](#4-lookaround).

## 2.6 Alternation

In a regular expression, the vertical bar `|` is used to define alternation.
Alternation is like an OR statement between multiple expressions. Now, you may be
thinking that character sets and alternation work the same way. But the big
difference between character sets and alternation is that character sets work at the
character level but alternation works at the expression level. For example, the
regular expression `(T|t)he|car` means: either (an uppercase `T` or a lowercase
`t`, followed by a lowercase `h`, followed by a lowercase `e`) OR
(a lowercase `c`, followed by a lowercase `a`, followed by
a lowercase `r`). Note that I included the parentheses for clarity, to show that either expression
in parentheses can be met and it will match.

<pre>
"(T|t)he|car" => <a href="#learn-regex"><strong>The</strong></a> <a href="#learn-regex"><strong>car</strong></a> is parked in <a href="#learn-regex"><strong>the</strong></a> garage.
</pre>

[regular expression ကို စမ်းသပ်ရန်](https://regex101.com/r/fBXyX0/1)

## 2.7 Escaping Special Characters

A backslash `\` is used in regular expressions to escape the next character. This
allows us to include reserved characters such as `{ } [ ] / \ + * . $ ^ | ?` as matching characters. To use one of these special character as a matching character, prepend it with `\`.

For example, the regular expression `.` is used to match any character except a
newline. Now, to match `.` in an input string, the regular expression
`(f|c|m)at\.?` means: a lowercase `f`, `c` or `m`, followed by a lowercase
`a`, followed by a lowercase `t`, followed by an optional `.`
character.

<pre>
"(f|c|m)at\.?" => The <a href="#learn-regex"><strong>fat</strong></a> <a href="#learn-regex"><strong>cat</strong></a> sat on the <a href="#learn-regex"><strong>mat.</strong></a>
</pre>

[Test the regular expression](https://regex101.com/r/DOc5Nu/1)

## 2.8 Anchors

In regular expressions, we use anchors to check if the matching symbol is the
starting symbol or ending symbol of the input string. Anchors are of two types:
The first type is the caret `^` that checks if the matching character is the first
character of the input and the second type is the dollar sign `$` which checks if a matching
character is the last character of the input string.

### 2.8.1 The Caret

The caret symbol `^` is used to check if a matching character is the first character
of the input string. If we apply the following regular expression `^a` (meaning 'a' must be
the starting character) to the string `abc`, it will match `a`. But if we apply
the regular expression `^b` to the above string, it will not match anything.
Because in the string `abc`, the "b" is not the starting character. Let's take a look
at another regular expression `^(T|t)he` which means: an uppercase `T` or
a lowercase `t` must be the first character in the string, followed by a
lowercase `h`, followed by a lowercase `e`.

<pre>
"(T|t)he" => <a href="#learn-regex"><strong>The</strong></a> car is parked in <a href="#learn-regex"><strong>the</strong></a> garage.
</pre>

[Test the regular expression](https://regex101.com/r/5ljjgB/1)

<pre>
"^(T|t)he" => <a href="#learn-regex"><strong>The</strong></a> car is parked in the garage.
</pre>

[Test the regular expression](https://regex101.com/r/jXrKne/1)

### 2.8.2 The Dollar Sign

The dollar sign `$` is used to check if a matching character is the last character
in the string. For example, the regular expression `(at\.)$` means: a
lowercase `a`, followed by a lowercase `t`, followed by a `.`
character and the matcher must be at the end of the string.

<pre>
"(at\.)" => The fat c<a href="#learn-regex"><strong>at.</strong></a> s<a href="#learn-regex"><strong>at.</strong></a> on the m<a href="#learn-regex"><strong>at.</strong></a>
</pre>

[Test the regular expression](https://regex101.com/r/y4Au4D/1)

<pre>
"(at\.)$" => The fat cat. sat. on the m<a href="#learn-regex"><strong>at.</strong></a>
</pre>

[Test the regular expression](https://regex101.com/r/t0AkOd/1)

##  3. Shorthand Character Sets

There are a number of convenient shorthands for commonly used character sets/
regular expressions:

|Shorthand|Description|
|:----:|----|
|.|Any character except new line|
|\w|Matches alphanumeric characters: `[a-zA-Z0-9_]`|
|\W|Matches non-alphanumeric characters: `[^\w]`|
|\d|Matches digits: `[0-9]`|
|\D|Matches non-digits: `[^\d]`|
|\s|Matches whitespace characters: `[\t\n\f\r\p{Z}]`|
|\S|Matches non-whitespace characters: `[^\s]`|

## 4. Lookarounds

Lookbehinds and lookaheads (also called lookarounds) are specific types of
***non-capturing groups*** (used to match a pattern but without including it in the matching
list). Lookarounds are used when a pattern must be
preceded or followed by another pattern. For example, imagine we want to get all
numbers that are preceded by the `$` character from the string
`$4.44 and $10.88`. We will use the following regular expression `(?<=\$)[0-9\.]*`
which means: get all the numbers which contain the `.` character and are preceded
by the `$` character. These are the lookarounds that are used in regular
expressions:

|Symbol|Description|
|:----:|----|
|?=|Positive Lookahead|
|?!|Negative Lookahead|
|?<=|Positive Lookbehind|
|?<!|Negative Lookbehind|

### 4.1 Positive Lookahead

The positive lookahead asserts that the first part of the expression must be
followed by the lookahead expression. The returned match only contains the text
that is matched by the first part of the expression. To define a positive
lookahead, parentheses are used. Within those parentheses, a question mark with
an equals sign is used like this: `(?=...)`. The lookahead expressions is written after
the equals sign inside parentheses. For example, the regular expression
`(T|t)he(?=\sfat)` means: match either a lowercase `t` or an uppercase
 `T`, followed by the letter `h`, followed by the letter `e`. In parentheses we
define a positive lookahead which tells the regular expression engine to match `The`
or `the` only if it's followed by the word `fat`.

<pre>
"(T|t)he(?=\sfat)" => <a href="#learn-regex"><strong>The</strong></a> fat cat sat on the mat.
</pre>

[Test the regular expression](https://regex101.com/r/IDDARt/1)

### 4.2 Negative Lookahead

Negative lookaheads are used when we need to get all matches from an input string
that are not followed by a certain pattern. A negative lookahead is written the same way as a
positive lookahead. The only difference is, instead of an equals sign `=`, we
use an exclamation mark `!` to indicate negation i.e. `(?!...)`. Let's take a look at the following
regular expression `(T|t)he(?!\sfat)` which means: get all `The` or `the` words
from the input string that are not followed by a space character and the word `fat`.

<pre>
"(T|t)he(?!\sfat)" => The fat cat sat on <a href="#learn-regex"><strong>the</strong></a> mat.
</pre>

[Test the regular expression](https://regex101.com/r/V32Npg/1)

### 4.3 Positive Lookbehind

Positive lookbehinds are used to get all the matches that are preceded by a
specific pattern. Positive lookbehinds are written `(?<=...)`. For example, the
regular expression `(?<=(T|t)he\s)(fat|mat)` means: get all `fat` or `mat` words
from the input string that come after the word `The` or `the`.

<pre>
"(?<=(T|t)he\s)(fat|mat)" => The <a href="#learn-regex"><strong>fat</strong></a> cat sat on the <a href="#learn-regex"><strong>mat</strong></a>.
</pre>

[Test the regular expression](https://regex101.com/r/avH165/1)

### 4.4 Negative Lookbehind

Negative lookbehinds are used to get all the matches that are not preceded by a
specific pattern. Negative lookbehinds are written `(?<!...)`. For example, the
regular expression `(?<!(T|t)he\s)(cat)` means: get all `cat` words from the input
string that are not after the word `The` or `the`.

<pre>
"(?&lt;!(T|t)he\s)(cat)" => The cat sat on <a href="#learn-regex"><strong>cat</strong></a>.
</pre>

[Test the regular expression](https://regex101.com/r/8Efx5G/1)

## 5. Flags

Flags are also called modifiers because they modify the output of a regular
expression. These flags can be used in any order or combination, and are an
integral part of the RegExp.

|Flag|Description|
|:----:|----|
|i|Case insensitive: Match will be case-insensitive.|
|g|Global Search: Match all instances, not just the first.|
|m|Multiline: Anchor meta characters work on each line.|

### 5.1 Case Insensitive

The `i` modifier is used to perform case-insensitive matching. For example, the
regular expression `/The/gi` means: an uppercase `T`, followed by a lowercase
`h`, followed by an `e`. And at the end of regular expression
the `i` flag tells the regular expression engine to ignore the case. As you can
see, we also provided `g` flag because we want to search for the pattern in the
whole input string.

<pre>
"The" => <a href="#learn-regex"><strong>The</strong></a> fat cat sat on the mat.
</pre>

[Test the regular expression](https://regex101.com/r/dpQyf9/1)

<pre>
"/The/gi" => <a href="#learn-regex"><strong>The</strong></a> fat cat sat on <a href="#learn-regex"><strong>the</strong></a> mat.
</pre>

[Test the regular expression](https://regex101.com/r/ahfiuh/1)

### 5.2 Global Search

The `g` modifier is used to perform a global match (finds all matches rather than
stopping after the first match). For example, the regular expression`/.(at)/g`
means: any character except a new line, followed by a lowercase `a`,
followed by a lowercase `t`. Because we provided the `g` flag at the end of
the regular expression, it will now find all matches in the input string, not just the first one (which is the default behavior).

<pre>
"/.(at)/" => The <a href="#learn-regex"><strong>fat</strong></a> cat sat on the mat.
</pre>

[Test the regular expression](https://regex101.com/r/jnk6gM/1)

<pre>
"/.(at)/g" => The <a href="#learn-regex"><strong>fat</strong></a> <a href="#learn-regex"><strong>cat</strong></a> <a href="#learn-regex"><strong>sat</strong></a> on the <a href="#learn-regex"><strong>mat</strong></a>.
</pre>

[Test the regular expression](https://regex101.com/r/dO1nef/1)

### 5.3 Multiline

The `m` modifier is used to perform a multi-line match. As we discussed earlier,
anchors `(^, $)` are used to check if a pattern is at the beginning of the input or
the end. But if we want the anchors to work on each line, we use
the `m` flag. For example, the regular expression `/at(.)?$/gm` means: a lowercase
`a`, followed by a lowercase `t` and, optionally, anything except
a new line. And because of the `m` flag, the regular expression engine now matches patterns
at the end of each line in a string.

<pre>
"/.at(.)?$/" => The fat
                cat sat
                on the <a href="#learn-regex"><strong>mat.</strong></a>
</pre>

[Test the regular expression](https://regex101.com/r/hoGMkP/1)

<pre>
"/.at(.)?$/gm" => The <a href="#learn-regex"><strong>fat</strong></a>
                  cat <a href="#learn-regex"><strong>sat</strong></a>
                  on the <a href="#learn-regex"><strong>mat.</strong></a>
</pre>

[Test the regular expression](https://regex101.com/r/E88WE2/1)

## 6. Greedy vs Lazy Matching
By default, a regex will perform a greedy match, which means the match will be as long as
possible. We can use `?` to match in a lazy way, which means the match should be as short as possible.

<pre>
"/(.*at)/" => <a href="#learn-regex"><strong>The fat cat sat on the mat</strong></a>. </pre>


[Test the regular expression](https://regex101.com/r/AyAdgJ/1)

<pre>
"/(.*?at)/" => <a href="#learn-regex"><strong>The fat</strong></a> cat sat on the mat. </pre>


[Test the regular expression](https://regex101.com/r/AyAdgJ/2)


## Contribution

* Open a pull request with improvements
* Discuss ideas in issues
* Spread the word
* Reach out with any feedback [![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/ziishaned.svg?style=social&label=Follow%20%40ziishaned)](https://twitter.com/ziishaned)

## License

MIT &copy; [Zeeshan Ahmad](https://twitter.com/ziishaned)
