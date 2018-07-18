---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Legt fest, ob ein Dokument gespeichert, die auf einem Microsoft SharePoint 2013-Server oder Microsoft OneDrive von mehreren Autoren gleichzeitig in einer Sitzung beim Entwicklersupport bearbeitet werden kann.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797548"
---
# <a name="nocoauth-cell-document-properties-section"></a>NoCoauth Cell (Document Properties Section)

Legt fest, ob ein Dokument gespeichert, die auf einem Microsoft SharePoint 2013-Server oder Microsoft OneDrive von mehreren Autoren gleichzeitig in einer Sitzung beim Entwicklersupport bearbeitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Dokument kann nicht Mitautor werden und für die Bearbeitung beim Öffnen gesperrt ist.  <br/> |
|FALSE  <br/> |Das Dokument kann Mitautor sein.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **NoCoauth** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NoCoauth  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **NoCoauth** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocNoCoauth** <br/> |
   

