import math
class Vector:  #定义二维向量类
    def __init__(self,x=3,y=4):
        self.x=x
        self.y=y
        self.vector_len=math.sqrt(x**2+y**2) #向量长度为类的属性
    def __repr__(self):
        return 'Vector(%r,%r)' % (self.x,self.y)
    def add(self, other):  #加
        x=self.x+other.x
        y=self.y+other.y
        return Vector(x,y)
    def minus(self,others):  #减
        x=self.x-others.x
        y=self.y-others.y
        return Vector(x,y)
    def multply(self,a):  #与标量乘法
        x = self.x*a
        y = self.y*a
        return Vector(x,y)
    def divide(self,a):   #与标量除法
        x = self.x/a
        y = self.y/a
        return Vector(x,y)

if __name__ == '__main__':
    cal=Vector() #实例化
    others=Vector(0,1)
    a=2
    print('the length of vector is',cal.vector_len)
    y1=cal.add(others)
    y2=cal.minus(others)
    y3=cal.multply(a)
    y4=cal.divide(a)
    print('[3,4]+[0,1]=',y1)
    print('[3,4]-[0,1]=',y2)
    print('[3,4]*2=',y3)
    print('[3,4]/2=',y4)

