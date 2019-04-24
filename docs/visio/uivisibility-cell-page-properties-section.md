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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357218"
---
# <a name="uivisibility-cell-page-properties-section"></a>Zelle "UIVisibility" (Abschnitt "Page Properties")

Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Der Seitenname wird in der Benutzeroberfläche angezeigt (Standardwert).  <br/> |**visUIVNormal** <br/> |
|1  <br/> |Der Seitenname wird nicht in der Benutzeroberfläche angezeigt.  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Festlegen der "UIVisibility-Zelle auf **visUIVHidden** verhindert, dass die Seite an einer beliebigen Stelle in der Benutzeroberfläche angezeigt wird, auf der die Zeichenfolge mit dem Seitennamen angezeigt wird. Die Seite wäre beispielsweise nicht als Option im **Zeichnungs-Explorer** oder auf den Seitenregisterkarten aufgeführt. Auf die Seite kann jedoch zugegriffen werden, wenn Sie Automatisierungs-oder UI-Pfade verwenden, die nicht den Seitennamen, beispielsweise den **Druck** Befehl, aufweisen. 
  
 Diese Zelle ist für die Verwendung mit Dokumentseiten vorgesehen. Es ist nicht für die Verwendung mit Markup Überlagerungs Seiten vorgesehen, bei denen die "UIVisibility-Zelle standardmäßig auf **visUIVHidden** festgelegt ist und nicht geändert werden sollte. 
  
> [!NOTE]
> Wenn Sie eine Seite aus dem **Druck** Befehl des Dokuments ausblenden möchten, legen Sie Sie als Hintergrundseite fest (**Type** -Eigenschaft ist **visTypeBackground** ), die von keiner Seite als Hintergrund verwendet wird (Shapes auf Hintergrundseiten werden gedruckt, wenn eine Seite, die es als Hintergrund verwendet, gedruckt). Der **Druck** Befehl des Dokuments funktioniert nur mit indizierten Seiten, und Hintergrundseiten werden nicht indiziert. 
  
Wenn Sie einen Verweis auf die Zelle "UIVisibility aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |"UIVisibility  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "UIVisibility aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageUIVisibility** <br/> |
   

