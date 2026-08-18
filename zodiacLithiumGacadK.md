#This function checks if the year is greater than 1900
def get_year(userYear):
    if userYear < 1900:
        return None
    else:
        zodiacNo = (userYear - 1900) % 12 #I used %12 because a zodiac sign will repeat every 12 years
        return zodiacNo 

#From the zodiac number, this function returns the corresponding zodiac sign
def get_zodiac(zodiacNo):
    if zodiacNo == 0:
        return "Rat (鼠 / Shǔ)"
    elif zodiacNo == 1:
        return "Ox (牛 / Niú)"
    elif zodiacNo == 2:
        return "Tiger (虎 / Hǔ)"
    elif zodiacNo == 3:
        return "Rabbit (兔 / Tù)"
    elif zodiacNo == 4:
        return "Dragon (龙 / Lóng)"
    elif zodiacNo == 5:
        return "Snake (蛇 / Shé)"
    elif zodiacNo == 6:
        return "Horse (马 / Mǎ)"
    elif zodiacNo == 7:
        return "Goat (羊 / Yáng)"
    elif zodiacNo == 8:
        return "Monkey (猴 / Hóu)"
    elif zodiacNo == 9:
        return "Rooster (鸡 / Jī)"
    elif zodiacNo == 10:
        return "Dog (狗 / Gǒu)"
    else:
        return "Pig (猪 / Zhū)"

#Asks the user to input their birth year
userYear = int(input("Enter your birth year: "))

#Get the zodiac number
zodiacNo = get_year(userYear)


if zodiacNo == None:
    print("Invalid year. Please enter a year greater than or equal to 1900.")
else:
    print("Your Chinese Zodiac sign is:", get_zodiac(zodiacNo)) #Shows the user their zodiac sign

    