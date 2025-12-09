# GL_POINTS
Menggambarkan titik-titik

```C++
glPointSize(5.0);  
glBegin(GL_POINTS);  
  glVertex3f(20.0, 20.0, 0.0);  
  glVertex3f(80.0, 20.0, 0.0);  
  glVertex3f(80.0, 80.0, 0.0);  
  glVertex3f(20.0, 80.0, 0.0);  
glEnd();
```
	
![[GL_POINTS.png]]
# GL_LINES
Menghubungkan setiap 2 titik
```C++
glBegin(GL_LINES);  
  glVertex3f(20.0, 20.0, 0.0);  
  glVertex3f(80.0, 20.0, 0.0);  
  
  glVertex3f(80.0, 80.0, 0.0);  
  glVertex3f(20.0, 80.0, 0.0);  
glEnd();
```

![[GL_LINES.png]]

# GL_LINE_STRIP
Menghubungkan setiap titik ke titik lain
```
glBegin(GL_LINE_STRIP);  
  glVertex3f(20.0, 20.0, 0.0);  
  glVertex3f(80.0, 20.0, 0.0);  
  
  glVertex3f(80.0, 80.0, 0.0);  
  glVertex3f(20.0, 80.0, 0.0);  
glEnd();
```

![[GL_LINE_STRIP.png]]

# GL_LINE_LOOP
Menghubungkan satu titik ke titik lain, kemudian menghubungkan titik terakhir ke titik pertama
```C++
glBegin(GL_LINE_LOOP);  
  glVertex3f(20.0, 20.0, 0.0);  
  glVertex3f(80.0, 20.0, 0.0);  
  
  glVertex3f(80.0, 80.0, 0.0);  
  glVertex3f(20.0, 80.0, 0.0);  
glEnd();
```
![[GL_LINE_LOOP.png]]
# GL_POLYGON
Menghubungkan setiap titik ke titik lain (titik terakhir dan pertama termasuk), kemudian mewarnai isi
```C++
glBegin(GL_POLYGON);  
  glVertex3f(20.0, 20.0, 0.0);  
  glVertex3f(80.0, 20.0, 0.0);  
  glVertex3f(80.0, 80.0, 0.0);  
  glVertex3f(20.0, 80.0, 0.0);  
glEnd();
```
![[GL_POLYGON.png]]