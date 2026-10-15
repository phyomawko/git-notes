# Cheetsheet for Time Travel in Git

1. git checkout 

မိမိရဲ့ ကုဒ်တွေကို အမှန်တကယ် time travel မလုပ်သေးဘဲ ခေတ္တခဏပြန်ကြည့်လိုသောအခါတွင်သုံးသည်

အောက်တွင်မြင်ရသည်မှာ checkout မလုပ်ခင်တွင်မြင်ရသောအနေအထားဖြစ်သည်
![alt text](<git graph ss before checkout.png>)

ထိုပုံအရ first commit, second commit , third commit ဟူသော commit သုံးခုရှိနေသည်။ ထိုအနေအထားတွင် "second commit"  တင်ပြီးချိန်ရှိနေသောအနေအထားကို ခဏပြန်ကြည့်ချင်တယ်ဆိုကြပါစို့ 
ပထမဦးစွာ "git log --oneline" ဖြင့် history  ကိုပြန်ကြည့်ပါမယ် 

![alt text](<check git history.png>)
အထက်ပါအတိုင်းမြင်ရပါမယ် second commit ကိုခဏပြန်ကြည့်ချင်တဲ့အတွက် 
git checkout eb1917e ကို run လိုက်ပါမယ် ထိုအခါ git histroy timeline သည်အောက်ပါပုံအတိုင်းဖြစ်သွားပြီး ကုဒ်များသည်လည်း  second commit တင်ပြီးချန်အနေအထားကိုခေတ္တပြန်လည်ရောက်ရှိသွားသည်ကိုတွေ့ရပါလိမ့်မယ်
![alt text](<git graph ss after checkout.png>)
သို့သော် ထိုအနေအထားသည် second commit အနေအထားသို့ permanent ရောက်ရှိသွားခြင်းမဟုတ်ဘဲ နောက်ဆုံး commit ဖြစ်သည့် third commit သို့အချိန်မရွေးပြန်လည်သွားရောက်နိုင်သညိ့အနေအထားဖြစ်သည်  နောက်ဆုံး commit သို့ပြန်လည်သွားရောက်လိုပါက git checkout main ကိုပြန်လည် run ပေးနိုင်သည် ထို အခါ checkout မလုပ်ခင်အနေအထားသို့ပြန်လည်ရောက်ရှိသွားသည်ကိုတွေ့ရမည်
![alt text](<git graph ss before checkout.png>)

အချုပ်အားဖြင့်ဆိုရသော် git checkout ကိုမူရင်းကုဒ်အနေအထားတစ်စုံတစ်ရာမပျက်ယွင်းစေဘဲ ေရှ့တွင်တင်ခဲ့သော ကုဒ်များကိုခဏပြန်လည်ကြည့်ရှုလိုသောအခါတွင်သုံးသည် 

2. git revert

ကုဒ်များကိုခဏပြန်ကြည့်ချင်ယုံမဟုတ်ဘဲ ထာဝရပြန်လည်သွားရောက်လိုသောအခါတွင်သုံးသည်
နမူနာအရ second commit ကို revert လုပ်လိုသောကြောင့် git revert eb1917e ကိုသုံးသည် ထိုအခါ ကုဒ်များသည် second commit မတင်ခင်အနေအထားသို့ uncommited changes များပေါ်လာပြီး အောက်ပါပုံအတိုင်းဖြစ်လာသည်

![alt text](<conflict after revert.png>)

incoming change သည် second commit ကိုမတင်ခင်ကကုဒ်များဖြစ်ပြီး ထိုအရင် ကုဒ်များကိုconfirm ပေးလိုက်ပါက second commit မတင်ခင်ကကုဒ်များကို commit အသစ်တစ်ခုဖြင့်မှတ်သားပြီး အသစ်ပြင်ပေးလိုက်သည်ကိုအောက်ပါအတိုင်းတွေ့ရလိမ့်မည်
![alt text](<git graph ss after revert.png>)


