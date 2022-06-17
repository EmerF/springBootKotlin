# springBootKotlin
Kotlin:
  dataClasses: 
    semelhante ao pojo
    não tem chaves
    Ex:
    data class dataTes(
      val nome: String
      val id:   Long
    )
    
    
  construtores 
  Ex:
  class TopicoController(private val topicoService: TopicoService){
    
  }
  
  function 
  Ex: 
  
  fun getNome(id: String) :String{
    return nome
  }
  
  pegar .class DataClass::class
  ## Compilação
    gera o código compilado em uma pasta out dentro do projeto
   
  ## Generics
    utiliza o tipo E para dizer que é genérico
    
    class MutableStack<E>(vararg items: E) {              // 1

    private val elements = items.toMutableList()

    fun push(element: E) = elements.add(element)        // 2

    fun peek(): E = elements.last()                     // 3

    fun pop(): E = elements.removeAt(elements.size - 1)

    fun isEmpty() = elements.isEmpty()

    fun size() = elements.size

    override fun toString() = "MutableStack(${elements.joinToString()})"
  }
  
  ## Herança
    usar open fun para habilitar a herança
    qdo tiver necessidade de um comportamento muito específico, que NÃO sirva para todos, criar uma nova classe.Ex: funcionárioAdmin tem autenticação que não é necessária para funcionário comum
  
  
  ### Rest
  return codes:
  get: 200 ok
  post: 201 created. Recurso novo retorna o path(uri)
                     Atualizado: devolve os dados novos
  delete:204 no content pois o registro foi deletado
  
  tratamento de erros:
  criar classe que represanta o erro
  criar um Controller advice que trata todos os erros de controllers
  
  ### JPA
  
    classes entity devem possuir um construtor no args. Dá para fezer isso usando dependências no pom
  ## Migrations
  
    conceito que nos ajuda a ter controle sobre a estutura de nossas tabels. Registra as alterações no esquema de banco de dados: criações de tabelas, alterações, drops
    Substitui a propriedade hibernate.hbm2ddl.auto e evita problemas de apagar dados das tabelas por exemplo
  
  ## Flyway
    Plugin para fazer migrations
    procura na pasta src/main/resources/db/migrations no projeto
    ** arquivos são imutaveis.
      padrão: 
          V1__create_table_delivery_methods
          V2__add_deliverymethods_column_name
      
  
    
  
