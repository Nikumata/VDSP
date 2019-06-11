# VDSP

#### 消费记录类：  
  Consume:  
  id: 2017141461055 name: 黄永杰 t: Fri Apr 27 08:05:43 CST 2018 money: 2.07 type: 8 remark: 计算机学院（软件学院）2017级 grade: 2017  

#### baseline时间范围内，所有学生的消费信息：
  baselineMap <Long, List<Consume>>  
  Long : 学生id  
  List<Consume> ： 消费记录集合  

#### recent时间范围内，所有学生的消费信息：
  recentMap <Long, List<Consume>>  
  Long : 学生id  
  List<Consume> ： 消费记录集合  
  
#### 时间窗类：
  Interval：  
  begin:时间窗开始时间（s）  
  end:时间窗结束时间（s）  

#### DBSCAN聚类:
  根据学生id，从recentMap中找到对应的消费记录集合List<Consume>，通过聚类Consume中t的时刻，得到时间窗List<Inteval>  
  
#### 时间窗消费汇总类:
  InConsume:  
    Interval：时间窗信息  
    int[21] consums:下标对应消费type，value为消费总金额  

#### u在recent时间范围内，根据List<Interval>时间窗，划分的消费信息：  
  uRecentMap<Long, List<InConsume>>  
