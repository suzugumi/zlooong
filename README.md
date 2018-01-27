<!doctype html>
<html lang="ja">

<head>
    <title>zlooong</title>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <link href="https://fonts.googleapis.com/css?family=Raleway+Dots" rel="stylesheet">
    <link rel="stylesheet" href="css/font-awesome.min.css">
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css" integrity="sha384-PsH8R72JQ3SOdhVi3uxftmaW6Vc51MKb0q5P2rRUpPvrszuE4W1povHYgTpBfshb" crossorigin="anonymous">
</head>
<style>
    /* ====検索 自分の足跡==== */
    /* classに ’ KEY ’ がある物は,UIに大きく関係している重要な物 */
    /* classに ’ JS ’ がある物は、javascriptを使っている物*/
    /* classに ’ AAA  ’ がある物は、骨組み。potision:absolute;を使い配置するためだけのベースエリア */
</style>
<!-- header -->

<header class="header">
    <div class="logo"></div>
</header>
<!-- ◆◆◆◆◆◆◆左セクション◆ -->
<!-- 名前決定画面 -->
<div id="mask" class="JS hidden">
    <div id="Confirmation_aria">
        <div class="container">
            <ul>
                <li>本当にこのニックネームで良いですか？</li>
                <li class="JS" id="Confirmation_aria_name"></li>
                <li><a href="#" class="KEY JS" id="Confirmation_Yes_button">はい</a>
                    <a href="#" class="JS" id="Confirmati_NO_button">いいえ</a>
                </li>
            </ul>
        </div>
    </div>
</div>
<!-- 左セクションの骨組み -->
<section class="JS left_section" id="left_section">
    <div class="AAA  left_background"></div>
    <!-- 音声アイコン ONとOFF-->
    <div class="music_icon_aria">
        <span class="KEY JS" id="off_Mute">
            <i class="fa fa-volume-off Configuration" aria-hidden="true"></i>
        </span>
        <span class="JS hidden" id="on_Music">
             <i class="fa fa-volume-up Configuration " aria-hidden="true"></i>
            </span>
    </div>
    <div class="container cf">
        <!-- 左セクションの肉付けテキスト要素 -->
        <div class="left_textAria" id="left_textAria">
            <h1>習慣化＠サポートアプリ</h1>
            <p> 良き習慣＝エサ、をあげて動物を成長させよう！</p>
            <ul class="AAA  text_arialist">
                <li>好きなニックネームを入力してね☆</li>
                <li><input type="text" class="JS" name="" maxlength="8" id="text_input">
                    <input type="button" class="JS" value="決定" id="decision_Button" onkeypress="sample1getValue();">
                    <input type="button" class="JS" id="reset_Button" value="リセット">
                    <!-- <input type="button" class="KEY JS hidden" value="初期化" id="Initializatio_Button"> -->
                </li>
                <li id="NOKORIMOJI" class="JS right">残り文字数:<span class="JS" id="label_num"></span></li>
            </ul>
            <!-- 左セクションのメイン入力エリア ！１！-->
            <div id="left_Main_textAria" class="KEY JS SectionInputAria hidden">
                <!-- 今日やるべき事エリア(左サイド) -->
                <div class="today_list">
                    <ul class="JS" id="today_here">
                        <p class="JS color bolod ">今日やるべき事(７個まで)</p>
                        <!-- ◆◆◆◆◆◆javascriptを使ってインプットエリアを７個生成◆◆◆◆◆◆ -->

                        <div class="decration" id="today_Button">●</div>
                        </li>
                    </ul>
                </div>
                <!-- 明日やるべき事エリア(右サイド) -->
                <div class="tomorrow_list">
                    <ul class="JS" id="tomorrow_here">
                        <p class="JS color bolod ">明日やるべき事(７個まで)</p>
                        <!-- ◆◆◆◆◆◆javascriptを使ってインプットエリアを７個生成◆◆◆◆◆◆ -->

                        <div class="decration">●</div>
                        </li>
                    </ul>
                </div>
                <!-- 左セクションのメイン意思決定エリア ！２！-->
                <div class="AAA  start_menu cf">
                    <!-- 今日やるべきこと -->
                    <div class="today_start">
                        <div class="today_start_aria">
                            <ul>
                                <li>
                                    <input type="button" value="決定" style="padding:10px;" class="JS " id="today_Decision_buttoon">
                                    <input type="button" value="リセット" style="margin-left: 5px; padding:10px;" class="JS button_color" id="today_reset_Button">
                                </li>
                            </ul>
                        </div>
                    </div>
                    <!-- 明日やるべきこと -->
                    <div class="tomorrow_start">
                        <div class="tomorrow_start_aria">
                            <ul>
                                <li>
                                    <input type="button" value="決定" style="padding:10px;" class="JS" id="tomorrow_Decision_butoon">
                                    <input type="button" value="リセット" style="margin-left: 5px; padding:10px;" class="JS button_color" id="tomorrow_reset_Button">
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="start_menu_center">
                        <pre style="user-select:none;">どちらかのやるべき事を入力して決定ボタンを押してね☆</pre>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- ◆右セクション開始◆◆◆◆◆◆◆ -->
