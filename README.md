# git-recipes-YutoUchima
enpit

PartA

A1.

% find .git/objects -type f | wc -l

    ファイルの数　2
    0でないのは、デフォルトのテンプレートや初期化設定が含まれるオブジェクトが作成されるため。

A2.

% cat .git/HEAD && cat .git/refs/heads/kitchen/YutoUchima     

    .git/HEAD の中身
    ref: refs/heads/kitchen/YutoUchima
    
    ブランチのファイルの中身
    56be284d632cc7b0bb121defb1cd48ce9cf23de8

A3.

% git cat-file -p HEAD^{tree}

    ファイルモード、オブジェクトのタイプ、ハッシュ値、ファイル名が並んでいる。
    100644 blob 6042ac74512ee9a17b36ac44544350faee1dee89	README.md
