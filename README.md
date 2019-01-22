page = 0
user_score = 0
elasped_time = 0


def setup():
    size(640, 480)


def draw():

    def pages():
        if page == 0:
            background(240, 128, 128)
            fill(123, 104, 238)
            rect(220, 20, 200, 100)
            fill(255, 255, 255)
            rect(220, 360, 200, 100)
            rect(10, 190, 200, 100)
            rect(430, 190, 200, 100)
        elif page == 1:
            background(240, 128, 128)
            fill(123, 104, 238)
            rect(220, 360, 200, 100)
            fill(255, 255, 255)
            rect(10, 190, 200, 100)
            rect(430, 190, 200, 100)
            rect(220, 20, 200, 100)
        elif page == 2:
            background(240, 128, 128)
            fill(123, 104, 238)
            rect(10, 190, 200, 100)
            fill(255, 255, 255)
            rect(220, 20, 200, 100)
            rect(220, 360, 200, 100)
            rect(430, 190, 200, 100)
        elif page == 3:
            background(240, 128, 128)
            fill(123, 104, 238)
            rect(430, 190, 200, 100)
            fill(255, 255, 255)
            rect(220, 20, 200, 100)
            rect(220, 360, 200, 100)
            rect(10, 190, 200, 100)
            rect(430, 190, 200, 100)

    def play(user_input, page):
        global user_score
        global elapsed_time

        valid = ["w", "a", "s", "d"]

        try:
            user_input = input()
        except:
            if user_input != valid:
                user_input = input()
        else:
            import random
            page = random.randint(0, 3)

    def tests():
        assert play("w", page=0) == user_input += 1
        assert play("a", page=2) == user_input += 1
        assert play("s", page=1) == user_input += 1
        assert play("d", page=3) == user_input += 1
        print("passed all tests")

    def main():
        background(255, 255, 255)
        textSize(20)
        fill(0)
        text("using WASD, click the position of the box that changes colour")
        if (page == 0 and user_input == "w") or
        (page == 1 and user_input == "s") or
        (page == 2 and user_input == "a") or
        (page == 3 and user_input == "d"):
            user_score += 1
        elif (page == 0 and user_input != "w") or
        (page == 1 and user_input != "s") or
        (page == 2 and user_input != "a") or
        (page == 3 and user_input != "d"):
                break
                text(user_score + elasped_time)
