---
title: Zelle "NoCoauth" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Legt fest, ob ein auf einem Microsoft SharePoint 2013-Server oder Microsoft OneDrive gespeichertes Dokument von mehreren Autoren gleichzeitig in einer Gemeinsamen Dokumentautorisierungssitzung bearbeitet werden kann.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420514"
---
# <a name="nocoauth-cell-document-properties-section"></a>Zelle "NoCoauth" (Abschnitt "Document Properties")

Legt fest, ob ein auf einem Microsoft SharePoint 2013-Server oder Microsoft OneDrive gespeichertes Dokument von mehreren Autoren gleichzeitig in einer Gemeinsamen Dokumentautorisierungssitzung bearbeitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Dokument kann nicht gemeinsam authentifiziert werden und ist beim Öffnen für die Bearbeitung gesperrt.  <br/> |
|FALSE  <br/> |Das Dokument kann gemeinsam authentifiziert werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle NoCoauth** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NoCoauth  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle NoCoauth** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocNoCoauth** <br/> |
   

