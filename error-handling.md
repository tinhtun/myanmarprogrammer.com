| Date | URL |
| -----| --- |
| March 26, 2018 | https://myanmarprogrammer.com/error-handling/ |

![Wallpaper](https://images.unsplash.com/photo-1453060113865-968cea1ad53a)

# Error များကိုင်တွယ်ဖြေရှင်းခြင်း
ကုဒ်ရေးပြီဆိုရင် error ဖမ်းတဲ့ကုဒ်တွေပါကိုပါရတာပါပဲ။ မဖမ်းရင်လဲ မရဘူးလေ။ input တွေက Null တွေဖြစ်နိုင်တယ်။ connection လှမ်းချိတ်လို့ မရတာလဲဖြစ်နိုင်တယ်။ လူတိုင်း Null စစ်တဲ့ကုဒ်တွေ try-catch တွေသုံးပြီးရေးတတ်ပါတယ်။ ဒါပေမဲ့ တော်တော်များများမသိကြတာက ကိုရေးလိုက်တဲ့ error ဖမ်းတဲ့ကုဒ်တွေကြောင့် ကို့ program ဟာဖတ်ရခက် နားလည်ရခက်သွားတာမျိုး ဖြစ်လေ့ရှိပါတယ်။ မယုံမရှိနဲ့ ကို့အခုအလုပ်က ကုဒ်တွေဆို လိုင်းပေါင်းတစ်ထောင်လောက်ရှိတဲ့ method တွေမှာ ရေးချင်တဲ့ logic ကတစ်ဝက်လောက်ပဲပါပြီး ကျန်တာက Null မဖြစ်အောင်ရှောင်တာရယ် try-catch တွေကြီးပဲ။ ဖတ်ကြည့်လိုက်ရင် လိုရင်းကိုဘယ်လိုမှကိုနားမလည်နိုင်ပဲ ခေါင်းတွေသာမူးသွားတာပဲအဖတ်တင်တယ်။ အဲဒါစီနီယာဆိုတဲ့ programmer အရင့်အမာကြီးတွေရေးထားတာနော်။
အဲတော့ error မတက်အောင်ကာကွယ်ရတဲ့ကုဒ်တွေကြောင့် ကို့ program ကြီးရှုပ်ရှက်ခက်မသွားအောင် လုပ်လို့ရတဲ့နည်းလမ်းတွေရှိပါတယ်။

## Unchecked Exception သုံးပါ
Java သမားတွေငြင်းလေ့ရှိပါတယ်။ ကိုရေးတဲ့ method တွေမှာ Exception ပစ်မယ်ဆိုရင် Checked နဲ့ Unchecked Exception ဘယ်ဟာပိုကောင်းလဲပေါ့။ Checked Exception ပစ်ရင် ခေါ်တဲ့သူက try-catch နဲ့မဖြစ်မနေဖမ်းကိုဖမ်းရတယ်။ ဥပမာ SQLException ပေါ့။ Unchecked Exception ပစ်ရင် ခေါ်တဲ့သူက မဖမ်းချင်လည်းရတယ်။ ဥပမာ NullPointerException ပေါ့။ အရင်တုန်းကတော့ ယူဆကြတယ် Checked Exception သုံးရင် ခေါ်တဲ့သူတိုင်း Error ကိုဖမ်းရတဲ့အတွက် ပိုကောင်းတယ်ပေါ့နော်။ Exception ဆိုတာနဲ့ မစဉ်းစားကြတော့ဘူး Checked ဆိုမှ Checked ပဲ။ ခေါ်သုံးတဲ့ကုဒ်တွေမှာလဲ try-catch တွေပလူပျံနေတာပဲ။ ဖမ်းပြီးဘာလုပ်ရမှန်းမသိလဲ log ရိုက်ပြီး ပြန်ပစ်ပေးလိုက်တာပဲ။ Checked Exception ကတစ်ကယ်ရော မဖြစ်မနေလိုအပ်လို့လား ပြန်စဉ်းစားကြည့်တော့ C#, Python, Ruby တို့မှာ Checked Exception ဆိုတာရှိတောင်မရှိဘူး။ သူတို့မှာ အဲဒါမသုံးပဲ ရေးတာအဆင်ပြေနေကြတာပဲလေ။ ကိုရေးနေတဲ့ method တစ်ခုမှာ Exception တက်ပြီဆိုရင် အဲဒိဟာကိုဖြေရှင်းပြီးဆက်အလုပ်လုပ်နိုင်တယ်ဆိုမှ ဖမ်းသင့်တယ်။ ဆိုပါစို့ SQLException တက်တယ်။ Database မှာဖြစ်တဲ့ဟာ ကိုကဘယ်လိုဖြေရှင်းလို့ရမှာလဲ။ နောက်ဆုံး UI ရေးတဲ့ကုဒ်ကပဲ Error ဖြစ်ကြောင်းပြပေးတာမျိုးလုပ်နိုင်မယ်။ ဘာမှလုပ်ပေးလို့မရပေမဲ့ Checked Exception ဖြစ်နေတော့ မဖမ်းလို့လဲမရ။ ကို့ method ရဲ့ throws နေရာမှာထည့်ရေးလိုက်ဖို့ကြတော့လဲ method signature ကိုမထိချင်။ တစ်ချို့အရေးကြီးတဲ့နေရာတွေမှာ Checked Exception သုံးသင့်တာတွေတော့ရှိပါတယ်။ နေရာတော်တော်များများမှာတော့ Unchecked Exception သုံးလဲရနိုင်ပါတယ်။ SpringFramework ရဲ့ Database နဲ့ပတ်သတ်တဲ့ method တွေမှာ DataAccesException ဆိုတဲ့ Unchecked Exception ကိုပဲပစ်တယ်။ ဒါပေမဲ့ သူတို့ရဲ့ method signature မှာတော့ အဲဒိဟာကို မရေးလဲရပေမဲ့ သက်သက်ကို ထည့်ရေးပေးတယ်။ ခေါ်သုံးတဲ့သူကို အသိပေးချင်တဲ့သဘောပေါ့။

ဒါက Checked Exception သုံးထားလို့ try-catch တွေနဲ့ရေးရတာမျိုးပါ
```java
public void saveEmployee(Employee employee) {
    try {
        Connection dbConnection = DBUtil.openConnection();
        EmployeeDAO dao = new EmployeeDAO(dbConnection);
        dao.insert(employee);
    } catch(DatabaseException e) {
        e.printStacktrace();
        throw e;
    } catch(DAOException e) {
        e.printStacktrace();
        throw e;
    }
}
```
ဒါက Unchecked Exception သုံးထားလို့ ကုဒ်တော်တော်နည်းသွားတာ
```java
public void insertRecord() {
    Connection dbConnection = DBUtil.openConnection();
    EmployeeDAO dao = new EmployeeDAO(dbConnection);
    dao.insert(employee);
}
```

## Exception ကောင်းကောင်းပစ်ပါ
Exception ပစ်တော့မယ်ဆိုရင် စဉ်းစားပါ။ Application သုံးနေရင်း Exception တက်ပြီဆိုရင် ကုဒ်ကိုပြန်ကြည့်စရာမလိုပဲ ဘာကြောင့်ဖြစ်လဲပြောနိုင်အောင်လုပ်ပါ။ SqlException တက်လာပြီး ဘာမှမပြောရင် Application သုံးနေတဲ့သူကဘာလုပ်ရမှန်းမသိတော့ဘူး။ လွန်ခဲ့တဲ့နှစ်လလောက်ကတည်းကသုံးနေတဲ့ Application ဆိုတော့ အခုလက်ရှိကုဒ်နဲ့လဲတူချင်မှတူတော့မယ်။ ကုဒ်အဟောင်းတွေပြန်ရှာ ကုဒ်တွေပြန်ဖတ်ပြီးအဖြေရှာရဖြစ်ကုန်ရော။ အဲတော့ Exception ပစ်ရင် အကြောင်းပြချက်သေသေချာချာရေးပေးလိုက်။ Root Exception ရှိရင်လဲထဲ့ပေးလိုက်။ အလုပ်ပိုပေမဲ့ ကိုရေးရမှာကတစ်ကြိမ်ထဲ။ Application ကသုံးနေသ၍ဒီ Exception ကတက်မှာ။
```java
public void connectDatabase(String jdbcUrl) {
    try {
        // trying to connect to database by given jdbcUrl
    } catch(SqlException sqlEx) {
        throw new DatabaseException(String.format("DBUtil.connectDatabase() has failed to connect to database by URL: %s", jdbcUrl), sqlEx);
    }
}
```

## ခေါ်တဲ့သူအတွက်အဆင်ပြေမဲ့ Exception တွေရေးပါ
ကိုရေးနေတဲ့ method တစ်ခုကနေ Exception ပစ်ရတော့မယ်ဆိုရင် စဉ်းစားစရာတွေရှိလာပြီ။ Exception class အသစ်ကို ဘယ်လိုနံမည်ပေးသင့်လဲဆိုရင် ခေါ်သုံးမဲ့သူဘက်ကတွေးကြည့်လိုက်။ EmployeeDAO object ဆီက findByName() ကိုခေါ်သုံးမဲ့သူအတွက် DataAccessException ဖမ်းရမယ်ဆိုရင် လုံလောက်ပြီ။ SqlException တို့ MongoException တို့ဖမ်းရမယ်ဆိုရင်တော့ မဟုတ်သေးဘူး။ ခေါ်တဲ့သူအတွက် ဘယ်လို Database အမျိုးအစားက error တက်လဲဆိုတာ အသုံးမှမဝင်တာ။ SQL သုံးနေတုန်းက SqlException ဖမ်းခိုင်းပြီး MongoDB ပြောင်းသုံးလို့ MongoException ပြောင်းဖမ်းကြဟေ့လို့ အားလုံးကိုလိုက်ပြင်ခိုင်းရမှာလား။ နောက်တစ်ခုက ကုဒ်က Exception သုံးမျိုးလောက်တက်နေရင် အားလုံးကို ကို့ method မှာပဲဖမ်းပြီး ခေါ်တဲ့သူအတွက်အဆင်ပြေမဲ့ Exception တစ်မျိုးပြောင်းပြီးပေးတာပိုကောင်းတယ်။ ဘယ်အချိန်မှာ မတူတဲ့ Exception ပစ်ပေးသင့်လဲဆိုရင် ခေါ်တဲ့သူက တစ်မျိုးစီအတွက် သူရဲ့အလုပ်လုပ်ပုံမတူနိုင်ဘူးဆိုရင်ပေါ့။ အဲဒါအတွက် အောက်ကကုဒ်ကိုကြည့်ပြီး ဆက်စပ်တွေးလို့ရနိုင်ပါတယ်။
```java
public void connectDatabase() {
    String jdbcUrl = "";
    try {
        // If fail to read property here, will throw IOException 
        jdbcUrl = PropertiesUtil.getProperty(Constants.Database.JDBC_URL);
        // If ThirdParty library fail, will throw multiple Exceptions
        ThirdPartyDriver databaseDriver = ThirdPartyDriver.getInstance(jdbcUrl);
        // For the caller, one exception is enough to know there is failure while connecting database
    } catch(IOException ioEx) {
        throw new DatabaseException("DBUtil.connectDatabase() was unable to get property for JDBC_URL", ioEx);
    } catch(SqlException sqlEx) {
        throw new DatabaseException(String.format("DBUtil.connectDatabase() has failed to connect to database by URL: %s", jdbcUrl), sqlEx);
    } catch(ThirdPartyDriverException driverEx) {
        throw new DatabaseException(String.format("DBUtil.connectDatabase() has failed to connect to database by URL: %s", jdbcUrl), driverEx);
    }
} 
```

## Null နဲ့ NullPointerException
Java နဲ.ရေးပြီဆိုရင် ကိုသုံးတဲ့ Object တွေ Null မဖြစ်အောင်တော်တော်သတိထားပြီးရေးရပါတယ်။ မဟုတ်ရင် NullPointerException တအားတက်လို့ပါ။ ကုဒ်တွေမှာ Null ဟုတ်မဟုတ်စစ်ရတဲ့ဟာတွေနဲ့ ပြည့်နေတတ်ပါတယ်။ အဲတာတွေပါတော့ဘာဖြစ်လဲကွာဆိုရင်တော့ ဒီလိုရှိပါတယ်။ ကုဒ်ဆိုတာနည်းလေကောင်းလေပါ။ တစ်ကယ်အလုပ်လုပ်မဲ့ကုဒ်ကဆယ်ကြောင်း Null မဖြစ်အောင်စစ်၇တဲ့ဟာတွေနဲ့ပေါင်းတော့အကြောင်းနှစ်ဆယ်ဆိုရင် လွဲနေပါပြီ။ အဲဒီကိုပြေလည်အောင်လုပ်လို့ရတဲ့နည်းလမ်းတွေရှိပါတယ်။

## Null ပြန်မပေးနဲ့
ကိုရေးတဲ့ method(or)function ကနေ Null ကို return ပြန်မပေးလိုက်နဲ့။ Null ပြန်ပေးလိုက်တာနဲ့ ကို့ကုဒ်ကိုခေါ်သုံးတဲ့နေရာတိုင်းမှာ Null ဟုတ်မဟုတ်စစ်ရတော့မယ်။ မစစ်တဲ့နေရာတိုင်းမှာ NullPointerException တတ်နိုင်ပြီ။ အဲဒါ Bug ပါ။ ဘာလုပ်သင့်လဲဆိုရင် Empty Value တွေပြန်လို့ရတယ်။ Array ပြန်ပေးရမဲ့နေရာမှာ ဘာ Data မှမရှိလို့ Null ပြန်မဲ့အစား Empty Array ပြန်လို့ရတယ်။ String ဆိုရင် Null မပြန်ပဲ Empty String ဖြစ်စေ Data မရှိဘူးဆိုတာကိုပြတဲ့ “UNKNOWN”, “INVALID”, “NA” လိုမျိုးအသေသတ်မှတ်ပြီးသုံး။ List တို့ Map တို့လိုမျိုး Collection တွေဆိုရင် Empty List တွေ Empty Map တွေပြန်လိုက်။ ဒါဆိုရင် Empty တန်ဘိုးပြလို့မရတဲ့ User တို့ Employee တို့လို Object တွေကြဘယ်လိုလုပ်မလဲ။ နည်းလမ်းရှိပါတယ်။ JDK8 မှာစပါလာတဲ့ Optional ကိုသုံး။ JDK8 မတိုင်ခင်ကတော့ Google ကထုတ်တဲ့ Guava library မှာ Optional ပါတယ်။ နောက်တစ်နည်းက Special Case Pattern လို့ခေါ်တဲ့နည်း။ ထားပါတော့ Category ဆိုတဲ့ Object နေရာမှာ Null အစား သီးသန့်ရေးထားတဲ့ UnknownCategory လိုမျိုး Object ပြန်ပေးလိုက်ရင် ခေါ်သုံးတဲ့နေရာမှာ Null လဲစစ်စရာမလို NullPointerException လဲမတက်နိုင်တော့ဘူး။
```java
public class UnknownCategory extend Category {
    private static final String UNKNOWN_CATEGORY = "UNKNOWN_CATEGORY";
 
    public String getName() {
        return UNKNOWN_CATEGORY;
    }
}
```

## Null ထည့်မပေးနဲ့
ကိုရေးတဲ့ကုဒ်ကတစ်ခြား method ကိုခေါ်သုံးရင် parameter ပေးတဲ့နေရာမှာ Null မပေးလိုက်နဲ့။ အဲဒိ method ကသူရတဲ့ parameter ကိုတန်ဘိုးရှိတယ်ပဲယူဆပြီးသုံးမှာပဲ။ တွေးကြည့်ရင် သုံးတဲ့သူက သူခေါ်တဲ့ method ကတောင်းတဲ့ parameter ကိုမပေးနိုင်ပဲဘာလို့သုံးနေသေးလဲ။

## References
- https://unsplash.com/photos/I8OhOu-wLO4
- Clean Code by Uncle Bob
