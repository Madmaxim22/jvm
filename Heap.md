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
## Heap
![](/resource/heap.png)
1. **Heap size - 260Mb**  
   **Used heap - 12MB**  
   Процессы:
   - Запуск главного метода main;  
   - Вывод в консоль - *"Please open 'ru.netology.JvmExperience' in VisualVm"*;
   - Приостановка программы на 20 секунд.
2. **Heap size - 260Mb**  
   **Used heap - 34MB**  
   Процессы:
   - Вывод в консоль - *"14:32:56.773547: loading io.vertx"*
   - Увеличение используемой памяти heap'а, из за создания и использования классов LocalTime, Reflections, а так же храние информации в интерфейсе Set <Class<?>>;
   - Вывод в консоль - *"14:32:57.009923: loaded 529 classes"*
3. **Heap size - 260Mb**  
   **Used heap - 34MB**  
   Процессы:
   - Приостановка программы на 6 секунд.
4. **Heap size - 260Mb**  
   **Used heap - 9MB**   
   Процессы:  
   - Происходит процесс сборки мусора без остановки программы.
5. **Heap size - 260Mb**  
   **Used heap - 42MB**  
   Процессы:
   - Вывод в консоль - *"14:33:02.773547: loading io.netty"*;
   - Увеличение используемой памяти heap'а, из за создания и использования классов LocalTime, Reflections, а так же храние информации в интерфейсе Set <Class<?>>;
   - Вывод в консоль - *"14:33:03.009923: loaded 2117 classes"*.
6. **Heap size - 260Mb**  
   **Used heap - 42MB**    
   Процессы:
   - Приостановка программы на 6 секунд.
7. **Heap size - 260Mb**  
   **Used heap - 83MB**  
   Процессы:
   - Вывод в консоль - *"14:33:09.606981: loading org.springframework"*;
   - Увеличение используемой памяти heap'а, из за создания и использования классов LocalTime, Reflections, а так же храние информации в интерфейсе Set <Class<?>>;
   - Вывод в консоль - *"14:33:12.009923: loaded 869 classes"*.
8. **Heap size - 260Mb**  
   **Used heap - 83MB**    
   Процессы:  
   - Приостановка программы на 6 секунд.
9. **Heap size - 275Mb**  
   **Used heap - 189MB**  
   Процессы:
   - Вывод в консоль - *"14:33:16.607423: now see heap"*;
   - Вывод в консоль - *"14:33:16.607567: creating 5000000 objects"*;
   - Увеличение используемой памяти heap'а, из за создания 5000000 объектов класса SimpleObject;
   - Увеличение памяти heap'а;
   - Вывод в консоль - *"14:33:17.607567: created"*.
10. **Heap size - 275Mb**  
   **Used heap - 189MB**   
   Процессы:    
   - Приостановка программы на 6 секунд.  
11. **Heap size - 460Mb**  
   **Used heap - 447MB**  
    Процессы:
   - Вывод в консоль - *"14:33:21.607423: now see heap"*;
   - Вывод в консоль - *"14:33:21.607567: creating 5000000 objects"*;
   - Увеличение используемой памяти heap'а, из за создания 5000000 объектов класса SimpleObject;
   - Увеличение памяти heap'а;
   - Вывод в консоль - *"14:33:22.607567: created"*.
12.  **Heap size - 460Mb**  
   **Used heap - 447MB**  
   Процессы:    
   - Приостановка программы на 6 секунд.  
13.  **Heap size - 1412Mb** 
14.  **Used heap - 651MB**  
   Процессы:
   - Вывод в консоль - *"14:33:28.607423: now see heap"*;
   - Вывод в консоль - *"14:33:28.607567: creating 5000000 objects"*;
   - Увеличение используемой памяти heap'а, из за создания 5000000 объектов класса SimpleObject;
   - Увеличение памяти heap'а;
   - Вывод в консоль - *"14:33:29.607567: created"*.
15.  **Heap size - 1412Mb**  
   **Used heap - 651MB**  
   Процессы:    
   - Приостановка программы на 6 секунд;  
   - Завершение работы программы.