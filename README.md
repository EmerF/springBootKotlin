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
  
  ### Rest
  return codes:
  get: 200 ok
  post: 201 created. Recurso novo retorna o path(uri)
                     Atualizado: devolve os dados novos
  delete:204 no content pois o registro foi deletado
  
  tratamento de erros:
  criar classe que represanta o erro
  criar um Controller advice que trata todos os erros de controllers
