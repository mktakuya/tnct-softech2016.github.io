---
layout: post
title:  "03 四則演算"
date:   2016-05-19 15:00:00 +0900

---

では、四則演算をやっていきましょう。
計算結果は、printf()関数で表示しましょう。

## printf()の使い方
printf("%d", 計算式); とやると、 %d の部分に計算式の答えが埋め込まれて表示されます。

%d が書いてあれば良いので、例えば

printf("The answer is %d\n", 計算式); などとやるとかっこいいです。

## 足し算
まずは、基本中の基本である足し算からやっていきましょう。
ファイル名は、 addition.c とします。

{% highlight c linenos %}
#include <stdio.h>
int main(void)
{
    printf("%d\n", 10 + 3);
    return 0;
}
{% endhighlight %}


## 引き算
次に、引き算をやってみましょう。
ファイル名は、 subtraction.c とします。

{% highlight c linenos %}
#include <stdio.h>
int main(void)
{
    printf("%d\n", 10 - 3);
    return 0;
}
{% endhighlight %}

## 乗算
乗算（掛け算）をやっていきましょう。
ファイル名は、 multiplication.c とします。

{% highlight c linenos %}
#include <stdio.h>
int main(void)
{
    printf("%d\n", 4 * 3);
    return 0;
}
{% endhighlight %}

## 除算
除算（割り算）です。

まずは、割り切れるときをやりしょう。
ファイル名は、division.c とします。

{% highlight c linenos %}
#include <stdio.h>
int main(void)
{
    printf("%d\n", 10 / 2);
    return 0;
}
{% endhighlight %}

整数同士の割り算で割り切れない時は、あまりは表示されません。
ファイル名は、division2.c とします。

{% highlight c linenos %}
#include <stdio.h>
int main(void)
{
    printf("%d\n", 10 / 3);
    return 0;
}
{% endhighlight %}

## 剰余算
あまりを計算したいときは、剰余算をします。
演算子（記号）は、 % を使います。
ファイル名は、 mod.c とします。

{% highlight c linenos %}
#include <stdio.h>
int main(void)
{
    printf("%d\n", 10 % 3);
    return 0;
}
{% endhighlight %}

もし、"3あまり1"という感じで表示したければ、

    printf("%dあまり%d", 10 / 3, 10 % 3);

というふうにコードを書きます。

## 四則演算と演算子の優先順位
+や-、*や/、%などの記号のことを演算子といいます。

数学で習ったとおり、演算子には優先順位があります。

printf("%d\n", 10 + 2 * 3); // 16と表示される。
printf("%d\n", (10 + 2) * 3); // 36と表示される。

では結果が違うので注意してください。

## 練習問題

1. たかし君は1個70円のりんご5個と、と1個30円のみかんを3個買いました。合計でいくら支払えばいいか求め、printf()関数で表示しなさい。ファイル名は、 takashi.c とします。

2. 上底が 5[cm]、下底が 3[cm]、高さが 3[cm]の台形の面積を求め、printf()関数を使って表示しなさい。ファイル名は、trapezoid.cとします。
