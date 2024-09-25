# ETAPA 3 AC1

Criei a classe filme e determinei atributos e condições para ser valido 

### 📋 Código
Crie uma classe Filme que contém os atributos título, duração em minutos e gênero. Essa classe deve encapsular e validar todos os atributos.

O título não pode estar vazio.
A duração deve ser maior que zero.
O gênero de ser Romance, Terror ou Comédia;

public class Filme { //Aqui defini a classe e seus atributos
    private String título;
    private int duração;
    private String gênero;

    Filme(String título, int duração, String gênero) { //Inicializei os atributos atraves do metodo constructor e usei o metodo setters para validar os valores
        setTítulo(título);
        setDuração(duração);
        setGênero(gênero);
    }

    public String getTítulo() { //No titulo, duração e Genero utilizei o metodo Setters e Getters para acessar e modificar os atributos de forma mais controlada incluido a validação que o titulo nao pode estar vazio, a duração ser maior que 0 e o genero deve ser Romance, Terror ou Comedia
        return título;
    }

    public void setTítulo(String título) {
        if (título == null || título.isEmpty()) { //Coloquei a condiçao que o titulo nao pode estar vazio
            System.out.println("O título não pode estar vazio.");
        }
        this.título = título;
    }

    public int getDuração() {
        return duração;
    }

    public void setDuração(int duração) { 
        if (duração <= 0) { //Coloquei a condiçao que a duraçao precisa ser maior que 0
            System.out.println("A duração deve ser maior que zero.");
        }
        this.duração = duração;
    }

    public String getGênero() {
        return gênero;
    }

    public void setGênero(String gênero) { //Coloquei a condiçao que o genero deve ser igual a Romance, Terror ou Comedia
        if (!gênero.equals("Romance") && !gênero.equals("Terror") && !gênero.equals("Comédia")) { 
            System.out.println("O gênero deve ser Romance, Terror ou Comédia.");
        }
        this.gênero = gênero;
    }

    public String descricao() { //Moldei como o codigo deve rodar a descriçao
        return "Nome: " + this.título + "\n" +
               "Duração (em minutos): " + this.duração + "\n" +
               "Gênero: " + this.gênero + "\n";
    }

    public static void main(String[] args) {
        try {
            Filme f1 = new Filme("Vai Que Cola o Filme", 95, "Comedia");
            Filme f2 = new Filme("Hereditário", 127, "Terror");
            System.out.println(f1.descricao());
            System.out.println(f2.descricao());
        } catch (IllegalArgumentException e) {
            System.out.println(e.getMessage());
        }
    }
}
///////////////////////////////////////////////////////////////////////////////


## 🛠️ Construído com

Ferramentas utilizadas e bibliotecas

* IDE Eclipse

## 📌 Versão

* **Versão 1.0** caso seja atualizado manter a descrição inicial e inserir uma nova linha com descrição da atualização.
* **Versão 1.1** - *Refatoração* *data 09/09/24*

## ✒️ Autores

João Carlos Ferreira de Araujo RA 248152 -- AC1 de Programação Orientada à Objetos
