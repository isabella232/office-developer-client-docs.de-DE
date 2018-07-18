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
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798365"
---
# <a name="uivisibility-cell-page-properties-section"></a>UIVisibility Cell (Page Properties Section)

Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Der Seitenname wird in der Benutzeroberfläche angezeigt (Standardwert).  <br/> |**visUIVNormal** <br/> |
|1  <br/> |Der Seitenname wird nicht in der Benutzeroberfläche angezeigt.  <br/> |**UIVisibility** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Zelle UIVisibility auf **UIVisibility** verhindert die Seite an einer beliebigen Stelle in der Benutzeroberfläche, wo die Zeichenfolge mit dem Namen der Seite angezeigt wird. Beispielsweise wird die Seite nicht als Option im **Zeichnungsexplorer** oder auf den Seitenregisterkarten aufgelistet werden. Die Seite weiterhin zugegriffen werden, jedoch bei Verwendung von Automatisierung oder Benutzeroberfläche Pfade, die nicht der Seitenname, beispielsweise den Befehl " **Drucken** " enthalten. 
  
 Diese Zelle kann nur für Dokumentseiten verwendet werden, nicht aber für Markupüberlagerungsseiten, deren Zelle UIVisibility standardmäßig auf visUIVHidden festgelegt ist und nicht geändert werden darf. 
  
> [!NOTE]
> Um eine Seite des Dokuments **Drucken** Befehl ausblenden möchten, können sie ein Hintergrundblatt (**Type** -Eigenschaft ist **VisTypeBackground** ), die nicht als Hintergrund jeder Seite (Shapes auf Seiten gedruckt werden, wenn eine Seite mit es als Hintergrund Hintergrund verwendet wird gedruckt). Befehl **Drucken** des Dokuments funktioniert nur für indizierte Seiten und Hintergrundblätter werden nicht indiziert. 
  
Wenn Sie einen Verweis auf die Zelle UIVisibility aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |UIVisibility  <br/> |
   
Wenn Sie einen Verweis auf die Zelle UIVisibility aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageUIVisibility** <br/> |
   