<section class="JS right_section cf" id="right_section">
    <!-- やる気スイッチエリア -->
    <div class="slidshow_Aria  AAA  Y_transform" id="slidshow_Aria">
        <div class="slidshow_decoration_aria" id="slid_decoration">
            <i class="fa fa-times-circle right slidshow_close" id="slidshow_close" aria-hidden="true"></i>
        </div>
        <div class="AAA " id="slidshow_base">
            <div id="slid_transform" class="JS KEY">
                <div class="" id="slid_A">
                    <div id="slid_text_A"></div>
                </div>
                <div class="" id="slid_B">
                    <div id="slid_text_B"></div>
                </div>
                <div class="" id="slid_C">
                    <div id="slid_text_C"></div>
                </div>
                <div class="" id="slid_D">
                    <div id="slid_text_D"></div>
                </div>
                <div class="" id="slid_E">
                    <div id="slid_text_E"></div>
                </div>
                <div class="" id="slid_F">
                    <div id="slid_text_F"></div>
                </div>

            </div>
        </div>
        <ul class="slidshow_Aria_list">
            <li>
                <h2>やるきスイッチ<i class="fa fa-power-off" aria-hidden="true"></i></h2>
            </li>
            <li id="slidshow_Aria_list">あなたのやる気きっとよみがえる！</li>
            <li id="slidshow_Aria_list2">自分の思考をスッキリしよう！</li>
            <li> <input type="button" class="button_color " value="START" id="slidshow_Start">
            </li>
        </ul>
    </div>

    <!-- 上からキャラクターが落ちてくる -->
    <div class="diving_CC drag-and-drop Y_transform JS KEY" id="diving_CC"></div>


    <!-- 動物家具エリア -->
    <div class="animal_kagu_aria">
        <div class="animal_kagu1 drag-and-drop hidden JS" id="animal_kagu1"></div>
        <div class="animal_kagu2 drag-and-drop hidden" id="animal_kagu2"></div>
        <div class="animal_kagu3 drag-and-drop hidden" id="animal_kagu3"></div>
    </div>
    <!-- キリン出現ゾーン -->
    <div id="kirin" class="transform"></div>
    <!-- 右セクションのマスクエリア -->
    <div class="right_mask hidden" id="right_mask">
        <div class="r_infoText_aria AAA">
            <div class="r_infoText_Main">
                <ul>
                    <li>はじめまして,,,</li>
                    <li><span id="USER_NAME"></span></li>
                    <li>STARTを押すと、動物カードが</li>
                    <li>１枚ランダムでもらるよ,,,</li>
                    <li>動物カードが、習慣化をサポートするかも,,,</li>
                </ul>
            </div>
            <div class="r_infoText_Decision">
                <a href="#" id="TODAY_INFO_START">START</a>
            </div>
        </div>
    </div>

    <!-- 明日やるべき事用のマスク-->
    <div class="tomorrow_mask hidden" id="tomorrow_mask">
        <div class="r_infoText_aria AAA">
            <div class="r_infoText_Main">
                <ul>
                    <li>どうも,,,</li>
                    <li>STARTを押すと、特別なアバター</li>
                    <li>がランダムでもらるよ,,,</li>
                    <li>アバターをすきなとこに配置して</li>
                    <li>毎日、習慣化して集めよう,,,</li>
                </ul>
            </div>
            <div class="r_infoText_Decision">
                <a href="#" id="TOMORROW_INFO_START">START</a>
            </div>
        </div>
    </div>
    <!-- right_background_base0は右セクションの背景の骨組 -->
    <div class=" right_background_base0 hidden  AAA" id="right_background_base0">
        <!-- カードエリア -->
        <div class="KEY card_aria1 AAA ">
            <div class="card_packageBG2 AAA ">
                <div class="packageBacground2 JS KEY" id="card_packageBacground"></div>
            </div>
            <!-- カードテキスト -->
            <div class="card_text_packageBG2 AAA ">
                <div class="card_text_packageBG2_title">
                    ５分でもやってみよう！
                </div>
                <div class="KEY JS card_text_packageBG2_Main" id="card_text_packageBG2_Main">
                    <!-- 格言 -->
                </div>
                <div class="KEY JS legend_packageBG2" id="legend_packageBG2">
                    <!-- 偉人名前 -->
                </div>
            </div>

            <!-- カードパッケージ -->
            <div class="card_package3 AAA ">
                <div class="CC_icon KEY JS " id="card_package3_CC"></div>
            </div>
            <!-- カードのフレーム -->
            <div class="card_flame KEY" id="card_flame">
                <div class="card_ringo_icon AAA">
                    <div class="ringo_icon inhover AAA" id="ringo_Button">
                        <div class="ringo_icon_text AAA KEY JS" id="ringo_icon_text"></div>
                    </div>
                </div>
            </div>
            <!-- ツイッターアイコン -->
            <div class="twitter_icon_aria AAA JS KEY">
                <a href="https://twitter.com/intent/tweet?button_hashtag=zlooong&ref_src=twsrc%5Etfw" class="twitter-hashtag-button" data-text="zlooong" data-lang="ja" data-show-count="false">
                    <i class="fa fa-twitter twitter_icon JS KEY" id="twitter_icon" aria-hidden="true"></i>
                </a>
            </div>
            <div class="dekpon_icon_aria AAA JS KEY" id="dekpon_icon">
                <div class="dekpon_icon"></div>
            </div>

            <div class=" JS card_CC_name AAA ">
                <div class="KEY card_CC_name_JS" id="card_CC_name_JS"></div>
            </div>
        </div>
    </div>


    <!-- カードエリアおわり -->
    <div class="left_section_doa AAA  ">
        <!-- <<画面拡大ボタン -->
        <span id="left_Open" class="KEY JS">
                <i class="fa fa-backward Configuration" aria-hidden="true"></i>
            </span>
        <span id="left_Colose" class=" JS hidden">
                <i class="fa fa-forward Configuration" aria-hidden="true"></i>
            </span>
    </div>

</section>

<body>
    <script src="js/main.js "></script>
    <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</body>

</html>