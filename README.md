# git-recipes-YutoUchima
enpit

PartA

A1.
% find .git/objects -type f | wc -l

    2
    デフォルトのテンプレートや初期化設定が含まれるオブジェクトが作成されるため。

A2.
% cat .git/HEAD && cat .git/refs/heads/kitchen/YutoUchima     

    .git/HEAD の中身
    ref: refs/heads/kitchen/YutoUchima
    ブランチのファイルの中身
    56be284d632cc7b0bb121defb1cd48ce9cf23de8
