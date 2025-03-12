# Felipe Lopes Gomide

## Questão 1:

$A \gets (Pesquisador X Autoria X Artigo)$

$A \gets (\sigma_{P.PID=Aut.PID \land Art.AID=Aut.AID}A)$

$\Pi_{P.Nome}(\sigma_{Aut.pos=1, Art.Ano=2020, art.veiculo="VLDB Journal"}A)$

## Questão 2:

$A \gets (Artigo \Join Autoria \Join Pesquisador)$

$\Pi_{P.Nome}(\sigma_{Aut.pos=1, Art.Ano=2020, art.veiculo="VLDB Journal"}A)$

## Questão 3:

$A \gets (Pesquisador ⟕ Autoria)$

$\Pi_{P.Nome}(\sigma_{Aut.PID=NULL}A)$

## Questão 4:

$S \gets \Pi_{Art.ID}(\sigma_{Art.Ano=2015}Artigo)$

$R \gets \Pi_{Aut.PID,Aut.AID}(Autoria)$

$Q \gets R \div S$

## Questão 5:

$D \gets Pesquisador \bowtie Autoria$

$S \gets (\sigma_{P.Nome="J Silva"}D)$

$R \gets (D \bowtie_{D.AID=C.Citante}Citação)$

$R \gets (R \bowtie _{C.Citado = S.AID}S)$

$\Pi_{D.Nome}(R)$

## Questão 6:

$R\gets(Citação\bowtie_{Citação.Citado=Artigo.AID} Artigo)$

$S \gets (Citação \bowtie _{Citação.Citante=Artigo.AID}Artigo)$

$\Pi _{R.AID}(R \bowtie_{S.Citado=R.AID\land R.Ano=S.Ano}S)$