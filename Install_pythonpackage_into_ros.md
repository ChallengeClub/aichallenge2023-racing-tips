# AIchallenge環境へのpythonライブラリの追加方法
## 評価サーバーへのpythonパッケージ追加方法
rosdepを使えば、パッケージビルド時に必要なパッケージをインストールしてくれます。
評価サーバー側でも[Dockerfile](https://github.com/AutomotiveAIChallenge/aichallenge2023-racing/blob/main/docker/evaluation/Dockerfile)内で以下のrosdep installが実行されているので、
これに従ってインストールできるようにpackage.xmlを記載しておけば、評価サーバ環境でもパッケージを追加できそう。
```
  rosdep update; \
  rosdep install -y -r -i --from-paths src --ignore-src --rosdistro $ROS_DISTRO;
```
学習側環境では実行されていないので、[build_autoware.sh](https://github.com/AutomotiveAIChallenge/aichallenge2023-racing/blob/main/docker/aichallenge/build_autoware.sh)に上記を追加しておくと便利。

## Pytorch の追加方法
package.xml に下記を追加する。
```package.xml
  <exec_depend>python-pytorch-pip</exec_depend>
```
以下がインスールされます。
```
torch                                2.1.2
torchvision                          0.16.2
```

## tensorflow の追加方法
package.xml に下記を追加する。
```package.xml
  <exec_depend>python-tensorflow-pip</exec_depend>
```
以下がインスールされます。
```
tensorflow                           2.15.0.post1
tensorflow-estimator                 2.15.0
tensorflow-io-gcs-filesystem         0.35.0

```
## onnxruntime-gpu の追加方法
package.xml に下記を追加する。
```package.xml
  <exec_depend>python3-onnxruntime-gpu-pip</exec_depend>
```
以下がインスールされます。
```
onnxruntime-gpu                      1.16.3
```

## onnxruntime の追加方法
package.xml に下記を追加する。
```package.xml
  <exec_depend>python3-onnxruntime-pip</exec_depend>
```
以下がインスールされます。
```
onnxruntime                          1.16.3
```
