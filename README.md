iOS UIAlertController・UIAlertActionのサンプル(Swift3)

# UIAlertController
## 概要
UIAlertControllerはアラートおよびアクションシートを管理するクラスです。

## 関連クラス
UIViewController
　
## 実装手順
1. ViewControllerでUIAlertControllerオブジェクトを生成します。（アラート用とアクションシート用の２つ）
2. storyboardからViewControlleに紐付けたUIButtionのアクションでアラートおよびアクションシートを表示します。

## イニシャライザ

|イニシャライザ|説明|サンプル|
|---|---|---|
|init(title: String?, message: String?, preferredStyle: UIAlertControllerStyle)| 各引数にプロパティにセットして、UIAlertControllerオブジェクトを生成する| let alert = UIAlertController(title: "タイトル", message: "本文", preferredStyle: .alert) |

## 主要プロパティ

|プロパティ名|説明|サンプル|
|---|---|---|
|title | タイトル（Read Only） | alert.title |
|message | 本文（Read Only）| alert.message |
|preferredAction | 強調表示するかどうか（アラートのみ） | alert.preferredAction |
|actions | 設定されているUIAlertActionの配列 | alert.actions |

## 主要メソッド

|メソッド名|説明|サンプル|
|---|---|---|
|addAction(_:) | UIAlertActionを追加する| alert.addAction(cancelAction) |
|addTextField(configurationHandler: ) | UITextFieldを追加する。（アラートのみ） |alert.addTextField(configurationHandler: {(text:UITextField!) -> Void in}|

## Constants

|定数名|説明|サンプル|
|---|---|---|
|UIAlertControllerStyle |UIAlertControllerのスタイルについての列挙型 | // アクションシート <br> .actionSheet <br> // アラート <br> .alert| 

## フレームワーク
UIKit.framework

## サポートOSバージョン
iOS8.0以上

## 参考
https://developer.apple.com/reference/uikit/uialertcontroller

# UIAlertAction
## 概要
UIAlertActionはアラートおよびアクションシートのアクションを管理するクラスです。

## 関連クラス
NSObject
　
## 実装手順
1. ViewControllerでUIAlertActionオブジェクトを生成します。
2. UIAlertControllerオブジェクトを生成し、UIAlertActionオブジェクトをセットします。

## イニシャライザ

|イニシャライザ|説明|サンプル|
|---|---|---|
|init(title: String?, style: UIAlertActionStyle, handler: ((UIAlertAction) -> Void)?)| 各引数にプロパティにセットして、UIAlertActionオブジェクトを生成する| let cancelAction = UIAlertAction(title: "cancel", style: .cancel) { _ in print("cancel")} |

## 主要プロパティ

|プロパティ名|説明|サンプル|
|---|---|---|
|title | タイトル（Read Only） | actiont.title |
|style | スタイル（Read Only）| action.style |

## Constants

|定数名|説明|サンプル|
|---|---|---|
|UIAlertActionStyle |UIAlertActionのスタイルについての列挙型 | // キャンセル <br> .cancel <br> // デフォルト <br> .default <br> // ディストラクティブ <br> .destructive| 

## フレームワーク
UIKit.framework

## サポートOSバージョン
iOS8.0以上

## 参考
https://developer.apple.com/reference/uikit/uialertaction

# 開発環境
|category | Version|
|---|---|
| Swift | 3.0.2 |
| XCode | 8.2.1 |
| iOS | 10.0〜 |
