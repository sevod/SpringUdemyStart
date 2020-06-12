# SpringUdemy
11.06.2020
IoC Injection of Controll

Commit 16
Базовый каркас, продемонстрировано внедрение интерфейса
git checkout -b newbrench

B17
Commit 17
Создали новый класс с интерфейсом

B18
Commit 18 (не коммитил)
3 варианты конфигурирования Spring
1. XML
2. Java Annotations
3. Java Soutce Code

B19
Commit 19

Создали файл applicationContext.xml
В нем создаем новые бины
    <bean id="myCoach"
    	class="org.sevod.springdemo.TrackCoach">
    </bean>
	
Для подключения к нашей конфигурации и создания "контекста" используем
ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
Извлечение бина
Coach theCoach = context.getBean("myCoach", Coach.class);
Обязательно закрываем контекст после окончания работы
context.close();

B20 Ничего особенного

12.06.2020
B21 (не коммител)
-Spring Dependency injection (DI)
--Constructor injection
--Setter injection

B22

B23

B24 (не коммител)
Реализуем DI через конструктор
Создаем конструктор в нужном классе и меняем файл applicationContext.xml
    <bean id="myCoach"
    	class="org.sevod.springdemo.BaseballCoach">
    	
    	<!-- set up constructor injection -->
    	<constructor-arg ref="myFortune"></constructor-arg>
    </bean>
	
B25
В HelloSpringApp.java вызываем System.out.println(theCoach.getDailyFortune());


