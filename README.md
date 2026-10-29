# One Piece — NPC Maker / New Frontier

Editor independente de NPCs, companheiros, criaturas e encontros. Abra `index.html` no navegador ou use a publicação do GitHub Pages. Sem instalação ou etapa de compilação.

## Ferramentas do Guia do Narrador

- **Nova ficha → Criatura pelo Guia:** base de ND 0–30 das tabelas de OP RPG 2.0.3 (pp. 124–126), com revisão antes de aplicar PV, PP, CR, CD e proficiência. O nível do personagem continua independente do ND.
- **Editar ficha → Criatura / ND:** avalia ND defensivo e ofensivo com dano médio das três primeiras rodadas, acerto ou CD predominante, resistências, invulnerabilidades, Logia, salvaguardas e voo. As defesas virtuais não alteram os PV reais. Faixas de PV sobrepostas no Guia têm seleção manual; o modo automático prefere o ND pretendido quando dentro da faixa, depois o centro mais próximo. Empates de ND final arredondam para cima.
- **Editar ficha → Companheiro:** profissão, graduação, função no navio, história, aparência, ideal, vínculo e limites. Lealdade opcional limitada pela maior Presença do grupo (escala 0–20); metade ímpar arredonda para baixo. Valor e histórico ficam reservados ao narrador. A consulta e o texto copiado não expõem lealdade; a impressão exige marcar notas reservadas. Os backups completos contêm dados reservados.
- **Encontros:** planos salvos com grupo de níveis diferentes, companheiros participantes, quantidades e ondas. Fichas vinculadas usam o nível/ND atual; se forem arquivadas ou excluídas, o plano avisa e usa os valores guardados ao adicioná-las.

O cálculo segue os limites e multiplicadores de OP RPG (pp. 45–47): com menos de três participantes, sobe um multiplicador; com cinco ou mais, desce um. Criaturas muito inferiores podem ser excluídas somente da contagem do multiplicador. O XP base continua como recompensa; o XP ajustado serve à avaliação de dificuldade. Cada onda é calculada separadamente. O orçamento diário e os limites de encontros cobrem níveis 1–20; a interface avisa quando não há tabela aplicável. ND 0 pode valer 0 XP quando não representar ameaça, ou 10 XP quando representar.

Os números são orientações de criação, sujeitos à revisão em mesa, especialmente para módulos, controle e Haki. A ferramenta não converte automaticamente fichas de outros sistemas.

## Dados e compatibilidade

O arquivo preserva a chave de armazenamento anterior e normaliza fichas antigas sem alterar seus números. Dados são salvos no IndexedDB, com alternativa em armazenamento local quando disponível. **Exportar → Arquivo completo (JSON)** inclui fichas, pastas e planos de encontros. Exportar uma ficha leva somente seus dados. O HTML exportado inclui o aplicativo e todo o arquivo; não há sincronização entre navegadores.

## Verificação

```sh
node tests/narrator-guide.cjs
```

Testes sem dependências cobrem limites de XP, multiplicadores, ondas, defesas virtuais, dano médio, compatibilidade e normalização dos dados. A interface também deve ser conferida no navegador antes de publicar mudanças de layout.
