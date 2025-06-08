## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
  ・エンドポイント：https://zipcloud.ibsnet.co.jp/api/search
  ・機能：日本の郵便番号から対応する住所を取得することができるAPI。
* リクエストとレスポンスのフォーマット
  ・リクエスト：https://zipcloud.ibsnet.co.jp/api/search
  ・レスポンス：‣status,ステータス,正常時は 200、エラー発生時にはエラーコードが返される。
  ‣message,メッセージ,エラー発生時に、エラーの内容が返される。
  ⊡results‣検索結果が複数存在する場合は、以下の項目が配列として返される
  ‣zipcode,郵便番号,7桁の郵便番号。ハイフンなし。
  ‣prefcode,都道府県コード,	JIS X 0401 に定められた2桁の都道府県コード。
  ‣address1,都道府県名
  ‣address2,市区町村名
  ‣address3,町域名
  ‣kana1,都道府県名カナ
  ‣kana2,市区町村名カナ
  ‣kana3,町域名カナ
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
  ・API：PoleAPI(ポケモン情報API)
  ・名称：https://pokeapi.co/
* エンドポイントと機能
  ・エンドポイント：https://pokeapi.co/api/v2/pokemon/${encodeURIComponent(name)}
  ・機能：指定したポケモンに関する基本情報を取得できるAPI。
* リクエストとレスポンスのフォーマット
  ・リクエスト：GET https://pokeapi.co/api/v2/pokemon/ditto
  ・レスポンス:‣id:ポケモンのID
  ‣name:ポケモンの名前
  ‣types:タイプ
  ‣abilities:特性
  ‣height/weight:高さ・重さ
### Q3-3. 感想
* 今回の課題で苦労したこと
  ・APIの構造を理解し正しく表示させるところに苦労した
* 演習を通して理解できたこと
  ・Web APIは基本的に「リクエストを送る→JSONでレスポンスを受け取る」という流れであること
* Web APIの利便性や課題など
  ・WebAPIを使えば自分で作ったWebアプリで取り込めるから便利だと思った
