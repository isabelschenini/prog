# prog
atividades programação 
//Exercicio 2
<?php
class Empregados{
  public $pnome;
  public $snome;
  public $salmen;
  public $salanu;

  public function __construct(){
    $this-> pnome = "Leonardo";
    $this-> snome = "Messa Wagner";
    $this-> salmen = 2000.00;
  }
  public function setPnome($recebe){
    return $this->pnome = $recebe;
  }
  public function getPnome(){
    return $this ->pnome;
  }
  public function setSnome($recebe1){
    return $this->snome = $recebe1;
  }
  public function getSnome(){
    return $this ->snome;
  }
  public function setSalmen($recebe2){
    return $this->salmen = $recebe2;
  }
  public function getSalmen(){
    return $this ->salmen;
  }
  public function setSalanu(){
    
    return $this->salanu = $this->salmen*12;
  }
  public function getSalanu(){
    return $this ->salanu;
  }
  public function validaSalmen(){
    if($this->salmen < 0){
      $this->salmen = 0.0;
    }
  }
  public function aumentasalmen(){
    $porc = ($this->salmen*10)/100;
    $this-> salmen = $this->salmen + $porc;
  }
}
//empregado 1
$emp1 = new Empregados();
$emp1->validaSalmen();
$emp1->setSalanu();
echo "O salario anual de {$emp1-> getPnome()} {$emp1->getSnome()} é R$ {$emp1->getSalanu()}\n"; 
$emp1 -> aumentasalmen();
$emp1->setSalanu();
echo "O salario anual de {$emp1-> getPnome()} recebeu acrescimo de 10% e agora é de R$ {$emp1->getSalanu()} \n ";
//empregado 2
$emp2 = new Empregados();
$emp2 -> setPnome("Junior");
$emp2 -> setSnome("da Silva");
$emp2->setSalmen(1000);
$emp2->validaSalmen();
$emp2->setSalanu();
echo "O salario anual de {$emp2-> getPnome()}  {$emp2->getSnome()} é R$ {$emp2->getSalanu()} \n"; 
$emp2 -> aumentasalmen();
$emp2->setSalanu();
echo "O salario anual de {$emp2-> getPnome()} recebeu acrescimo de 10% e agora é de R$ {$emp2->getSalanu()} \n ";
?>
