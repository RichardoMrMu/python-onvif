# python-onvif
test code to control hikcamera using onvif 
# Requirement
1. python-onvif-zeep
2. opencv-python
```shell
pip install onvif_zeep
pip install opencv-python
```
# Introduction
The [move.py](https://github.com/RichardoMrMu/python-onvif/blob/main/move.py) can achieve move function like absolute move and relate move (including up,down,left and right four axises), meanwhile, it uses functional language. And the  [ptz_control.py](https://github.com/RichardoMrMu/python-onvif/blob/main/move.py) can achieve get configurations, move, goto presets, etc. It uses oop(Object Oriented Programming). You can chooses the style you like.
# Using
For [move.py](https://github.com/RichardoMrMu/python-onvif/blob/main/move.py), you need to change [this line](https://github.com/RichardoMrMu/python-onvif/blob/a4277a9957ec30a96ce359404948710d6cb9421d/move.py#L77) as your ip, passwd and username. Then you can run 
```shell
python move.py
```
and see camera move successfully if connecting. And for [ptz_control.py](https://github.com/RichardoMrMu/python-onvif/blob/main/move.py), your should replace [this line](https://github.com/RichardoMrMu/python-onvif/blob/a4277a9957ec30a96ce359404948710d6cb9421d/ptz_control.py#L11) 's ip, username, passwd ans port as yours, and you can write your own main function like this :
```python
if __name__ == '__main__':
    ptz = ptzControl()
    ptz.goto_preset()
    ptz.zoom_relative(0.5,0.4)
```
Then run like this :
```shell
pyhton ptz_control.py
```
enjoy it!
