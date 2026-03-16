## プロジェクトの概要

このリポジトリは、`OpenFOAM`（`pimpleFoam`）と `ParaView` を用いて、室内におけるウイルスを含むエアロゾルの挙動を再現・可視化するためのCFDシミュレーション環境をまとめたものです。

建築環境分野・室内空気質の研究を行う方が、なるべく迷わずにシミュレーション環境を構築・改変できることを目的としています。

環境構築手順については、以下の前編記事で詳しく解説しています。

[【室内エアロゾルCFD：前編】OpenFOAM（pimpleFoam）環境構築の完全ガイド](https://zenn.dev/satotakahumi)

**このリポジトリはforkやcloneを行い、自由に改変して利用していただいて問題ありません。**

## Usage

環境構築が完了していることを前提に、最短でシミュレーションを実行する手順は次のとおりです。

```bash
# リポジトリを取得
git clone https://github.com/Bakado0704/hokudai-pimplefoam-cfd.git

# ディレクトリへ移動
cd hokudai-pimplefoam-cfd

# 計算実行
./Allrun
```

計算結果を削除してやり直したい場合は、以下を実行してください。

```bash
./Allclean
./Allrun
```

## Requirements（前提環境）

本リポジトリは、以下の環境を前提としています。

**【OS】**
- Windows10/11（blueCFD-Core 前提）

**【CFD】**
- `blueCFD-Core 2024`（`OpenFOAM`をWindows上で利用するため）
- `OpenFOAM`（pimpleFoam ソルバを使用）
- `ParaView`（粒子挙動の可視化および CSV エクスポート用）

**【バージョン管理】**
- `Git`（このリポジトリの取得・更新用）

## このリポジトリでできること

- **粒子挙動の可視化**:  
  `ParaView`を用いて、室内空間内のエアロゾル粒子の移動・滞留の様子を時系列で確認できます。

- **粒子データの出力**:  
  全粒子の座標をタイムステップごとのCSVとして保存し、粒子密度・滞留時間などの解析に利用できます。

