Hướng dẫn sử dụng git

add key git: eval "$(ssh-agent -s)" && ssh-add ../key/


1. Config git:
  -  git config user.email "hieu@gmail.com"
  -  git config user.name "Minh Hieu"
2.  Sửa commit cuối cùng:
  -   sửa code
  -   git add 
  -  git commit --amend --no-edit
  -  git push origin nhánh -f

3. Đổi name, mail người commit
  - git commit --amend --author="Minh Hiếu <hieu.com>" --no-edit

4. Nếu đổi tên commit thì dùng
  - git commit --amend -m "tên commit mới“

5. Đổi tên branch
  - Nếu bạn đang ở branch bạn muốn đổi tên:
  - git branch -m new-name
  - Còn nếu bạn đang trên 1 branh khác:
  - git branch -m old-name new-name
  - Xóa branch old-name trên remote và push new-name từ local lên remote:
    + git push origin :old-name new-name
  - Sửa lại upstream cho new-name trên local để sau này nó push lên new-name trên remote
    + git push origin -u new-name

6. Lỗi: fatal: Not possible to fast-forward, aborting.
  - xoá checkout sang branch khác rùi xor branch lỗi, rùi git fetch ten nhánh đã xoá rùi checkout snag tên nhánh đã xoá

7. Tạo patch sửa file ( cả php lẫn js )
  -  git diff --patch app/code/xxx > 354.patch    - tạo file patch
  -  git apply -R 354.patch       - revert code
  -  git apply 354.patch            - add new code
  -  git apply m2-hotfixes/PACIFICA_341.patch
    
8. 


Note: 
- Nếu clone về bị modified thì sudo nano .git/config -> sửa filemode = false
- 
