# aframe-stereo-component

> [A-Frame](https://aframe.io) VR用のステレオコンポーネントです。

## デモ
2つのサンプルのデモはプロジェクトページ *(demo unavailable)*で確認できます。

## 機能
- **'stereocam' コンポーネント**: モノスコピック表示（「VRモード」に入っていない状態）において、A-Frameのカメラにどちらの「目」をレンダリングするかを指示します。
- **'stereo' コンポーネント**: エンティティを「右目」または「左目」のどちらに含めるかをA-Frameに指示します。球体に投影されたステレオスコピック動画のレンダリングを可能にします。
- ステレオスコピック動画における、サイドバイサイド方式の正距円筒図法（equirectangular projection）をサポートします。
- レンダリング用のキャンバスに「click」イベントをアタッチすることで、モバイルデバイスでの動画再生を可能にします。

## 使い方

### ブラウザでのインストール

[ブラウザ用のファイル](dist)を直接読み込むことでインストールして使用できます:

```html
<html>
  <head>
    <script src="https://aframe.io/releases/latest/aframe.min.js"></script>
    <script src="aframe-stereo-component.js.min.js"></script>
  </head>
  <body>
    <a-scene>
      <!-- 使用例 -->
      <a-camera position="0 0 10" cursor-visible="false" stereocam="eye:left;"></a-camera>
      <a-entity geometry="primitive: sphere" material="shader: flat; src: #myVideo;" scale="-1 1 1" stereo="eye:left"></a-entity>
      <a-entity geometry="primitive: sphere" material="shader: flat; src: #myVideo;" scale="-1 1 1" stereo="eye:right"></a-entity>
    </a-scene>
  </body>
</html>
```

## ライセンス
MIT License — [LICENSE](LICENSE) を参照してください。
