/生產力倍化-Google Cloud 工作術-免費批量下載youtube影片並生成字幕檔
這主要是給自己(一個新手小白)看的筆記,歡迎專業人士多多交流指教!

在Google Colab使用python和youtube-dl下載影片/mp3到google drive
>使用youtube-dl庫下載影片/mp3
>將檔案儲存到google drive
如下載的是影片檔則使用cloud convert將檔案轉為mp3
>使用cloud convert庫將影片轉為mp3
將檔案下載並解壓縮到本地電腦資料夾
>將檔案從google drive下載到本地電腦
>解壓縮檔案
將本地電腦資料上傳到Cloud Storage (Google)
>使用google cloud storage庫將檔案上傳到雲端
使用Speech to Text功能調用Cloud Storage中的檔案進行語音轉文字
>使用google speech to text庫對上傳的檔案進行語音轉文字
得到字幕檔
>將轉換後的文字儲存為字幕檔


相關連結:

youtube-dl: https://rg3.github.io/youtube-dl/
(直接在colab上運行!pip install youtube-dl就可以了,另外youtube-dl下載的檔案要使用ffmpeg轉檔,我是直接使用cloud convert手動轉檔..)
cloud convert: https://cloudconvert.com/
google cloud storage: https://cloud.google.com/storage
google speech to text: https://cloud.google.com/speech-to-text


注意事項:

youtube-dl下載影片/mp3時需要網路連接
cloud convert轉檔需要網路連接且有一定的轉檔時間
需要先建立google cloud storage的帳號並且建立一個儲存桶(類似資料夾的概念)
需要先建立google speech to text的帳號並且申請api key
*Google Cloud和相關功能的免費流量仍有限制,如果大量使用會產生費用,使用時請注意*


使用情境:

需要將youtube上的影片或音樂下載下來並且轉檔成mp3
需要將本地電腦的音檔轉成文字


建議:

youtube-dl和cloud convert的使用最好在colab或是其他雲端環境中使用，因為它們需要網路連接
在將檔案上傳到cloud storage之前，建議先將檔案壓縮，可以節省上傳的時間
google speech to text的語音轉文字功能需要一定的語音資料，如果音檔短小可能無法正確轉換
