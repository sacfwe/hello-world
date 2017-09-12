import random
print "esc退出"
ops = ['+', '-', '*', '/']
ans = ""
i = 1
while ans != "esc":
    add1 = random.randint(1, 10)
    add2 = random.randint(1, 10)
    op = random.randint(0, 3)
    eq = str(add1) + ops[op] + str(add2)
    val = eval(eq)
    print "Q%d: %s=" % (i, eq)
    ans = raw_input("A: ")
    if ans == 'esc':
        break
    elif val == int(ans):
        print "right!"
    else:
        print "error. the right answer is %d" % val
    i += 1
    print
