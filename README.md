# freight-value-sender
This app sends to VTEX the list of the freight prices generated by https://planilha.xpagencia.com.br . 
The sheet has the headers: ZipCodeStart, ZipCodeEnd, PolygonName, WeightStart, WeightEnd, AbsoluteMoneyCost, PricePercent, PriceByExtraWeight, MaxVolume, TimeCost, Country, MinimumValueInsurance
Ps. : There is an example here: example_sheet.xls

This app can also make some changes to adapt the prices to the company's reality (instructions will appear when you execute the app).

Here some directions:
Create a file config.py and inside set the variables:
x_vtex_api_appkey = "Your appkey here"
x_vtex_api_apptoken = "Your apptoken here"
You will need a shipping policy created on your VTEX admin to send the prices using the ID of the shipping policy (the app will ask)

Some extras:
You can create an .exe for this program. Just do "pyinstaller --onefile adjust_table.py" in your terminal
You can use "black adjust_table.py" in your terminal to automatically adjust the code