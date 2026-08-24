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

A4.

% git log --oneline | tail -1

    56be284 Initial commit

% git checkout 56be284 && cat .git/HEAD

    Note: switching to '56be284'.
    
    You are in 'detached HEAD' state. You can look around, make experimental
    changes and commit them, and you can discard any commits you make in this
    state without impacting any branches by switching back to a branch.
    
    If you want to create a new branch to retain commits you create, you may
    do so (now or later) by using -c with the switch command. Example:
    
      git switch -c <new-branch-name>
    
    Or undo this operation with:
    
      git switch -
    
    Turn off this advice by setting config variable advice.detachedHead to false
    
    HEAD is now at 56be284 Initial commit
    56be284d632cc7b0bb121defb1cd48ce9cf23de8

% git checkout -b rescue && git checkout kitchen/YutoUchima && git branch -d rescue

    Switched to a new branch 'rescue'
    Switched to branch 'kitchen/YutoUchima'
    Deleted branch rescue (was 56be284).

