# POO_Reto_3

1. Reactangle (I don't know what that pun means either).
   
   ```
   import math

    class Point:
        def __init__(self, x, y):
            self.x = x
            self.y = y
        def compute_distance(self, other: 'Point'):
            return ((self.x - other.x)**2 + (self.y - other.y)**2)**0.5
            
    class Line:
        def __init__(self, start: Point, end: Point):
            self.start = start
            self.end = end
        def compute_length(self):
            self.length = self.start.compute_distance(self.end)
            return self.length
        def compute_slope(self):
            # slope in degrees
            self.slope = math.atan((self.end.y - self.start.y) / (self.end.x - self.start.x))
            return self.slope
        def compute_horizontal_cross():
            pass
        def compute_vertical_cross():
            pass
    
    class Rectangle:
        def __init__(self, method: int, arg1, arg2, *arg3):
            self.method = method
            match self.method:
                case 1:
                    # arg1 is left corner Point, arg2 is width, arg3 is height
                    self.center: Point = Point(arg1-0.5*arg2, arg1-0.5*arg3)
                    self.width: float = arg2
                    self.height: float = arg3
                case 2:
                    # arg1 is center Point, arg2 is width, arg3 is height
                    self.center: Point = arg1
                    self.width: float = arg2
                    self.height: float = arg3
                case 3:
                    # arg1 is a Point, arg2 is another Point
                    self.center: Point = Point(arg1.x + 0.5*arg2.x, arg1.y + 0.5*arg2.y)
                    self.width: float = arg2.x - arg1.x
                    self.height: float = arg2.y - arg1.y
                case 4:
                    # arg1 is a Line, arg2 is a Line
                    #self.center: Point = Point(arg1.start.x + 0.5*arg2, arg1.y + 0.5*arg3)
                    self.width: float = arg1.lenght
                    self.height: float = arg2.length
                   
        def compute_area(self):
            self.area = self.width * self.height
            return self.area
        def compute_perimeter(self):
            self.perimeter = 2 * (self.width + self.height)
            return self.perimeter
        def compute_interference_point(self, Point):
            pass
        def compute_interference_line(self, Line):
            pass
    
    class Square(Rectangle):
        def __init__(self, method, arg1, arg2):
            super().__init__(method, arg1, arg2)
            self.height = self.width
   ```
   This code features 4 different methods to initialize a Rectangle, and its child class, Square.
   
2. Restourant
   ```
   
   ```

   
