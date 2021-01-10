#!/usr/bin/env python
# test = './secure_house tan key'

# res = test.split(" ")
# def main():
import sys

# from pip._vendor.distlib.compat import raw_input
i = -1
j = 0
k = 0
cho = 0
enter = 0
owner = []
ownerKey = []
member = [""]
memberKey = [""]
house = [" "]
turnkey = []
text = []
# try:
ten = str(sys.argv[1])
dai = len(sys.argv)
for x in range(2, dai):
    key = str(sys.argv[x])
    ownerKey.append(key)
seKey = "FIREFIGHTER_SECRET_KEY"
ownerKey.append(seKey)
owner.append(ten)

# print(dai)
# print(ownerKey)
# print(key)
# print("owner :" + owner[0] + " owner's key: " + ownerKey[0])

lai = 1

while lai != 0:
    try:
        text = raw_input("")
    except EOFError:
        break
    # text = raw_input("")
    textSplit = text.split(" ")

    # print(textSplit)
    # print(len(text))
    # print(len(textSplit))
    if textSplit[0] == "INSERT" and textSplit[1] == "KEY":
        member.append(textSplit[2])
        memberKey.append(textSplit[3])

        # print(member)
        # print(memberKey)
        # text.clear()
        print("KEY " + textSplit[3] + " INSERTED BY " + textSplit[2])
    elif textSplit[0] == "TURN" and textSplit[1] == "KEY":
        check = textSplit[2]

        # print(check)
        i = -1
        for check in member:

            i = i + 1
            # print(i)

            if check == textSplit[2]:
                # print(check)
                j = i
            elif check != textSplit[2]:
                # print(check)
                k = i
            # print(i)
            # print(j)
            # print(k)
            # for i, check in enumerate(member):
            # print(i, check)
            # if check in member:
            # print("hit")

        if memberKey[j] in ownerKey:
            # if checkKey == True:
            print("SUCCESS " + member[j] + " TURNS KEY " + memberKey[j])
            # house.append(member[j])
            turnkey.append(member[j])
            # print("house check ?")
            # print(house)
            i = -1
            j = i
        elif (textSplit[2] == seKey):
            print("SUCCESS Firefighters" + " TURNS KEY " + seKey)
            fire = "Firefighters"
            house.append(fire)
        else:
            print("FAILURE " + member[j] + " UNABLE TO TURN KEY " + memberKey[j])
            # print(k)
            # print(member)
            i = -1
            j = i
            k = i
            # print("problem")
            # print(k)
    elif textSplit[0] == "ENTER" and textSplit[1] == "HOUSE":
        checkHouse = textSplit[2]
        #print("checkHouse" + checkHouse)
        check1 = textSplit[2]
        check2 = check1 in turnkey
        #print(check2)
        maxL = len(turnkey)

        if check2 is False:
            enter = 1
        elif check2 is True:
            for k in range(0, maxL):
                if checkHouse == turnkey[k]:
                    j = k
                    enter = 2


        # print(enter)
        i = -1

        if enter == 2:
            print("ACCESS ALLOWED")
            house.append(textSplit[2])
            del turnkey[j]
        elif enter == 1:
            print("ACCESS DENIED")


    elif textSplit[0] == "WHO'S" and textSplit[1] == "INSIDE?":
        checkIn = len(house)
        text2 = []

        D = len(house)

        for g in range(1, D):
            text = str(house[g])
            text2.append(text)

        if checkIn == 1:
            print("NOBODY HOME")
        else:

            print(','.join(map(str, text2)))
    elif textSplit[0] == "CHANGE" and textSplit[1] == "LOCKS":

        if textSplit[2] != owner[0]:
            print("ACCESS DENIED")
        elif textSplit[2] == owner[0] and owner[0] in house:
            # print("here")
            # ownerKey.clear(ownerKey)
            del ownerKey[:]
            del turnkey[:]
            keylen = len(textSplit)

            for m in range(3, keylen):
                # print(m)
                tex = str(textSplit[m])
                # print(tex)
                ownerKey.append(tex)
                # print(ownerKey)
            print("OK")
            ownerKey.append(seKey)
            del turnkey[:]
        else:
            print("ACCESS DENIED")
            # print(ownerKey)
    elif textSplit[0] == "LEAVE" and textSplit[1] == "HOUSE":

        tef = textSplit[2]
        # print(tef)
        i = 0

        moi = tef in house
        # print(moi)
        if moi is True:
            for tef in house:

                # print(i)
                # print("check")
                if tef == textSplit[2]:
                    cho = i
                # print(cho)
                i = i + 1

            # print(house)
            # print(cho)
            # print(house[cho])
            del house[cho]
            #del turnkey[cho]
            i = -1

            print("OK")
        else:
            print(textSplit[2] + " NOT HERE")
    elif textSplit[0] == "DATA":

        print("OWNER ", owner)
        print("OWNER 'S KEY", ownerKey)
        print("PEOPLE IN HOUSE ", house)
        print("PEOPLE TURN KEY ", turnkey)
        print("PEOPLE INSERT KEY ", member)
        print("MEMBER KEY ", memberKey)







    elif text == "":
        lai = 0
    else:
        print("ERROR")

# main()