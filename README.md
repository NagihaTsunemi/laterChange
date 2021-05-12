# API仕様

| No  | API名                                        | URI                                     | メソッド | 概要                                           |
| :-: | -------------------------------------------- | --------------------------------------- | -------- | -------------------------------------------- |
| 1   | [勤務形態](#workingStyles)                    |                                          |          |                                              |
| 1-1 | [勤務形態情報取得（一覧）](#GET勤務形態情報取得（一覧）) | /workingStyles                      | GET      | 勤務形態情報一覧を取得する。                     |
| 1-2 | [勤務形態情報取得（個別）](#GET勤務形態情報取得（個別）) | /workingStyles/:workingStyleCode    | GET      | 勤務形態情報を取得する。                        |
| 1-3 | [勤務形態情報登録](#POST勤務形態情報登録)     | /workingStyles                               | POST     | 勤務形態情報を登録する。                        |
| 1-4 | [勤務形態情報更新](#PUT勤務形態情報更新)      | /workingStyles/:workingStyleCode             | PUT      | 勤務形態情報を更新する。                        |
| 1-5 | [勤務形態情報削除](#DELETE勤務形態情報削除)   | /workingStyles/:workingStyleCode             | DELETE   | 勤務形態情報を削除する。                        |

## /workingStyles

### GET:勤務形態情報取得（一覧）

| API名        | 勤務形態取得（一覧）               |
| ------------ | ------------------------------ |
| 概要         | 勤務形態一覧（マスタ）を取得する。 |
| アクセスURI  | /workingStyles                    |
| HTTPメソッド | GET                            |
| 備考         |                                |

#### 要求データ

- なし

#### 応答データ

| キー           | 名称         | 備考     |
| -------------- | ------------ | -------- |
| ※下記JSON参照 | 検索結果一覧 | JSON形式 |

``` ts
[
  {
    workingStyleCode: string,
    workingStyleName: string,
    workingStyleAbbreviation: string,
    startTime: string,
    endTime: string,
    workingTimes: number,
    date: number,
    displayOrder: number,
    overtimeTargetKubunCode: string,
    unregisteredCheckTargetFlag: boolean,
    invalidFlag: string,
  }
]
```
## GET:勤務形態情報取得（個別）

| API名        | 勤務形態取得（個別）              |
| ------------ | ------------------------------ |
| 概要         | 指定された勤務形態を取得する。      |
| アクセスURI  | /workingStyles/:workingStyleCode |
| HTTPメソッド | GET                             |
| 備考         |                                 |

#### 要求データ

| キー             | 名称          | 備考             |
| ---------------- | ------------ | ---------------- |
| workingStyleCode | 勤務形態コード | パスパラメーター   |

#### 応答データ

| キー           | 名称         | 備考     |
| -------------- | ------------ | -------- |
| ※下記JSON参照 | 検索結果     | JSON形式 |

``` ts
{
    workingStyleCode: string,
    workingStyleName: string,
    workingStyleAbbreviation: string,
    startTime: string,
    endTime: string,
    workingTimes: number,
    date: number,
    displayOrder: number,
    overtimeTargetKubunCode: string,
    unregisteredCheckTargetFlag: boolean,
    invalidFlag: string,
}
```

## POST:勤務形態情報登録

| API名        | 勤務形態情報登録              |
| ------------ | -------------------------- |
| 概要         | 勤務形態情報を登録する。       |
| アクセスURI  | /workingStyles               |
| HTTPメソッド | POST                        |
| 備考         |                             |

#### 要求データ

- なし

#### 応答データ

| キー           | 名称         | 備考     |
| -------------- | ------------ | -------- |
| ※下記JSON参照 | 検索結果     | JSON形式 |

``` ts
{
    workingStyleCode: string,
    workingStyleName: string,
    workingStyleAbbreviation: string,
    startTime: string,
    endTime: string,
    workingTimes: number,
    date: number,
    displayOrder: number,
    overtimeTargetKubunCode: string,
    unregisteredCheckTargetFlag: boolean,
    invalidFlag: string,
}
```

## PUT:勤務形態情報更新

| API名        | 勤務形態情報更新                 |
| ------------ | ------------------------------ |
| 概要         | 勤務形態情報を更新する。           |
| アクセスURI  | /workingStyles/:workingStyleCode |
| HTTPメソッド | PUT                             |
| 備考         |                                |

#### 要求データ

| キー             | 名称          | 備考             |
| ---------------- | ------------ | ---------------- |
| workingStyleCode | 勤務形態コード | パスパラメーター   |

#### 応答データ

| キー           | 名称         | 備考     |
| -------------- | ------------ | -------- |
| ※下記JSON参照 | 検索結果     | JSON形式 |

``` ts
{
    workingStyleCode: string,
    workingStyleName: string,
    workingStyleAbbreviation: string,
    startTime: string,
    endTime: string,
    workingTimes: number,
    date: number,
    displayOrder: number,
    overtimeTargetKubunCode: string,
    unregisteredCheckTargetFlag: boolean,
    invalidFlag: string,
}
```

## DELETE:勤務形態情報削除

| API名        | 勤務形態情報削除                   |
| ------------ | ------------------------------- |
| 概要         | 勤務形態情報を削除する。            |
| アクセスURI  | /workingStyles/:workingStyleCode  |
| HTTPメソッド | DELETE                           |
| 備考         |                                 |

#### 要求データ
| キー             | 名称          | 備考             |
| ---------------- | ------------ | ---------------- |
| workingStyleCode | 勤務形態コード | パスパラメーター   |

#### 応答データ

- なし
