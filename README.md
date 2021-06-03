# Practical.CleanArchitecture

# Links
https://github.com/microsoftarchive/cqrs-journey



clean-architecture-api-boilerplate

root - repositório
 - docs
 -  database
 - microservice (nome a definir)
	 - src
		 - **application** - _camada de aplicação_
		   - errors - _erros e ou exceções da aplicação_
		   - use-cases - _representa as lógica de negócios  **do aplicativo**_
		   - validation - _controla a validação dos value objects_
		   - controllers - _gerencia o comportamento dos dados através de regras de negócios_
		   - middlewares - _uma camada de abstração da aplicação_
		 - **common** - _camada comun_
		   - adapters - _adaptares de modelos de datasources_
			   - TreeAdpter - _classe_
		   - helpers - _ajudantes - classes comuns_
			   -  ObjectKey - _classe_
			- data-mappers - _mapeadores de dados são rápidos de escrever e simples de testar e mesmo que sua implementação seja entediante. [http://modelmapper.org/](http://modelmapper.org/)
		- **domain** - _camada de domínio_
        	- entities - 
        	  - User - classe user
        	  - Progress - classe progress
        	  - UserProgress - classe user progress
        	- value-objects - _**objeto** imutável sem identidade. Ex.: Email, FullName_
             	-  Email - classe e-mail
        	- use-cases - _representa as lógica de negócios  **do domínio**_
        	- repositories - _ armazena classes abstratas de repositórios_ 
	   - **models** - _camada de modelos de datasources_
		   - UserModel - classe User
	       - dtos -  _ Os DTOs são a representação do modelo de objeto de uma solicitação / resposta JSON / XML ou de uma tabela de banco de dados, portanto sua estrutura é a mais adequada para a comunicação remota_
       - **infrastructure** - _camada de infra "frameworks"
         - express
         - nestjs
         - typeorm
       - **presentation** - camada de apresentação
         - responses
         - requests
       - **datasources** - camada fonte de dados, na qual os dados se originam e permite sua persistência_
         - **repositories** - _O padrão Repository faz a mediação entre o domínio e as camadas de mapeamento de dados ([Martin Fowler](http://martinfowler.com/))_
           - ProgressRepository
           - UserRepository
           - fakers -_preencher sua persistência para fazer um teste de resistência ou anonimizar dados obtidos de um serviços_
             - FakerRepository - classe faker de um repositório
           - TreeRepository
           - UserRepository

Refs:


>  - [Domain Driven Design](https://domainlanguage.com/ddd/)
>  - [Design a DDD-oriented microservice](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/ddd-oriented-microservice)
>  - [Design a microservice domain model](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/microservice-domain-model)
> - [Definition of the software principle ‘clean architecture’](https://logistikknowhow.com/en/it-and-software/definition-of-the-software-principle-clean-architecture/#:~:text='Clean%20architecture'%20is%20an%20architectural,frameworks%2C%20databases%20and%20user%20interfaces.)
>  - [Explaining Clean Architecture](https://www.oncehub.com/blog/explaining-clean-architecture)
>  - [Why you need Use Cases/Interactors](https://proandroiddev.com/why-you-need-use-cases-interactors-142e8a6fe576)
>  - [The “Real” Repository Pattern in Android](https://proandroiddev.com/the-real-repository-pattern-in-android-efba8662b754)
>  - [Why ModelMapper?](http://modelmapper.org/)
>  - [Design the infrastructure persistence layer](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design)
>  - [Repository](https://martinfowler.com/eaaCatalog/repository.html)
>  - [SOLID](https://deviq.com/principles/solid)
