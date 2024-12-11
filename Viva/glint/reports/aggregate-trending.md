---
title: Viva Glint aggregate grouping - trends and best practices
description: Aggregate grouping can surface useful insights but the survey cycles must be identical in order for this trend to show.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: trend, aggregate score, trend score, aggegate trend
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 12/11/2024
---

# Viva Glint aggregate groupings - trends and best practices

## Understand aggregate trending

Aggregate trending informs historical data over time. Trend points reflect matching items from one cycle to the cycle immediately preceding it. Changing items within an aggregate (group) interrupts trend.

## Viva Glint aggregate trending terminology

| Term | Definition |
|-----------|-----------|
|Aggregate | A grouping of two or more items that measure a concept within a survey|
|Aggregate score | The average score of all the items divided by that number of items|
|Trend | Any difference in the score of a single item from one cycle to the previous cycle |
|Aggregate trend | Any difference in the combined score from one cycle to the previous cycle. Aggregate trend exists only when all items in two consecutive cycles are identical. |

>[!TIP]
> It's best not to use aggregate groupings in surveys.

## Aggregate grouping can lead to unreliable aggregate trend 

Why **not** to use aggregate groupings in surveys: 

- Surveying more frequently with fewer individual questions produce more useful, focused results. 
- Measuring single items are better than multiple-item measures when it comes to utility and reliability. They can predict future behavioral outcomes, and they can do it consistently over time. 
- Grouping multiple items (an aggregate) may limit the intervention opportunities for a single item within that group. That one item can become lost inside the group of items. 
- Action taking should only happen at the single item level. Focusing managers on aggregate scores doesn’t help enable action. 

>[!CAUTION]
> Trend is unreliable when it isn't measuring “apples to apples” - when there are differences in the items that appear in an aggregate between the new cycle and the same aggregate in the previous cycle. Trend is shown when at least one item is identical in the same aggregate in two cycles. Unless all items are identical, however, the aggregate trend isn't measuring a consistent group of items and isn't as reliable as single item trend data.

## Aggregate trend examples across 2 cycles
There's a lot to consider when comparing survey cycles with aggregate groupings.

### Use case 1
3 items are part of the aggregate in both cycles, but because they aren't the same 3 items; no aggregate trend forms.

:::image type="content" source="../../media/glint/reports/aggregate-1.png" alt-text="Chart showing that Cycle A and Cycle B don't share the same three items.":::

### Use case 2 
One item is removed from the aggregate in the second cycle.
Cycle A contains 3 items, but Cycle B contains only 2 items. Aggregate Trend doesn’t exist because the aggregate isn't identical; there's no aggregate history. Individual items show trend but they don't reflect upon the aggregate as a whole unit.

:::image type="content" source="../../media/glint/reports/aggregate-2.png" alt-text="Chart showing the 2 cycles share no history because the aggregate trend isn't identical.":::

### Use case 3 
A new question is added to the aggregate grouping.
A new item is added to Cycle B so no aggregate trend is associated; there's no identical history. 

:::image type="content" source="../../media/glint/reports/aggregate-3.png" alt-text="Chart showing that no aggregate history is associated between the 2 cycles.":::

## Aggregate trend across 3 or more cycles

>[!IMPORTANT]
>Trend always looks at the previous cycle. 

### Use case 4 

:::image type="content" source="../../media/glint/reports/aggregate-4.png" alt-text="Chart showing only the last 2 cycles are considered for aggregate trending.":::

### Use case 5

:::image type="content" source="../../media/glint/reports/aggregate-5.png" alt-text="Chart showing aggregate trend becomes more complicated across multiple cycles.":::
