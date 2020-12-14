#  Описание
Пример бизнес процесса на Tibco
# Сборка проекта через Maven
1) В папке .m2 в файле settings.xml
a) Добавить profile (в <tibco.home> прописать свой путь до tibco)
```xml
	<profile>
		<id>tibco</id>
		<activation>
			<activeByDefault>true</activeByDefault>
		</activation>
		<properties>
			<tibco.home>C:\tibco</tibco.home>
			<executables.extension>.exe</executables.extension>
			<libraries.extension>.dll</libraries.extension>
			<tibco.bw.version>5.8</tibco.bw.version>
			<tibco.designer.version>5.8</tibco.designer.version>
			<tibco.ems.version>6.3</tibco.ems.version>
			<tibco.tra.version>5.8</tibco.tra.version>
			<tibco.rv.version>4.9</tibco.rv.version>
			<tibco.hawk.version>4.9</tibco.hawk.version>
		</properties>
	</profile>
```
b) Добавить плагины в <pluginGroups>

	<pluginGroup>fr.fastconnect.factory.tibco.bw.maven</pluginGroup>
	<pluginGroup>fr.fastconnect.factory.tibco.bw.codereview</pluginGroup>
	<pluginGroup>fr.fastconnect.factory.tibco.bw.fcunit</pluginGroup>

2) Запустить админскую консоль, перейти в папку проекта (BusinessWorks)
3) Выполнить: mvn clean package
