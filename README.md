# caidatgittrenmacos
Cài đặt Git trên Mac OSX

Kiểm tra xem Git đã được cài đặt trên Mac OSX hay chưa?
1- Mở Terminal
2- Kiểm tra version hiện tại của Git nếu đã cài bằng lệnh git –version
3- Kiểm tra Git được cài ở thư mục nào bằng lệnh which git


Nếu Git chưa cài thì có 2 cách để cài.
Trường hợp 1: Cài XCode sau đó cài Command Line Tools (mở XCode > Preferences… chọn tab Downloads để kiểm tra).
Khi này Command Line Tools tự động cài Git client ở thư mục /usr/bin

Trường hợp 2: Bạn không dùng XCode để lập trình mà dùng tool khác để lập trình. Khi này cần cài đặt Git từ Bộ cài Git cho MacOSX ở đây . Git sẽ được cài ở thư mục /usr/local/git. File chạy thực sự sẽ ở /usr/local/git/bin/git

Thường thì version git do XCode command line tools thấp hơn bản Git mới nhất tải về từ http://git-scm.com/. Nếu bạn thích dùng phiên bản mới hơn thì phải sửa biến $PATH để ưu tiên tìm git ở /usr/local/git trước.
1- Mở Terminal, gõ lệnh edit ~/.bash_profile HOẶC vi ~/.bash_profile HOẶC subl ~/.bash_profile HOẶC mate ~/.bash_profile
2- File .bash_profile sẽ được mở bằng trình soạn text mặc định trong Mac của bạn. Bổ xung các dòng sau đây

GIT_HOME=/usr/local/git
PATH=${GIT_HOME}/bin:${PATH};export PATH
MANPATH=${GIT_HOME}/share/man:${MANPATH};export MANPATH

3- Đóng Terminal, mở lại rồi gõ which git
xem kết quả có phải là thư mục /usr/local/git/bin/git không?
