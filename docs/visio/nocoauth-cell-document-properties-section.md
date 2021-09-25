---
title: Zelle "NoCoauth" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Legt fest, ob ein auf einem Microsoft SharePoint 2013-Server gespeichertes Dokument oder Microsoft OneDrive gleichzeitig von mehreren Autoren in einer Sitzung für die gemeinsame Dokumenterstellung bearbeitet werden kann.
ms.openlocfilehash: 505617992f2a35e0603ed676b1e6dcb1fa1b5511
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562972"
---
# <a name="nocoauth-cell-document-properties-section"></a>Zelle "NoCoauth" (Abschnitt "Document Properties")

Legt fest, ob ein auf einem Microsoft SharePoint 2013-Server gespeichertes Dokument oder Microsoft OneDrive gleichzeitig von mehreren Autoren in einer Sitzung für die gemeinsame Dokumenterstellung bearbeitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Dokument kann nicht gemeinsam erstellt werden und ist beim Öffnen für die Bearbeitung gesperrt.  <br/> |
|FALSE  <br/> |Das Dokument kann gemeinsam erstellt werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "NoCoauth"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NoCoauth  <br/> |
   
Um einen Verweis auf die Zelle **"NoCoauth"** anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocNoCoauth** <br/> |
   

