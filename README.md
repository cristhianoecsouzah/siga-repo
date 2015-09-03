# siga-repo
Repositório maven com bibliotecas específicas do SIGA


# Como usar o siga-repo?

Acrescente o seguinte trecho no seu arquivo pom.xml

```
	<repositories>
	
	  ... 
		
		<repository>
			<id>github</id>
			<url>https://raw.githubusercontent.com/projeto-siga/siga-repo/master/repo</url>
		</repository>
		
		...
		
  </repositories>
```


# Adicionando uma nova biblioteca no siga-repo

* Faça o clone deste repositório (https://github.com/projeto-siga/siga-repo.git)
* Execute o comando abaixo, alterando os parêmetros necessários

```
mvn install:install-file -Dfile=C:\deploy\arquivo.jar -DgroupId=br.jus.trf2 -DartifactId=biblioteca-x -Dversion=1.2.3 -Dpackaging=jar -DlocalRepositoryPath=C:\Trabalhos\Repositorios\siga-repo\repo
```

Onde,

```
-Dfile = arquivo que se deseja incluir no repositório
-DgroupId = nome do grupo que será utilizado no pom.xml do projeto que fizer referência ao arquivo.
-DartifactId = nome do artefato que será utilizado no pom.xml do projeto que fizer referência ao arquivo.
-Dversion = versão do artefato
-Dpackaging = tipo do empacotamento
-DlocalRepositoryPath = caminho do repositório (onde o siga-repo foi clonado)
```

* O arquivo será instalado no repositório especificado em -DlocalRepositoryPath
* Faça o commit/push do repositório para publicar a instalação



