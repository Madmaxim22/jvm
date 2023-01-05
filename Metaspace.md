# Исследование JVM через VisualVM
## Параметры VM 
-XX:ConcGCThreads=3  
-XX:G1ConcRefinementThreads=10  
-XX:GCDrainStackTargetSize=64  
-XX:InitialHeapSize=259529344  
-XX:MarkStackSize=4194304  
-XX:MaxHeapSize=4152469504  
-XX:MinHeapSize=6815736  
-XX:+PrintCommandLineFlags  
-XX:ReservedCodeCacheSize=251658240  
-XX:+SegmentedCodeCache  
-XX:+UseCompressedClassPointers   
-XX:+UseCompressedOops   
-XX:+UseG1GC   
openjdk version "19.0.1" 2022-10-18  
OpenJDK Runtime Environment (build 19.0.1+10)  
OpenJDK 64-Bit Server VM (build 19.0.1+10, mixed mode)  
## Metaspace
![](/resource/metaspace.png)
1. **Metaspace size - 0kb**  
   **Used metaspace - 0kB**  
   Процессы:
   - Запуск главного метода main;  
   - Вывод в консоль - *"Please open 'ru.netology.JvmExperience' in VisualVm"*;
   - Приостановка программы на 20 секунд.
2. **Metaspace size - 15859kb**  
   **Used metaspace - 15290kB**   
   Процессы:
   - Вывод в консоль - *"14:32:56.773547: loading io.vertx"*
   - Увеличение используемой памяти metaspace'а, из за добавления информации о классах;
   - Увеличение памяти metaspace'а, из за увеличения используемой информации;
   - Вывод в консоль - *"14:32:57.009923: loaded 529 classes"*
3. **Metaspace size - 15859kb**  
   **Used metaspace - 15290kB** 
   Процессы:
   - Приостановка программы на 6 секунд.
4. **Metaspace size - 22147kb**  
   **Used metaspace - 21225kB**   
   Процессы:
   - Вывод в консоль - *"14:33:02.773547: loading io.netty"*;
   - Увеличение используемой памяти metaspace'а, из за добавления информации о классах;
   - Увеличение памяти metaspace'а, из за увеличения используемой информации;
   - Вывод в консоль - *"14:33:03.009923: loaded 2117 classes"*.
5. **Metaspace size - 22147kb**  
   **Used metaspace - 21225kB**   
   Процессы:
   - Приостановка программы на 6 секунд.
6. **Metaspace size - 33681kb**  
   **Used metaspace - 32671kB**  
   Процессы:
   - Вывод в консоль - *"14:33:09.606981: loading org.springframework"*;
   - Увеличение используемой памяти metaspace'а, из за добавления информации о классах;
   - Увеличение памяти metaspace'а, из за увеличения используемой информации;
   - Вывод в консоль - *"14:33:12.009923: loaded 869 classes"*.
7. **Heap size - 275Mb**  
   **Used heap - 189MB**  
   Процессы:    
   - Приостановка программы на 6 секунд; 
   - Простой metaspace памяти;  
   - Завершение работы программы.