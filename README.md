# curency_local
helper
=========
extension String{
     func toCurrencyFormat() -> String {
        if let intValue = Int(self){
           let numberFormatter = NumberFormatter()
           numberFormatter.locale = Locale(identifier: "ig_NG")/* Using Nigeria's Naira here or you can use Locale.current to get current locale, please change to your locale, link below to get all locale identifier.*/ 
           numberFormatter.numberStyle = NumberFormatter.Style.currency
           return numberFormatter.string(from: NSNumber(value: intValue)) ?? ""
      }
    return ""
  }
}

IOS local identifier:
https://gist.github.com/jacobbubu/1836273
