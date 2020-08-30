# datetime
import datetime
def days_in_month(year,month):
     return (datetime.date(year, month + 1, 1) - datetime.date(year, month, 1)).days
print(days_in_month(2020,8))
def is_valid_days(year,month,day):
    if(year>datetime.MINYEAR and year<datetime.MAXYEAR):
        if(month>=1 and month<=12):
            if(day>=1 and day<=days_in_month(year,month)):
                return("valid days")
    else:
        return("not valid")
print(is_valid_days(2020,8,31))
def days_between(year1, month1, day1, year2, month2, day2):
    day=(datetime.date(year1,month1,day1)-datetime.date(year2,month2,day2)).days
    if not(is_valid_days(year1,month1,day1)and is_valid_days(year2,month2,day2)):
        return 0
    day=(datetime.date(year1,month1,day1)-datetime.date(year2,month2,day2)).days
    if day<0:
            return -(day)
print(days_between(2017, 1, 1, 2017, 11, 1))
def age_in_days(year,month,day):
    if(is_valid_days(year,month,day)):
        return (datetime.date.today()-datetime.date(year,month,day)).days
    else:
        return 0
print(age_in_days(1999, 7, 29))


    
