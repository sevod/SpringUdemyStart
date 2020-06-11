# SpringUdemy
11.06.2020
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