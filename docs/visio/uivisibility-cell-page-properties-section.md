---
title: Zelle "UIVisibility" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437329"
---
# <a name="uivisibility-cell-page-properties-section"></a>Zelle "UIVisibility" (Abschnitt "Page Properties")

Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Der Seitenname wird in der Benutzeroberfläche angezeigt (Standardwert).  <br/> |**visUIVNormal** <br/> |
|1  <br/> |Der Seitenname wird nicht in der Benutzeroberfläche angezeigt.  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>Hinweise

Durch Festlegen der Zelle UIVisibility auf **visUIVHidden** wird verhindert, dass die Seite an einer beliebigen Stelle auf der Benutzeroberfläche angezeigt wird, an der die Zeichenfolge mit dem Seitennamen angezeigt wird. Beispielsweise würde die Seite nicht als Option  im Zeichnungs-Explorer oder auf den Registerkarten der Seite aufgeführt. Auf die Seite kann jedoch weiterhin zugegriffen werden, wenn Sie Automatisierungs- oder Benutzeroberflächenpfade verwenden, die nicht den Seitennamen enthalten, z. B. den **Befehl Drucken.** 
  
 Diese Zelle ist für die Verwendung mit Dokumentseiten vorgesehen. Sie ist nicht für die Verwendung mit Markupüberlagerungsseiten vorgesehen, für die die Zelle UIVisibility standardmäßig **auf visUIVHidden** festgelegt ist und nicht geändert werden sollte. 
  
> [!NOTE]
> Um eine Seite aus dem  Befehl Drucken des Dokuments auszublenden, machen Sie sie zu einer Hintergrundseite (**Type-Eigenschaft** ist **visTypeBackground** ), die von keinem Blatt als Hintergrund verwendet wird (Shapes auf Hintergrundseiten werden gedruckt, wenn eine Seite gedruckt wird, die sie als Hintergrund verwendet). Der Befehl **Drucken** des Dokuments funktioniert nur mit indizierten Seiten, und Hintergrundseiten werden nicht indiziert. 
  
Um einen Verweis auf die Zelle UIVisibility anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |UIVisibility  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle UIVisibility nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageUIVisibility** <br/> |
   

