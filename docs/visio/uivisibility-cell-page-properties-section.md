---
title: Zelle "UIVisibility" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
ms.localizationpriority: medium
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.
ms.openlocfilehash: 564cb13d5b8e1cf1394787bba1d5bdab82a9c85a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603228"
---
# <a name="uivisibility-cell-page-properties-section"></a>Zelle "UIVisibility" (Abschnitt "Page Properties")

Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Der Seitenname wird in der Benutzeroberfläche angezeigt (Standardwert).  <br/> |**visUIVNormal** <br/> |
|1  <br/> |Der Seitenname wird nicht in der Benutzeroberfläche angezeigt.  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Durch Festlegen der Zelle "UIVisibility" auf **visUIVHidden** wird verhindert, dass die Seite an einer beliebigen Stelle auf der Benutzeroberfläche angezeigt wird, in der die Zeichenfolge mit dem Seitennamen angezeigt wird. Beispielsweise wäre die Seite nicht als Option im **Zeichnungsexplorer** oder auf den Seitenregisterkarten aufgeführt. Auf die Seite kann weiterhin zugegriffen werden, wenn Sie jedoch Automatisierungs- oder Benutzeroberflächenpfade verwenden, die nicht den Seitennamen enthalten, z. B. den Befehl **"Drucken".** 
  
 Diese Zelle ist für die Verwendung mit Dokumentseiten vorgesehen. sie ist nicht für die Verwendung mit Markupüberlagerungsseiten vorgesehen, bei denen die Zelle "UIVisibility" standardmäßig auf **visUIVHidden** festgelegt ist und nicht geändert werden sollte. 
  
> [!NOTE]
> Um eine Seite aus dem Befehl **"Drucken"** des Dokuments auszublenden, machen Sie sie zu einer Hintergrundseite (**Die Type-Eigenschaft** ist **visTypeBackground** ), die von keiner Seite als Hintergrund verwendet wird (Shapes auf Hintergrundseiten werden gedruckt, wenn eine Seite gedruckt wird, die sie als Hintergrund verwendet). Der Befehl **"Drucken"** des Dokuments funktioniert nur mit indizierten Seiten, und Hintergrundseiten sind nicht indiziert. 
  
Um einen Verweis auf die Zelle "UIVisibility" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |UIVisibility  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle UIVisibility anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageUIVisibility** <br/> |
   

