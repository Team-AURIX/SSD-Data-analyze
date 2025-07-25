import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D
import numpy as np
import os
import json

graph_x = np.arange(70)
graph_y = np.arange(55)
graph_x, graph_y = np.meshgrid(graph_x, graph_y)
graph_x = graph_x.flatten()
graph_y = graph_y.flatten()
graph_z = np.zeros_like(graph_x)
dx = dy = 1
lwir_min_dz = np.zeros((70, 55), dtype = int)
lwir_max_dz = np.zeros((70, 55), dtype = int)
visible_min_dz = np.zeros((70, 55), dtype = int)
visible_max_dz = np.zeros((70, 55), dtype = int)


# 3D 플롯 생성
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# 막대 그래프 그리기

with open('predict_center.json', 'r') as k:
        gt_json = json.load(k)

# one = np.array(gt_json[0][0:640])
# two = np.array(gt_json[0][641:1280])
# three = np.array(gt_json[0][1281:1940])
# four= np.array(gt_json[0][1941:2580])
# five = np.array(gt_json[0][2581:3220])
# six = np.array(gt_json[0][3221:])

dz = np.array(gt_json[4])

ax.plot_trisurf(graph_x, graph_y, dz, cmap="inferno")


# ax.bar3d(graph_x[0:640], graph_y[0:640], graph_z[0:640], dx, dy, one, color='red')
# ax.bar3d(graph_x[641:1280], graph_y[641:1280], graph_z[641:1280], dx, dy, two, color='orange')
# ax.bar3d(graph_x[1281:1940], graph_y[1281:1940], graph_z[1281:1940], dx, dy, three, color='yellow')
# ax.bar3d(graph_x[1941:2580], graph_y[1941:2580], graph_z[1941:2580], dx, dy, four, color='lime')
# ax.bar3d(graph_x[2581:3220], graph_y[2581:3220], graph_z[2581:3220], dx, dy, five, color='skyblue')
# ax.bar3d(graph_x[3221:], graph_y[3221:], graph_z[3221:], dx, dy, six, color='purple')
ax.set_title("3D Bar Chart")
ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_zlabel('Count')

plt.show()
