# Different Types of Git Merget Strategies

git merge strategy ၂မျိုးရှိသည် အဲ့ဒါတွေက 
၁.  fast forward
၂.  non fast forward တို့ဖြစ်သည်

1. fast forward
main branch တွင် a နဲ့ b ဟူ၍ commit 2ခုရှိသည်ဆိုပါစို့ ထိုအချိန်တွင် feat/test ဟူသော branch တစ်ခုကို main branch မှထပ်ခွဲ၍ c နဲ့ d ဟူသော commit နှစ်ခုကိုထပ်တင်လိုက်သည် ပုံကိုကြည့်ပါ
![alt text](<git graph ss of same history.png>)
ထိုပုံအရ main branch တွင် commit တစ်ခုထပ်မလုပ်သ၍  history တူနေမည်ဖြစ်သည် ထိုအချိန်တွင် feat/test ကို main branch merge လိုက်ပါက history တူနေသည့်အတွက် fast foward နည်းဖြင့် merge သွားမည်ဖြစ်သည်
![alt text](<git graph ss of fast foward merge.png>)
ပုံအရ graph သည်တစ်ဖြောင့်ထဲဖြစ်နေပြီး ကြည့်ရသည်မှာအလွန်ရိုးရှင်းသည် 

2. non fast forward
![alt text](<git graph ss of non fast foward.png>)
အထက်ပါအခြေအနေတွင် non fast forward ဖြင့် merge လိုက်ပါက source branch မှကုဒ်များသည် timelime အသစ်တစ်ခုဖြင့်ခွဲသွားပြီး target branch တွင် uncommitted change များအဖြစ်ဝင်သွားသည်ကိုတွေ့ရမည်
![alt text](<git graph ss of non fast foward after commit.png>)
commit လုပ်ပြီးမှသာလျှင် source branch မှကုဒ်များ ေရာက်လာပြီး commit အသစ်တစ်ခုဖြစ်သွားသည် 

ပုံမှန်အားဖြင့် source branch နဲ့ target branch history တူပါက fast foward ဖြင့် merge လေ့ရှိပြီး မတူပါက non fast forward ဖြင့် merge လေ့ရှိသည် 

