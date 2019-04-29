---
title: NoCoauth Cell (Document Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Legt fest, ob ein auf einem Microsoft SharePoint 2013-Server oder einem Microsoft OneDrive gespeichertes Dokument von mehreren Autoren gleichzeitig in einer gemeinsamen Sitzung bearbeitet werden kann.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420514"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth Cell (Document Properties section)

Legt fest, ob ein auf einem Microsoft SharePoint 2013-Server oder einem Microsoft OneDrive gespeichertes Dokument von mehreren Autoren gleichzeitig in einer gemeinsamen Sitzung bearbeitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Dokument kann nicht gemeinsam erstellt werden und ist für die Bearbeitung gesperrt, wenn es geöffnet wird.  <br/> |
|FALSE  <br/> |Das Dokument kann gemeinsam erstellt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **NoCoauth** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NoCoauth  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **NoCoauth** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocNoCoauth** <br/> |
   

