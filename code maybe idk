import random

def card_values():
    cards = list(range(2,15))
    faces = ["jack", "queen", "king", "ace"]
    card1 = random.choice(cards)
    card2 = random.choice(cards)
    
    if card1 >= 11:
        facecard = random.choice(faces)
        if facecard == "ace":
            ace_choice = int(input("you got an ace, do you want it to equal 1 or 11?: "))
            card1 = ace_choice            
        else:
            card1 = 10
        print("card 1: ", facecard)
    else:
        print("card 1: ", card1)

    if card2 >= 11:
        facecard2 = random.choice(faces)
        if facecard2 == "ace":
            ace_choice2 = int(input("you got an ace, do you want it to equal 1 or 11?: "))
            card2 = ace_choice2
        else:
            card2 = 10
        print("card 2: ", facecard2)
    else:
        print("card 2: ", card2)

    return card1, card2, cards

def hit_stand(card1, card2, cards):
    total = card1 + card2
    print("your total is: ", total)
    while True:
        if total <= 21:
            hit_input = input("would you like to hit or stand: ")
            if hit_input == "hit":
                card3 = random.choice(cards)
                if card3 >= 11:
                    facecard = random.choice(["jack", "queen", "king", "ace"])
                    if facecard == "ace":
                        ace_choice = int(input("You got an ace, do you want it to equal 1 or 11?: "))
                        card3 = ace_choice            
                    else:
                        card3 = 10
                    print("you got a ", facecard)
                else:
                    print("you got a ", card3)
                total += card3
                print("your total is: ", total)
            elif hit_input == "stand":
                print("you stood with a total of ", total)
                break
            else:
                print("wrong answer idiot")
        else:
            print("you busted")
            bustcount = 1
            break
def dealer(cards, total, bustcount):
    dealer_card1 = random.choice(cards)
    dealer_card2 = random.choice(cards)
    dtotal = dealer_card1 + dealer_card2
    if bustcount != 1:       
        if dealer_card1 >= 11:
            facecard = random.choice(["jack", "queen", "king", "ace"])
            if facecard == "ace":
                if total > 10:
                    dealer_card1 = 1
                else:
                    dealer_card1 = 11
            else:
                dealer_card1 = 10     

        if dealer_card2 >= 11:
            facecard2 = random.choice(["jack", "queen", "king", "ace"])
            if facecard2 == "ace":
                if total > 10:
                    dealer_card2 = 1
                else:
                    dealer_card2 = 11
            else:
                dealer_card2 = 10    

        if dtotal >= 21:
            print(dtotal, "dealer busted, you win")
        else: 
            if dtotal >= total:
                print("dealer has more, you lose")
                
        if dtotal <=16:
            print("dealer has decided to hit")
            dealer_card3 = random.choice(cards)
            dtotal = dtotal + dealer_card3
            print(dtotal)
            if dtotal >= 21:
                print("dealer busted, you win")
            else:
                if dtotal >= total:
                    print("dealer has more, you lose")
                else: 
                    dtotal = dtotal + dealer_card3
    
    
    
    else:
        print("you lose")
card1, card2, cards, = card_values()
total = card1 + card2
hit_stand(card1, card2, cards)
dealer(cards, total)