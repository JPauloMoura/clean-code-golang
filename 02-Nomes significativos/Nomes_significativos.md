# Nomes significativos
Escolher bons nomes leva tempo, mas economiza mais.
Então cuide de seus nomes e troque-o quando encontar melhores.

**Ruim:**
```go
var d // data atual
```
**Bom:**
```go
var today
```
---
**Cuidado ao usar nomes muito parecidos. Fica difícil perceber as pequenas diferenças**
```go
func getDaysWorkedWithOvertime(){
  //code
}

func getDaysWorkedWithoutOvertime(){
  //code
}
```
---

### Use nomes que revelem seu propósito
Escolher nomes que revelem seu propósito pode facilitar bastante o entendimento e a alteração do código.

Por exemplo, você saberia dizer qual o propósito deste código?
```go
func getThem(theList List) List {
	var list1 List

	for _, x := range theList {
		if x[0] == 4 {
			list1 = append(list1, x)
		}
	}
	return list1
}
```
É agora?
```go
const STATUS = 0
const HAS_BOMB = 4

func getCellsWithBombs(gameBoard Cells) Cells {
	var cellsWihBombs Cells

	for _, cell := range gameBoard {
		if cell[STATUS] == HAS_BOMB {
			cellsWihBombs = append(cellsWihBombs, cell)
		}
	}
	return cellsWihBombs
}
```
Com essas simples alterações de nomes, não fica difícil entender o que está acontecendo. Esse é o poder de escolher bons nomes.

---
### Faça distinções significativas nos nomes
Usar números sequenciais em nomes `(a1, a2)` nao oferece informação alguma sobre o real sentindo do dado.

Palavras muito comuns são outra forma de distinção que nada expressam:

```go
  type Product struct {}

  type ProductInfo struct {}

  type ProductData struct {}
```
```go
  func getProduct() {}

  func getProductInfo() {}

  func getProductData() {}
```
Nesses casos foram usados nomes distintos que não revelam nada de diferente. Info e Data são palavras comuns e vagas. Então, **faça a distinção dos nomes de uma forma que o leitor compreenda as diferenças**.


