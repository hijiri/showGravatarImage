/**
 * Loggix_Plugin - Show Gravatar Image
 *
 * @copyright Copyright (C) UP!
 * @author    hijiri
 * @link      http://tkns.homelinux.net/
 * @license   http://www.opensource.org/licenses/bsd-license.php  New BSD License
 * @since     2010.05.20
 * @version   10.5.24
 */

●コメント投稿者のGravatar画像を表示するプラグイン

■概略
このソフトウェアは、Loggixでコメントを投稿する際にGravatarに登録したメールアドレスで投稿すると対応する画像を表示するプラグインです。

■詳細
"Recent Comments"とコメント欄に表示されるアイコンを、投稿したメールアドレスに対応するGravatarの画像で表示します。

未登録のメールアドレスや未記入の場合はLoggix標準のアイコンを表示します。

■インストール/アンインストール方法
インストール
    1.Loggixではデフォルトでコメント投稿のメールアドレスを記録しませんので、http://github.com/hijiri/Loggix/commit/a05e504b91487b394f1d2fabfcf7cddaa12db380を参照して3つのファイルを修正してアップロードします。
    2./plugins/へshowGravatarImage.phpをアップロードします。必要であれば画像サイズやratingを設定してください。
    3./modules/comment/theme/comments.htmlへ<?php echo showGravatarImage($item['comments']['id'], $item['comments']['class'])?>をGravatarの画像を表示したい個所へ追加してアップロードします。
    4.デフォルトのテーマではCSSの背景画像と重複するので適宜CSSを修正します。
アンインストール
    1./modules/comment/theme/comments.htmlから<?php echo showGravatarImage($item['comments']['id'], $item['comments']['class'])?>を削除します。
    2./plugins/からshowGravatarImage.phpを削除します。
    3.インストールの4で修正したCSSを元に戻します。
    4.インストールの1での修正は元に戻す必要はありませんが気になる場合は元に戻します。

■使用方法
コメント投稿時にGravatarに登録したメールアドレスを入力して投稿します。

■その他
Loggixのデフォルトテーマに近いスタイルにする場合は、インストールの4で/theme/css/default/default.cssと/theme/css/default/modules.cssの修正をhttp://github.com/hijiri/Loggix/commit/c0c2a8d4fa3e9bed1af12c35ff4bb211c2691526を参照して行います。

■サポート
作者多忙の為サポート出来ません。意見/感想はContactからご連絡ください。

■更新履歴
2010-05-24:公開
