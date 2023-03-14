# Programação Web I &amp; II 


![](https://media.licdn.com/dms/image/D4D16AQGXjDuJTi0xew/profile-displaybackgroundimage-shrink_350_1400/0/1664726164160?e=1684368000&v=beta&t=afU-9CR7WwOmTaS-dhowG7vUiZFkr7EbIxvGEEkuE8c  "Photo by ...")

Este repositório contém o material e um conjunto de exemplos relacionados as disciplinas de Programação Web do IFAL.
Atualmente este repositório foca nas tecnologias de HTML, CSS e Javascript para front-end e Java/Jakarta EE/Spring Framework e Node/Express para back-end.

O material deste repositório é usado em disciplinas de nível técnico e superior no [IFAL/Maceió](https://www2.ifal.edu.br/campus/maceio/). 

Em particular:

* *PWEB124 PROGRAMAÇÃO WEB - 01 *: Nível Superior. 
   Documentation [here](doc/intro/main.md).

* *MACDSIPWEB2 - PROGRAMAÇÃO WEB (2022 .1 - 922A)*: Nível Técnico.
   Documentation [here](doc/advanced/main.md). 
   
* *MACDSIPWEB2 - PROGRAMAÇÃO WEB (2022 .1 - 922B)*: Nível Técnico.
   Documentation [here](doc/advanced/main.md). 

* *MAC69WEB24 - PROGRAMAÇÃO WEB II (2022 .1 - 924A)*: Nível Técnico.
   Documentation [here](doc/advanced/main.md). 


-- 


The repository is built with Maven, and it is divided in two main sub-modules:

* `intro`: material used in the first PG5100 course, where the goal is to be able to build
           a web application accessing a SQL database, and deployed on a cloud provider.
           Main technologies: Java, JEE, JPA, EJB, JSF, WildFly, SpringBoot, Spring Security, 
           Selenium, Docker.
           
* `advanced`: material used in the second PG6100 course, where the goal is to dig into the details
            of web services and micro-service architectures.
            Main technologies: Kotlin, SpringBoot, REST, GraphQL, React, Docker, Spring Security, 
            Spring Cloud, AMQP.            


For building GUIs, the second part of the course `advanced` relies on knowledge of JavaScript and Single-Page-Applications.
This is covered in a different course, called [Web Development and API Design](https://github.com/arcuri82/web_development_and_api_design) (PG6301).
Such course should be taken before the `advanced` one (PG6100), in parallel or after the `intro` course (PG5100). 

Before taking these courses, you might want to refresh your knowledge of algorithms and
data structures (e.g., [PG4200](https://github.com/arcuri82/algorithms)), as those are widely used here
(e.g., maps, sets and streams).

### Filosofia deste Repositório

Há muitos recursos (por exemplo, cursos e livros) por aí que lidam com o
*desenvolvimento* de sistemas web/empresariais, utilizando diferentes tecnologias (por exemplo, Java e C#). 
Entretanto, muitas vezes tais recursos lidam apenas com o *desenvolvimento* desses sistemas,
enquanto conceitos importantes como *teste* e *segurança* são tratados como 
apenas preocupações secundárias, se tratadas de alguma forma.
Esta situação tem melhorado nos últimos anos, mas mais poderia ser feito, e esperamos que 
os cursos neste repositório são um passo nessa direção.

Há muitas aplicações fora de lá que são afligidas por bugs e
furos de segurança. 
A correção e a segurança devem desempenhar um papel importante no desenvolvimento de software,
e tentamos refletir isso neste repositório.

Além disso, a engenharia de software é uma disciplina prática, como qualquer outra 
disciplina de engenharia. 
Como tal, embora a teoria seja importante, também é importante 
*sujar as mãos* desenvolvendo software real, e colocando a teoria em prática.
Portanto, neste repositório, todos os conceitos são explicados também através de exemplos,
com casos de teste (unidade e integração/sistema).
Em outras palavras, seguimos o princípio de *Código é Rei*, ou seja, se algo
vale a pena discutir, então você deve ter um exemplo de trabalho com casos de teste para isso.
No passado, teria sido um problema quando você tinha que baixar e configurar
todos os softwares necessários manualmente, como por exemplo um banco de dados PostgreSQL ou um Servidor RabbitMQ. 
Felizmente, com a chegada do *Docker*, isto não é mais um problema.   
    
Neste repositório, são utilizados duas linguagens: *Java* e *Javascript*.
Também são usados dois frameworks diferentes: *Spring* e *Java EE*.
Por que tais escolhas? 
Ao estudar os conceitos de desenvolvimento/teste/segurança de software empresarial,
os idiomas/estruturas efetivamente utilizados não são tão importantes.
Os idiomas/frameworks são usados apenas para obter *prática*, e sujar as mãos.
Por exemplo, usar C# com .Net também teria sido uma opção viável.
Quando você se formar em engenharia de software, por todos os meios depois
você pode acabar trabalhando com C#/.Net e nunca mais tocar em Java. 
Portanto, é importante aprender os conceitos fundamentais por trás desses 
idiomas/estruturas, e não apenas seus detalhes técnicos de baixo nível. 

-----------




Trying and getting some experience with all the main languages and frameworks would be good. 
However, when studying 
such topics for a university degree, time is limited, and one needs to make
some choices.
And switching between too many languages/frameworks would just be a too large overhead
(e.g., learning different IDEs and building tools).
The motivation for the choices of languages and frameworks in this repository is as
follows:

* `Java`: one of the most used programming languages, with a very large
  ecosystem of existing applications and libraries.
  Java is one of the main languages for enterprise development 
  (if not *the* main language). 
  Enterprise systems are often large and complex, and so a *statically typed*
  language is recommended. 
  In our personal opinion, this excludes languages like JavaScript, Python, Ruby, etc.
  TypeScript is statically typed, but it is still JavaScript in its core...  
  Nowadays, C# is a good option, and as a language might even be considered
  better than Java.
  On one hand, it does not have as large ecosystem as Java.
  On the other hand, considering the bullshit of Oracle's new 6 month release cycle,
  .Net seems a more open-source friendly option (depending on how effective
  [adoptopenjdk.net](https://adoptopenjdk.net) will be).
  Note: stating something like this before 2010 (when Oracle bought Sun) would
  rightly grant you a single way ticket to your local asylum.
  So strange to see how much the computing world has changed since 
  the [Java Zone Trailer](https://www.youtube.com/watch?v=8Px-GHPxB4I)
  and 
  [Lady Java](https://www.youtube.com/watch?v=1JZnj4eNHXE)
  videos came out. 
  

* `Kotlin`: our language of choice. It is a better Java that can reuse all
    of its existing ecosystem. 
    However, it does have more abstractions and "magic" than Java, which arguably
    means that it is not suited to learn as first language, i.e., better
    to learn Java first.
    That is the reason why it is only used in the `advanced` course, and not the
    `intro` one.
    Furthermore, job-wise, Kotlin is not so popular yet, although there are some 
    interesting cases (e.g., the Tax Department of Norway using it for their backend
    development, with [few systems open-source](https://github.com/Skatteetaten) on GitHub).


* `Spring`: our framework of choice. SpringBoot is simply great.
    It does have a non-trivial learning curve though.
    However, once you understand the concepts of *dependency injection* and
    *proxy classes*, it is a great tool.
    For the development of web services, DropWizard can be a good choice
    as well, especially if you do not like the "magic" of Spring and want
    a more direct/explicit library. 
    
    
* `Java EE`: in theory it was the "official" Java framework for enterprise development.
   But Oracle (owner of Java) donated it away in 2017, and now it is called `Jakarta EE`.
   Anyway, in our opinion, it is much worse than Spring.
   Job-wise, at least in Norway, it is used less and less. 
   Still, it is important to look at different frameworks. 
   As the jump from Java EE to Spring is relatively simple, it is a good
   choice as starting point before moving into SpringBoot.
   Furthermore, you cannot really appreciate SpringBoot until you have
   gone through the blood, sweat and tears of debugging an
   EJB test using Arquillian to deploy to a WildFly container. 


### Documentation

Current documentation is available 
[here](doc/intro/main.md) for the `intro` course, and
[here](doc/advanced/main.md) for the second `advanced` course.

### Requirements

* JDK 11 (download it from [https://adoptopenjdk.net/](), do not use the JDK from Oracle)
  
* An IDE (recommended _IntelliJ IDEA Ultimate Edition_)

* _Maven_ 3.x

* _Docker_ 

* _Chrome_ and _Chrome Driver_ (only needed to run Selenium tests locally instead of in Docker)

* _YARN_ and _NodeJS_

The code in this repository should run on all major operating systems, i.e. Mac, Linux and Windows.

On Windows, if you have problems with too long file names 
when checking out the code with Git, then you might need to run
the following command on a terminal:

`git config --system core.longpaths true`




### Useful Maven Command

* `mvn clean install -DskipTests`

  this will compile all the code and install all the generated jar files into 
  your local Maven repository. Does not run the tests.
  **Note**: first time your run it, it might take a long while, as needing to download
  many dependencies.
   
 

### How to Contribute

There are many ways in which you can contribute. 
If you found the material in this repository of any use, the easiest
way to show appreciation is to *star* it.
Furthermore, if you find issues, you can report them on 
the [issues](https://github.com/arcuri82/testing_security_development_enterprise_systems/issues) 
page.
Possible types of issues:
  
* Some of the code examples are unclear, or with not enough
  documentation to understand exactly what is going on.
   
  
* You find a *non-intended* security vulnerability or bad practice in any of the 
  code examples.
  Note: in some cases, for didactic reasons there will be non-secure code.
  But in those cases that should be explicitly stated.

* Comments regarding a tool/library/framework are no longer valid (e.g., since a new version
  has been released).


--




### Licença e Direitos Autorais

Os materiais aqui contidos são todos Copyright (c) de [Leonardo Fernandes](https://www.linkedin.com/in/leofernandesmo/) 
e [constribuidores](TODO).
Este material foi e é produzido enquanto trabalho no IFAL/Maceió.

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">
<img alt="Creative Commons License" style="border-width:0" 
src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a>
<br />
The documentation is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivs 4.0 Unported License</a>.


