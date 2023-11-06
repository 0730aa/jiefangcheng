# 导入 math 模块，用于计算平方根
import math

# 定义一个函数，接受三个参数 a, b, c，分别代表一元二次方程的系数
def solve_quadratic(a, b, c):
    # 计算判别式
    delta = b**2 - 4*a*c
    # 如果判别式小于零，说明方程无实数解
    if delta < 0:
        print("方程无实数解")
    # 如果判别式等于零，说明方程有一个重根
    elif delta == 0:
        # 计算重根的值
        x = -b / (2*a)
        # 输出结果
        print(f"方程有一个重根，x = {x}")
    # 如果判别式大于零，说明方程有两个不同的实数根
    else:
        # 计算两个根的值
        x1 = (-b + math.sqrt(delta)) / (2*a)
        x2 = (-b - math.sqrt(delta)) / (2*a)
        # 输出结果
        print(f"方程有两个不同的实数根，x1 = {x1}, x2 = {x2}")

# 测试函数
solve_quadratic(1, -5, 6) # 输出方程有两个不同的实数根，x1 = 3.0, x2 = 2.0
solve_quadratic(1, -4, 4) # 输出方程有一个重根，x = 2.0
solve_quadratic(1, 2, 3) # 输出方程无实数解
