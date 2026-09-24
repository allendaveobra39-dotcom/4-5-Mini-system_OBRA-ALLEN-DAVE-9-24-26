# SECTION 4: GENERAL-PURPOSE MATH FUNCTIONS
        def general_menu():
            print_header("GENERAL-PURPOSE MATH FUNCTIONS")
            print("""
            1. Compute ceil, floor, and trunc of a value
            2. Compute a factorial
            3. Compute the hypotenuse of a right triangle
            0. Back to Main Menu
            """)
            choice = safe_input("Enter your chioce: ").strip()
        
            if choice == "1":
            x = get_float("Enter a decimal number x: ")
            print(f"\n ceil({x})  = {math.ceil(x)}")
            print(f"  floor({x}) = {math.floor(x)}")
            print(f"  trunc({x}) = {math.trunc(x)}")
        
            elif choice == "2":
            n = get_int(Enter a non-negative whole number: ")
            try:
                print(f"\ {n}! = {math.factorial(n)}")
                exceptValueError:
                print("  factorial() requires a non-negative integer.")
                elif choice == "3":
            x = get_float("Enter the length of leg x: ")
            y = get_float("Enter the length og leg y: ")
            print(f"\n hypot({x}, {y}) = [math.hypot(x,Y)}")
            print(f"  (same idea as sqrt({x}**2 + {y}**) = "
                    f"{math.sqrt(x**2 + y**2)}, but hypot()
                    is more precise.)")
        
        elif choice == "0":
            return
        else:
        print("\nInvalid choice .")
        pause()
        #SECTION 5: THE RANDOM MODULE 
        def random_menu():
            print_header("THE RANDOM MODULE")
            def random_menu():
                print_header("THE RANDOM MODULE")
                print("""
                
                1. Set a seed (so results can be repeated)
                2. Generate a number with randrange()
                3. Generate a number with randint()
                4. Pick a random item from a list with a choice()
                5. Drwa several UNIQUE items from a list with a sample() (like a lottery)
                0. BACK TO MAIN Menu
                """)
                choice = safe_input("Enter your choice: ").strip()
                
                if choice == "!":
                    pick = safe_input(Type " time to seed with current time, or type an "
                                    "integer to seed manually:
        ")>strip()
                if pick.lower() == "time":
                    random.seed()
                    print("\nSeed set using the current time. every run will now "
                    "differ."")
                else: 
                    try:
                        random.seed(int(pick))
                        print(f"\nSeed set to {int(pick)}. the random sequence "
                        f"produced from now on is 
            repeatable.")
                    except ValueError:
                        print("\nInvalid integer. seed not changed.")
                    elif choice =="2":
                        print("Choose a form: 1) randrange(end)  2) randrange(beg, end)"
                        " 3) randrange(beg, end, step)")
                        form = safe_input("Form (1/2/3): ").strip()
                        if form =="1":
                            end = get_int(Enter end: ")
                            print(f"\nrandom.randrange([end}) ={random.randrange(end)}")
                        elif form == "2":
                            beg = get_int(Enter beg: ")
                            end = get_int("ENTER end: ")
                            print(f"\nrandom.randrange ({beg}, {end}) = "
                            
                            f"{random.randrange(beg, end)}")
                        elif form == "3":
                            beg = get_int("enter beg: ")
                            enf = get_int("enter end: "
                            step = get_int("enter steps: ")
                            print(f'\nrandom.randrange(beg{}, {end}, {step}0 = "
                            f"{random.randrange(beg, end, step)}")
                        else:
                            print("\nInvalid form.")
                            
                        elif choice == "3":
                            left = get_int("Enter the left (lowest): ")
                            right = get_int("Enter the right (highest bound: ")
                            try:
                                print("f\nrandom.randint({left, {right}) = "
                            except ValueError:
                                print("\nleft must be <= right.")

                            elif choice == "4":
                                raw = safe_input("Enter items seperated by commas (e.g.,
                                apple,banana,
                                "cherry): ")
                                items = [item.strip() for item in raw.split(",") if item.strip()]
                                if items:
                                    print(f"\nYour list: {items}")
                                    print(f"random.choice(list) picked: {random.choice(items)}")
                                else:
                                    print("\nYou didn"t enter any items>")

                                elif choice == "5":
                                    raw = safe input("Enter items seperated by commas (e.g.,
                                    1,2,3,4,5,6,7,"
                                                        "8,9,10 or names for a lottery): ")
                                          items = [item.strip() for item in raw.split(",") if item.strip()]
                                          if not items:
                                            print("\nYou didn't enter any items.")
                                          else:
                                            k = get_int(f"How many UNIQUE items to draw (1 to "f"{len(items)})")
                                            try:
                                                print(f"\nYour lsit: {items}")
                                                print(f"random.sample(list, {k}0 drew: "
                                                f"{random.sample(items, k)}")
                                            except exceptValueError:
                                                print(f"\nk must be between 1 and {len(items)} (the sample "
                                                f"cannot be larger than the population).")
                                            elif choice == "0":
                                                return
                                            else:
                                                print("\nInvalid choice.")

                                            pause()
                                                   

        
