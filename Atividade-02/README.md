# Atividade 02 - Reconhecimento de Atividades Humanas com Modelos Clássicos

## Objetivos
- Trabalhar com uma base de dados reais derivados de acelerômetros e giroscópios presentes em _smartphones_ contendo múltiplos _datasets_;
- Aplicar modelos tradicionais de classificação não-linear;
- Realizar uma comparação sistemática entre os desempenhos de diferentes classificadores.
  
## Conjunto de dados

DAGHAR - Disponível no Zenodo: https://zenodo.org/records/13987073

Apresentação detalhada do _dataset_: https://www.nature.com/articles/s41597-024-03951-4

### Informações dos *datasets* contidos no DARHAR

**Parâmetros originais[^1]:**
![](https://github.com/EA991-Lab/utils/blob/main/figs/daghar_1.png)

**Atividades selecionadas para o DARHAR[^1]:**
![](https://github.com/EA991-Lab/utils/blob/main/figs/daghar_2.png)

- Padronização dos rótulos (_standard activity code_):

| Rótulo    | Atividade |
| :----:    |    :---   
| 0   | Estar sentado       
| 1   | Ficar em pé        
| 2   | Caminhar        
| 3   | Subir escadas      
| 4   | Descer escadas
| 5   | Correr      

**Particionamento[^1]:**

![](https://github.com/EA991-Lab/utils/blob/main/figs/daghar_3.png)

**Organização das amostras:**
- Cada amostra contém janelas de 3 segundos (sem sobreposição) concatenadas de Acc-x, Acc-y, Acc-z, Gyr-x, Gyr-y, Gyr-z.

## Procedimento de entrega

1. Faça um *fork* do repositório 'Atividade_02' para a sua conta;
2. Abra o *notebook* 'roteiro_atividade_02_EA991_1s2025' e desenvolva a sua solução para os itens propostos;
3. Ao terminar de resolver a atividade, faça o *upload* do *notebook*, renomeado conforme o padrão atividade_02_numero_RA.ipynb, no diretório 'solucao' dentro do repositório.
   - Google Colab: Arquivo -> Salvar uma cópia no Github -> Selecione o repositório (o *fork* criado). No campo "caminho", coloque "solucao/atividade_02_numero_RA.ipynb" para que o *notebook* seja colocado no diretório desejado. 
     
## Prazo para entrega

**Data:** 06/05/2025

[^1]: Napoli, O., Duarte, D., Alves, P. et al. A benchmark for domain adaptation and generalization in smartphone-based human activity recognition. Sci Data 11, 1192 (2024). https://doi.org/10.1038/s41597-024-03951-4


