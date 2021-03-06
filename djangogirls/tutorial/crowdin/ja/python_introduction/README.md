# Introduction to Python

> このチャプターの一部はGeek Girls Carrots (http://django.carrots.pl/) のチュートリアルに基づいています。

さあ、コードを書いてみましょう！

## Python prompt

Pythonであそぶために、コマンドライン を開きましょう。 やり方は、チャプター Intro to Command Line で学びましたね。

準備ができたら、次の指示に従ってやってみましょう。

Pythonコンソールを開きましょう。Windowsならpython、Mac OSやLinuxならpython3とタイプして Enterキーをおしてください。..

    $ python3
    Python 3.4.3 (...)
    Type "help", "copyright", "credits" or "license" for more information.
    >>>
    

## Your first Python command!

Pythonのコマンドが走ると、プロンプト記号が >>>に変わりました。 これは、今Pythonの言語を実行できますという意味です。 >>>はタイプしなくていいですよ。 - Pythonがあなたの代わりにやってくれます。

Pythonコンソールを終わる時は、exit()　とタイプするか、ショートカットCtrl + Z （Windows）、 Ctrl + D（Mac/Linux）で終了です。 >>> は現れなくなりました。

けど、今はまだコンソールを終了しないで、 もっと動かして学びましょう。 もっと動かして学びましょう。 例えば、簡単な計算をしてみましょう。2 + 3とタイプして、Enterキーを押してください。.

    >>> 2 + 3
    5
    

できました！答えがでてきましたね。Pythonは計算ができます。他にも、次のようなコマンドを試してみましょう: - `4 * 5` - `5-1` - `40/2`

ちょっとの間楽しんであそんでみたら、またココに戻ってきてくださいね

お分かりのとおり、Pythonはステキな計算機ですね. 他になにができるんだろう…と思ったら、次にいってみましょう。

## Strings

あなたのお名前を次のようにクォーテーションをつけてタイプしてください。

    >>> "Ola"
    'Ola'
    

はじめてのString（文字列）が完成です！ Stringとは、文字の集合のことです。 シングルクォーテーション (') あるいは、ダブルクォーテーション (") で囲います。 - クォーテーションの中が文字列であることを意味しています。

複数の文字列を結合することもできます。次のように試してみましょう。

    >>> "Hi there " + "Ola"
    'Hi there Ola'
    

文字列を繰り返すためには、演算子を使って繰り返し回数を指定することもできます。

    >>> "Ola" * 3
    'OlaOlaOla'
    

アポストロフィーを文字列の中に含めたい場合は、２通りの方法があります。

まずは、ダブルクォーテーションを使う方法です。

    >>> "Runnin' down the hill"
    "Runnin' down the hill"
    

あるいは、バックスラッシュ (\)を使う方法もあります。

    >>> 'Runnin\' down the hill'
    "Runnin' down the hill"
    

できましたか？次に、あなたの名前を大文字に変えてみましょう。次のように記述してください。

    >>> "Ola".upper()
    'OLA'
    

ここで`upper` **関数** を使うことができましたね! 関数 (upper()など) は、呼び出したオブジェクト ("Ola"のことです) に対してどのような手順でどのような処理をするかをひとまとめにしたものです。

あなたの名前の文字数を知りたいときは、その関数もあります！

    >>> len("Ola")
    3
    

どうして、文字列の後に. をつけて関数を呼び出したり ("Ola".upper()のように)、あるいは、先に関数を呼び出してかっこの中に文字列をいれているのか、と疑問に思ったかもしれません。 そうですね。時に、オブジェクトに結びついた関数というのがあります。例えば、upper()は、文字列にのみ実行される関数です。 私たちはこれをメソッド (method)と呼びます。 それとは別に、特定のオブジェクトに関連せず、異なるタイプのオブジェクトに対して実行できる関数があります。例えばlen()ですね。 len 関数の引数として"Ola"をかっこの中にいれているのです。

### 概要

文字列はだいじょうぶですね。ここまでに学んだことをまとめましょう。

*   **プロンプト** - Pythonプロンプトにコマンド（コード）を入力すると、答えがかえってきます。
*   **数値と文字列** - 数値は計算に、文字列はテキストに使われます。
*   **演算子** -例えば + や * のように、値を計算して新しい値を返します。
*   **関数** - upper() や len() のようにオブジェクトに対して行う機能のことです。

すべてのプログラミング言語に共通する基礎になります。 もう少し難易度の高いものに挑戦してみましょう。準備はいいですか？

## Errors

さて、新しいことをやってみましょう。あなたの名前の文字数を数えたように、数字の文字列は数えれるでしょうか？ len(304023)と記述して、Enterキーを押してみましょう。

    >>> len(304023)
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: object of type 'int' has no len()
    

はじめてのエラーがでました！オブジェクトタイプ"int" (integers, 数値) は文字数がありませんと言っています。では、どうすればよいでしょうか？この数字を文字列として扱えれば、文字数を数えれるはずですよね？

    >>> len(str(304023))
    6
    

うまく行きました！ `str` 関数を`Len`の中に記述しました。`str()` はその中身を文字列に変換します。

*   `Str` 関数 は**文字列** に変換します
*   `int` 関数 は**文字整数** に変換します

> 数字は文字列にすることはできますが、全ての文字が数字に変換できるわけではありません。 例えば `int('hello')`は数字にはなりませんよね？

## Variables

変数（variables）は、プログラミングの重要なコンセプトです。 後で使うためにつける単なる名札ではありません。 プログラマーは変数を使ってデータを保管したり、 コードを読みやすくして、後でそれが何だったか覚えておかなくてもいいようにします。

変数`name`を新しくつくってみましょう。

    >>> name = "Ola"
    

できましたか？簡単ですね。単純に name イコール（=） Olaと記述するだけです。

見てのとおり、プログラムは、なにも返してくれませんね。では、変数がきちんとあるか、どうやって確かめたらいいのでしょうか？ `name`とタイプして、</code>0>Enterキー</0>をおしてください。

    >>> name
    'Ola'
    

やりました！あなたのはじめての変数ができましたね！代入する値を変えることもできます。

    >>> name = "Sonja"
    >>> name
    'Sonja'
    

関数にも使えます。

    >>> len(name)
    5
    

素晴らしいですね！変数は、もちろん数値にも使えますよ。

    >>> a = 4
    >>> b = 6
    >>> a * b
    24
    

もしも、間違えた変数名を使ってしまったら、どうなるでしょうか？予想できますか？やってみましょう！

    >>> city = "Tokyo"
    >>> ctiy
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    NameError: name 'ctiy' is not defined
    

エラーになりました！ 前回とは違うエラータイプです。**NameError**という、初めてみるエラータイプですね。 作成されていない変数を使った時は、Pythonがエラーを教えてくれます。 もし、このエラーに出くわしたら、記述したコードにタイプミスがないか確認してください。

ちょっと遊んで、何ができるか試してみてくださいね！

## The print function

次に挑戦してみましょう。

    >>> name = 'Maria'
    >>> name
    'Maria'
    >>> print(name)
    Maria
    

単に`name`とタイプした時は、Pythonインタプリタが、変数'name'の *representation*を返します。 ここでは、 M-a-r-i-aという単なる文字の集まりで、シングルクォーテーション（''）に囲われています。 しかし、 print(name)と記述した時は、Pythonは変数の中身を出力します。クォーテーションはありません。

これからさらに詳しくみていきますが、`print()` は、関数から出力をする時や、複数行の出力を行うときにも便利です。

## Lists

数値と文字列の他にも、すべてのオブジェクトタイプを勉強しておきましょう。 **list**というものがあります。 リストは、その名のとおり、オブジェクトの並びをもつものですね。

まずはリストを作りましょう

    >>> []
    []
    

はい、このリストは空っぽです。使いにくいですよね。では、くじ引きの番号のリストを作りましょう。 この番号を何度も繰り返し書きたくはないから、同時に変数に代入してしまいましょう。

    >>> lottery = [3, 42, 12, 19, 30, 59]
    

よし、これでリストができました！このリストで何をしましょうか？では、くじ引きの番号がいくつあるか、数えてみましょう。何の関数を使えばいいか、予想できますか？すでに知っていますよね！

    >>> len(lottery)
    6
    

そうです！`len()` がリストにあるオブジェクトの数を取得できます。便利ですね。では、くじ引きの番号をソートしてみましょう。

    >>> lottery.sort()
    

これは何も返してきません。これはリストに表示される番号を、順番に並べ替えただけです。再度出力して、確かめてみましょう。

    >>> print(lottery)
    [3, 12, 19, 30, 42, 59]
    

ご覧のとおり、小さい順に並び替えられましたね。おめでとう！

逆順に並び替えてみたくなりましたか？やってみましょう。

    >>> lottery.reverse()
    >>> print(lottery)
    [59, 42, 30, 19, 12, 3]
    

簡単でしたね？リストに何かを追加したいときは、次のようにコマンドを記述してください。

    >>> lottery.append(199)
    >>> print(lottery)
    [59, 42, 30, 19, 12, 3, 199]
    

最初の数字だけを出力したいときは、インデックス**indexes**を使って指定することができます。 インデックスは、アイテムがリストのどこにあるかを指す番号です。次のとおり試してみてください。 インデックスは、リストの先頭の要素から順に「０」、次に「１」と割り当てられています。次のとおり試してみてください。 次に挑戦してみましょう。

    >>> print(lottery[0])
    59
    >>> print(lottery[1])
    42
    

このように、リスト名と要素のインデックスを[]に記述することで、指定した要素を取り出すことができます。

上記で学んだように**indexes** を利用してリストから削除をする事もできます。**del** （削除の略）は指定したインデックスの要素を削除します。 例で試してみましょう。リストの最初の要素を削除しています。

    >>> print(lottery)
    [59, 42, 30, 19, 12, 3, 199]
    >>> print(lottery[0])
    59
    >>> del lottery[0]
    >>> print(lottery)
    [42, 30, 19, 12, 3, 199]
    

お見事！

他のインデックスも試して遊んでみてください。例えば、 6, 7, 1000, -1, -6, -1000 などをインデックスに指定するとどうなるでしょうか。コマンドを実行する前に予測してみましょう。結果はどうですか？

ご参考に、こちらのドキュメントにリストメソッドがすべて記されています。 https://docs.python.org/3/tutorial/datastructures.html

## Dictionaries

辞書(ディクショナリ)について確認しましょう。リストに似ていますが、インデックスのかわりにキーと呼ばれる識別子で値を参照します。キーは文字列も数値も使えます。ディクショナリは次のように{}括弧で囲んで作成します。

    >>> {}
    {}
    

これで中身が空っぽのディクショナリができましたね。やったね！

では、つぎのコマンドを記述してみましょう。 (あなた自身の情報に値をおきかえてみてもいいですよ）

    >>> participant = {'name': 'Ola', 'country': 'Poland', 'favorite_numbers': [7, 42, 92]}
    

このコマンドで、0>participant</code> という名前の変数をつくって、３つのキーと値をもつ要素を作成しました。

*   キー `name` が指す値 `'オーラ'` (`string` オブジェクト)
*   キー `country` が指す値 `'Poland'` (`string` オブジェクト)),
*   キー `favorite_numbers/0> は リスト <code>[7, 42, 92]/0>。 (数字を3つ持つlist).</li>
</ul>

<p>次の構文で各キーの値を確認できます。</p>

<pre><code>>>> print(participant['name'])
Ola
`</pre> 
    リストに似ていますね。しかし、ディクショナリーでは、インデックスを記憶する必要がなく、名前でいいのです
    
    もし存在しないキーを参照しようとすると、どうなるでしょうか？予想できますか？実際にやってみましょう！
    
        >>> participant['age']
        Traceback (most recent call last):
          File "<stdin>", line 1, in <module>
        KeyError: 'age'
        
    
    またエラーです。今回は **KeyError**.というエラーが出ました。Pythonは、このディクショナリにキー'age'は存在しませんよ、と教えてくれています。
    
    ディクショナリとリストはどう使い分ければよいのでしょうか？そうですね、これはゆっくり考えてみるべきポイントですね！この後の解答を読むまえに、考えてみてください。
    
    *   必要なのは、順序付けられた一連のアイテムですか？　リストを使いましょう。
    *   キーに対応する値が必要？キーから値を参照する？　ディクショナリを使いましょう。
    
    ディクショナリやリストは、生成後に値を変更できるオブジェクトです。これを *mutable*,と呼びます。
    
        >>> participant['favorite_language'] = 'Python'
        
    
    リストと同様に、`len()` 関数をディクショナリに使ってみましょう。ディクショナリでは、キーと値のペアの数を返します。コマンドを入力してやってみましょう。:
    
        >>> len(participant)
        4
        
    
    お分かり頂けたでしょうか。 :) では、ディクショナリを使ってもう少し練習してみましょう。準備ができたら、次の行にいってみましょう。
    
    ディクショナリの要素を削除する時は、delコマンドを使います。 例えば、 キー`'favorite_numbers'`の要素を削除するには、次のように記述してください。
    
        >>> del participant['favorite_numbers']
        >>> participant
        {'country': 'Poland', 'favorite_language': 'Python', 'name': 'Ola'}
        
    
    このように、'favorite_numbers'のキーと値が削除されます。
    
    同様に、次のように記述することで、すでにあるキーの値を変更することができます。
    
        >>> participant['country'] = 'Germany'
        >>> participant
        {'country': 'Germany', 'favorite_language': 'Python', 'name': 'Ola'}
        
    
    これで、キー'`'country'` 'の値は、`'Poland'` 'から`'Germany'`に変わりました。面白くなってきましたか？その調子です！
    
    ### 概要
    
    素晴らしいです! これで、あなたはプログラミングについて沢山のことを学びました。ここまでのところをまとめましょう。
    
    *   **エラー** - あなたのコマンドをPythonが理解できない時にエラーが表示されます。
    *   **変数** コードを簡単にまた読みやすくするために、文字や数値などのオブジェクトにつける名札。
    *   **リスト** - 複数の値（要素）が順に並んでいるもの。
    *   **dictionaries** キーと値のペアの集合です。
    
    次に進む準備はいいですか？
    
    ## Compare things
    
    比較することは、プログラミングの醍醐味の１つです。簡単に比較できるものといえば、何でしょうか？そうです、数字ですね。さっそくやってみましょう。
    
        >>> 5 > 2
        True
        >>> 3 < 1
        False
        >>> 5 > 2 * 2
        True
        >>> 1 == 1
        True
        >>> 5 != 2
        True
        
    
    Pythonにいくつか比較する数字をあたえてみました。数字を比較するだけでなく、演算式の答えも比較することができます。便利でしょ？
    
    ２つの数字がイコールであるかどうかを比べる時に、イコールの記号が２つ==並んでいます。 Pythonを記述する時、イコール１つ=は、変数に値を代入するときに使います。 ですので、値同士が等しいかどうか比較するときは、**必ず** イコール記号２つ==を記述してください。 等しくないものを求める事もできます。 その時は例のように `!=`と記述します。
    
    次の２つはどうでしょうか
    
        >>> 6 >= 12 / 2
        True
        >>> 3 <= 2
        False
        
    
    `>` と `< `は簡単でしたね。` >= `と` <=` はどうでしょうか？それぞれの意味は、次のとおりです。
    
    *   x > y : x は y　より大きい
    *   x < y : x は y　より小さい
    *   x <= y : x は y　以下
    *   x >= y : x は y　以上
    
    すばらしい! もう少しやってみましょう。
    
        >>> 6 > 2 and 2 < 3
        True
        >>> 3 > 2 and 2 < 1
        False
        >>> 3 > 2 or 2 < 1
        True
        
    
    条件式が複数あって複雑になっても、その答えを出してくれます。とても賢いですね。
    
    *   **and** - andの左辺と右辺が共にTrueの場合、True。
    *   **or** -orの左辺あるいは右辺の少なくとも１つがTrueの時、True。
    
    "comparing apples to oranges"という英語の表現を聞いたことはありますか？文字通り訳すと「リンゴとオレンジを比較する」となり、「比較にならないものを比較する」という意味です。Pythonでも同じようなことをやってみましょう。
    
        >>> 1 > 'django'
        Traceback (most recent call last):
          File "<stdin>", line 1, in <module>
        TypeError: unorderable types: int() > str()
        
    
    Pythonは、数値(int)　と文字列(str)の比較はできません。 **TypeError** とエラーが表示され、２つのオブジェクトタイプが比較できないことを教えてくれています。
    
    ## Boolean
    
    偶然にも、ブール型**Boolean**というあたらしいオブジェクトタイプを学びました。 -- おそらく、ブール型は一番簡単なオブジェクトタイプです。
    
    ブール型は、たった２つの値を持ちます。 - True - False
    
    Pythonを記述するときは、Trueの最初は大文字のT、残りは小文字です。 ** true, TRUE, tRUE **は間違いです。True と記述してください (もちろん False についても同様です。)
    
    ブール型は、次のように変数に代入することもできます。
    
        >>> a = True
        >>> a
        True
        
    
    このようなこともできます。
    
        >>> a = 2 > 5
        >>> a
        False
        
    
    ブール型を使って、練習して遊んでみましょう。次のコマンドを試してみてください。
    
    *   `True and True`
    *   `False and True`
    *   `True or 1 == 1`
    *   `1 != 2`
    
    おめでとうございます！ブール型を理解することは、プログラミングでとても大事です。ここまでできましたね！
    
    # Save it!
    
    ここまでインタプリタでPythonのコードをかいてきました。つまり、コードを１行づつしか書くことができませんでした。 普通のプログラムはファイルに保存され、インタプリタ あるいは コンパイラでプログラミング言語を処理して実行します。 ここまで、私たちはプログラムを１行ごとにPython インタプリタで実行してきました。 ここかっらは、１行以上のコードを実行していきましょう。次のような流れになります。
    
    *   Pythonインタプリタを終了します。
    *   お好きなエディタを起動します。
    *   Pythonファイルとしてコードを保存します。
    *   実行します！
    
    これまで使っていたPythonインタプリタを終了しましょう。 exit() ファンクションを記述してください。
    
        >>> exit()
        $
        
    
    これで、コマンドプロンプトに戻りました。
    
    前のチャプター [code editor][1] で、エディタを紹介しました。エディタを起動して、新しいファイルにコードを書いてみましょう。
    
        python
        print('Hello, Django girls!')
        
    
    > **メモ**コード エディターについてクールなものの一つに気づくべきである: 色! Python コンソールですべてになった同じ色 `印刷` 関数は文字列から別の色であることがわかります。 これは「構文」と呼ばれています「ハイライトする」こと、そして、コーディングとき、それは本当に役に立つ特徴です。 文字の色でタイプミスがないかを確認する事ができます。 これが私たちがコードエディタを使う理由の１つです。
    
    あなたは、すでにベテランのpython開発者です。今日学んだコードを自由に書いてみてください。
    
    コードを書いたら、わかりやすい名前をつけて保存しましょう。 **python_intro.py**と名前をつけて、デスクトップに保存してください。 ファイル名は何でもかまいません。ここで重要なことは、拡張子を**py**とすることです。 コンピュータにこのファイルは**python**で実行するファイルですとおしえます。
    
    ファイルを保存したら、実行してみましょう！コマンドラインのセクションで学んだことを思い出して、ターミナルの **ディレクトリを変更**して、デスクトップにしましょう。
    
    Macでは、コマンドは次のようになります。
    
        $ cd /Users/<your_name>/Desktop
        
    
    Linuxでは、次のようになります。("Desktop"のところは"デスクトップ"と表示されているかも知れません):
    
        $ cd /home/<your_name>/Desktop
        
    
    Windowsでは、次のようになります。
    
        > cd C:\Users\<your_name>\Desktop
        
    
    うまくできない時は、質問してください。
    
    次に、ファイルのコードを実行します。
    
        $ python3 python_intro.py
        Hello, Django girls!
        
    
    できました！これで、あなたはファイルに保存されたPythonプログラムを実行できましたね。いい気分ですね。
    
    では、ここからプログラミングに不可欠のツールを学んでいきましょう
    
    ## If...elif...else
    
    ある条件が成立するときに処理を行いたいという時に用いるのが、**if 条件式**です。.
    
    では、**python_intro.py** ファイルのコードを次のように書き換えてください。
    
        python
        if 3 > 2:
        
    
    これを保存して実行すると、次のようなエラーがでます。
    
        $ python3 python_intro.py
        File "python_intro.py", line 2
                 ^
        SyntaxError: unexpected EOF while parsing
        
    
    条件式 3 > 2　がTrueの時、どのように処理をすべきかが記述されていませんね。 では、Python に “It works!”　と出力してもらいましょう。 **python_intro.py **ファイルの中身を、次のとおりに書き換えてください。
    
        python
        if 3 > 2:
            print('It works!')
        
    
    ２行目をスペース４つでインデントしていることに気が付きましたか？ if文がTrueの時、どのコードを実行するかPythonに知らせる必要があります。 スペース１つでもできますが、ほぼ全員のPythonプログラマーはスペース４つとしています。 タブ１つも、スペース４つと同じです。
    
    保存して、もう一度実行してみましょう。
    
        $ python3 python_intro.py
        It works!
        
    
    ### What if a condition isn't True?
    
    前述の例では、if文の条件式がTrueの時だけ、コードが実行されました。Pythonは、elif や else といった記述もできます。
    
        python
        if 5 > 2:
            print('5 is indeed greater than 2')
        else:
            print('5 is not greater than 2')
        
    
    これを実行した場合、次のように出力されます。
    
        $ python3 python_intro.py
        5 is indeed greater than 2
        
    
    2が５より大きい場合、２行目のコマンドが実行されます。では、 elif　はどうなるのでしょうか？
    
        python
        name = 'Sonja'
        if name == 'Ola':
            print('Hey Ola!')
        elif name == 'Sonja':
            print('Hey Sonja!')
        else:
            print('Hey anonymous!')
        
    
    それを実行すると...
    
        $ python3 python_intro.py
        Hey Sonja!
        
    
    `elif`を追加する事で 、上記の条件が失敗した場合に実行する余分な条件を追加する事ができます。
    
    最初の条件分岐の後に好きなように多くの`elif`を追加する事ができます。例えば...
    
        python
        volume = 57
        if volume < 20:
            print("It's kinda quiet.")
        elif 20 <= volume < 40:
            print("It's nice for background music")
        elif 40 <= volume < 60:
            print("Perfect, I can hear all the details")
        elif 60 <= volume < 80:
            print("Nice for parties")
        elif 80 <= volume < 100:
            print("A bit loud!")
        else:
            print("My ears are hurting! :(")
        
    
    Pythonは上から順番に各条件をテスト、実行し、出力します。
    
        $ python3 python_intro.py
        Perfect, I can hear all the details
        
    
    ### 概要
    
    ３つのエクササイズを通して、これまでに学んだことは、、、
    
    *   **比較** - - 比較に用いる >, >=, ==, <=, < そしてand, or といった演算子があります。
    *   **Boolean** - - True と False ２つの値のみを持ちます。
    *   **ファイルを保存する** - コードはファイルに保存することで、大きなプログラムも実行できます。
    *   **if...elif...else **-- 条件分岐することで、特定の条件によって処理を分けて実行することができます。
    
    では、このチャプターの最後のパートに挑戦していきましょう！
    
    ## Your own functions!
    
    Pythonには`len()`のように関数があったのを覚えていますか？ ここでは、自分で関数を作る方法を学びます。
    
    実行する機能をひとまとめにしたものを関数といいます。 Pythonでは、functionは`def`というキーワードからはじまり、引数を含むことができます。 簡単なものからはじめてみましょう **python_intro.py** の中身を書きのコードに置き換えてください。:
    
        python
        def hi():
            print('Hi there!')
            print('How are you?')
        
        hi()
        
    
    あなたの最初の関数を実行する準備ができましたね!
    
    ここであなたは、最後の行になぜ関数の名前を書いたのだろう、と疑問に感じたかもしれません。 これは、Pythonがファイルを読み、上から下へ実行していくからです。 関数を定義したあとに、もう一度その関数を書いて呼び出します。
    
    では実行して、どうなるか見てみましょう:
    
        $ python3 python_intro.py
        Hi there!
        How are you?
        
    
    簡単にできましたね！次に引数をつかった関数を作ってみましょう。先ほどの例を使います。'hi'という挨拶をする関数に、挨拶をする人の名前をいれてみます。
    
        python
        def hi(name):
        
    
    このとおり、関数に`name`という引数を足します。
    
        python
        def hi(name):
            if name == 'Ola':
                print('Hi Ola!')
            elif name == 'Sonja':
                print('Hi Sonja!')
            else:
                print('Hi anonymous!')
        
        hi()
        
    
    上記のように、`print`関数の前に、インデントを２ついれる必要があります。` if の条件式`が真の時に、なにをすべきかという処理はインデントの後に記述します。 実行して、どのように動くか見てみましょう。
    
        $ python3 python_intro.py
        Traceback (most recent call last):
        File "python_intro.py", line 10, in <module>
          hi()
        TypeError: hi() missing 1 required positional argument: 'name'
        
    
    おっと、エラーがでてしまいました。 Pythonがエラーメッセージを表示してくれています。 定義した関数`hi()`は、`name`という引数が必要ですが、関数を呼び出す時に引数を忘れてしまっています。 最後の行を修正しましょう。:
    
        python
        hi("Ola")
        
    
    実行してください。:
    
        $ python3 python_intro.py
        Hi Ola!
        
    
    では、名前を変えてみたらどうなりますか？
    
        python
        hi("Sonja")
        
    
    再度実行してください。:
    
        $ python3 python_intro.py
        Hi Sonja!
        
    
    では、OlaやSonja以外の名前を入れた時、どうなるかわかりますか？やってみて、予測が正しいか確認して下さい。このように出力されましたか。:
    
        Hi anonymous!
        
    
    すばらしいですね。 挨拶をする人の名前を毎回何度も繰り返して書く必要がなくなりました。 これが関数を作る理由です。何度も繰り返してコードを書く必要はありません！
    
    もっとスマートなやり方を試してみましょう。 --２人以上の名前があり、それぞれに対して条件をつけるのは大変ですよね。
    
        python
        def hi(name):
            print('Hi ' + name + '!')
        
        hi("Rachel")
        
    
    では、実行してみましょう。：
    
        $ python3 python_intro.py
        Hi Rachel!
        
    
    おめでとうございます！Functionsの書き方を学びましたね。:)!
    
    ## Loops
    
    さぁ、もう最後のパートですよ。あっという間ですね。 :)
    
    先ほどお話したとおり、プログラマーはめんどくさがりで、同じことを繰り返すことは好きではありません。プログラミングはすべてを自動的に処理したい。私たちはすべての人の名前ひとつひとつに対して挨拶をしたくないですよね？こういう時にループが便利です。
    
    リストを覚えていますか？女の子の名前をリストにしてみましょう。:
    
        python
        girls = ['Rachel', 'Monica', 'Phoebe', 'Ola', 'You']
        
    
    名前を呼んで、全員にあいさつをしてみましょう。` hi `関数が使えますね。ループの中でつかいましょう。:
    
        python
        for name in girls:
        
    
    この for は if に似ています。この次に続くコードは、４つスペースを入れる必要があります。
    
    ファイルに書かれるコードはこのようになります。
    
        python
        def hi(name):
            print('Hi ' + name + '!')
        
        girls = ['Rachel', 'Monica', 'Phoebe', 'Ola', 'You']
        for name in girls:
            hi(name)
            print('Next girl')
        
    
    実行してみましょう。:
    
        $ python3 python_intro.py
        Hi Rachel!
        Next girl
        Hi Monica!
        Next girl
        Hi Phoebe!
        Next girl
        Hi Ola!
        Next girl
        Hi You!
        Next girl
        
    
    ご覧のとおり、girlsリストのすべての要素に対して、`for `の中にインデントして書かれたことが繰り返されています。.
    
    for 文では、range 関数をつかって指定した回数だけ繰り返すこともできます。:
    
        for i in range(1, 6):
            print(i)
        
    
    これを実行すると、次のように出力されます:
    
        1
        2
        3
        4
        5
        
    
    range関数は、引数に指定した開始と終了の数値から連続する数値の値を要素として持つリスト型のオブジェクトを作成します。
    
    2つ目の引数（終了の数値）は、リストに含まれないことに注意してください。 つまり、 range(1, 6) は、１から５のことであり、６は含まれません。
    
    ## 概要
    
    以上です！**おめでとう！頑張りました！** これは簡単ではなかったと思います。自分を褒めてあげてくださいね。ここまで進めることができたのは、本当に素晴らしいことです！
    
    次のチャプターにうつるまえに、少し気晴らしに、ストレッチやお散歩をして、目や身体を休ませてあげてくださいね。 
    
    ![Cupcake][2]

 [1]: ../code_editor/README.md
 [2]: images/cupcake.png