Git command line: Git Bash
 
Local là cục source ở máy. Remote là branch của repository thấy ở Inventory [github, gitlab, bitbutket etc]

git clone  git://github.com/xxx/yyy.git: clone repository về local

git fetch: compare local và remote có thay đổi gì

git fetch && git checkout <branch_name>: switch local đến <branch_name> NẾU tồn tại branch này ở remote. Ngược lại, branch mới tên <branch_name> sẽ được tạo từ branch đang đứng hoặc default branch khi không đứng ở branch nào hết.

git merge origin/<branch_name>: merge branch <branch_name> vào branch đang đứng. Nếu command line hỏi linh tinh comment cho commit thì bấm :q để skip.

git merge -X ours/theirs origin/<branch_name>: resolve conflict với việc override từ <branch_name> [theirs] hoặc từ branch remote đang đứng [ours].

git push origin <branch_name>: sử dụng sau git merge để push nhưng thay đổi từ local lên remote. Hoặc push những file đã commit vô branch local lên remote.

git push -f origin <7_chữ_đầu_của_hashcommit>:<branch_name>: reset REMOTE tới hashcommit. Những commit sau hashcommit sẽ bị mất hêt.

git log: xem log commit của local và remote.

git status: xem những file change ở local.

git reset --hard origin <branch_name>: reset local cho giống với remote.

git reset <hashcommit>: reset local đến cái commit <hashcommit>. Dùng git log để lấy <hashcommit># SuDungGit
