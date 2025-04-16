# SteerGear

[English](README.md) | Português

Conjunto de engrenagens personalizável para volantes - Criado para usar com AgOpenGPS

Projeto paramétrico criado no FreeCAD para gerar engrenagens personalizadas para o volante de um trator.

<img src="assets/gears.png" alt="Gears" height="500"><br>

Criado usando [Freecad](https://www.freecad.org/downloads.php) 1.0.0 com [freecad.gears workbench](https://github.com/looooo/freecad.gears)

Baixe [`SteerGears.FCStd`](SteerGears.FCStd)

## Variáveis

O `VarSet` contém todas as variáveis disponíveis e está localizado no documento do projeto, abaixo dos dois corpos.

Personalizável:

- `big_teeth_count`: Inteiro - Número de dentes da engrenagem grande - testado na faixa de 30 a 60
- `small_teeth_count`: Inteiro - Número de dentes da engrenagem pequena
- `height`: Float - Altura total das engrenagens
- `module`: Float - Módulo dos dentes da engrenagem
- `teeth_angle`: Ângulo - Ângulo da hélice dos dentes da engrenagem

Variáveis somente leitura - Usadas para cálculos internos e como um resumo das informações das engrenagens

- `big_diameter`: Float - Diâmetro da engrenagem grande
- `big_diameter_inner`: Float - Diâmetro interno da engrenagem grande (dentro dos suportes)
- `big_support_length`: Float - Comprimento disponível para suporte na engrenagem grande - Usado para calcular o número de furos possíveis na peça de suporte
- `gear_ratio`: Float - Relação entre a engrenagem grande e a pequena (grande/pequena)

## Exportar

Atualize as configurações de Tesselação para um valor menor do que o padrão do FreeCAD:

<img src="assets/max_deviation.png" alt="Tesselation in FreeCAD" height="400"><br>

Selecione o corpo do `BigGear`, vá para "Arquivo" e depois para "Exportar". Repita o processo para o `SmallGear`

## Correções de possíveis problemas

Recomendo desativar a recompilação automática:

<img src="assets/skip_recompute.png" alt="Skip recomputes" height="300"><br>

Em seguida, depois de atualizar a engrenagem, use o botão de atualização (🔁) para recalcular

---

Se a navegação for muito lenta (passar o mouse, selecionar, ...), você pode iniciar o FreeCad com o comando:

```bash
QT_QPA_PLATFORM=xcb FreeCAD
```

Mais em [#16560](https://github.com/FreeCAD/FreeCAD/issues/16560)
