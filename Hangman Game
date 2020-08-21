import time
import random
def intro() :
    print("It is adviced to play with uppercase characters.")
    time.sleep(2)
    print("Just remember, if you are ever stuck and need help, hit the 'h'(not 'H') button.\n")
    print("Best of luck for the game !!")
    time.sleep(2)
    pr("Let's begin the game...")
    print("\n")
    time.sleep(3)

def lev() :
    lev=input("Enter the level, you want to play (Easy/Medium/Hard) : ")
    print("You want to play {} level.".format(lev))
    time.sleep(2)
    
    easy_words=["JUICY", "FUNNY", "FILM", "QUIZ", "LUCKY"]
    easy_hint=["We all love to eat _ _ _ _ _ apples.", "It struck her _ _ _ _ _ and she giggled.", "He made his _ _ _ _ debut in 1992.", "The sports trivia _ _ _ _ isn't all that bad.", "She got _ _ _ _ _, and won jackpot."]
    
    medium_words=["PUZZLE", "ZOMBIE", "YUMMY", "YIPPEE"]
    medium_hint=["The pieces of the _ _ _ _ _ simply didn't fit together", "a corpse said to be revived by witchcraft, especially in certain African and Caribbean religions.", "These gummy bears are so _ _ _ _ _.", "Expressing wild excitement or delight."]
    
    hard_words=["KNOWLEDGE", "MICROWAVE", "UNKNOWN", "BOOKWORM", "WITCHCRAFT", "TRANSPLANT"]
    hard_hint=["I acquired more _ _ _ _ _ _ _ _ _ on the subject.", "These are immense artificial excavations of _ _ _ _ _ _ _ date.", "A _ _ _ _ _ _ _ _ is a person who enjoys reading.", "Witch A person, normally a woman who practices _ _ _ _ _ _ _ _ _ _.","Cornea _ _ _ _ _ _ _ _ _ _ was carried out in March 2001."]
    
    if lev.lower()=="easy" :
        intro()
        game(easy_hint, easy_words,6)
    elif lev.lower()=="medium" :
        intro()
        game(medium_hint, medium_words, 7)
    elif lev.lower()=="hard" :
        intro()
        game(hard_hint, hard_words, 9)
    else :
        print("You entered an invalid input !")
        br()
        again()
        
def again() :
    ask=input("Do you want to play again (y/n) ?")
    time.sleep(1)
    if ask.lower()=="y" or ask.lower()=="yes" :
        br()
        lev()
    else :
        print("Have a good day !")
        br()
    
def br() :
    print("_"*25, "\n")
    
def pr(str1="") :
    print(" "10, ""8, str1, ""*8)
    time.sleep(2)

def game(hint_list, word_list, c=8) :
    words_list=["JUICY", "WAVE", "QUIZ", "LUCKY", "JUMBO"]
    index=random.randint(0,len(words_list)-1)
    chance=c
    print("You can try {} times.".format(chance))
    word=(word_list[index])
    guesses=""
    wrong=[]
    l=len(word)
    #print(word)

    while chance>0 :
        cnt=0
        for char in word :
            if char in guesses :
                print(char)
            else :
                print("_")
                cnt+=1
        time.sleep(2)
        if cnt==0 :
            print("You won, smartie !!")
            print("The word is : ", word)
            br()
            time.sleep(3)
            break
        if c==9 :
            if chance==8 :
                print("         \n"
                    "         \n"
                    "         \n"
                    "         \n"
                    "         \n"
                    "         \n"
                    "  |      \n"
                    "_|_\n")
        if c==9 :
            if chance==7 :
                print("         \n"
                    "         \n"
                    "         \n"
                    "         \n"
                    "         \n"
                    "  |      \n"
                    "  |      \n"
                    "_|_\n")
        if c==7 :
            if chance==6 :
                print("         \n"
                    "         \n"
                    "         \n"
                    "         \n"
                    "  |      \n"
                    "  |      \n"
                    "  |      \n"
                    "_|_\n")    
            
        if chance==5 :
            print("         \n"
                  "         \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "_|_\n")

        if chance==4 :
            print("          \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "_|_\n")

        if chance==3 :
            print("   ___\n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "_|_\n")

        if chance==2 :
            print("   ___\n"
                  "  |     | \n"
                  "  |     |\n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "  |      \n"
                  "_|_\n")

        if chance==1 :
            print("   ___\n"
                  "  |     | \n"
                  "  |     | \n"
                  "  |     |\n"
                  "  |     o\n"
                  "  |      \n"
                  "  |      \n"
                  "_|_\n")

        guess=input("\nGuess the character :")
        if len(guess)==1 :
            guesses+=guess.upper() + " "
            if guess.upper() not in word :
                if guess=="h":
                    ask_h=input("Do you need help ?(y/n)")
                    if ask_h.lower()=="y" or ask_h.lower()=="yes":
                        print("This is your hint...")
                        time.sleep(2)
                        print(hint_list[index])
                        chance+=1
                    else :
                        print("Use Uppercase, 'H'")
                        time.sleep(2)
                else :
                    chance-=1
                    print("Wrong guess.")
                    time.sleep(2)
                    br()
                    print("You have {} more guesses.".format(chance)) 
                    time.sleep(2)
                    
            if chance==0 :
                print("   ___\n"
                      "  |     | \n"
                      "  |     | \n"
                      "  |     | \n"
                      "  |     o \n"
                      "  |    /|\ \n"
                      "  |    / \ \n"
                      "_|_ \n")
                print("You lose !")
                    
            print("Already guessed characters : ", guesses.replace("H",""))
        else :
            print("One character at a time !!")
            time.sleep(2)
    again()
    
pr("WELCOME TO HANGMAN GAME")
name=input("Enter your name: ")
print("Hello {} !!".format(name))
time.sleep(1)
lev()
