---
title: Zelle "Address" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796403"
---
# <a name="address-cell-hyperlinks-section"></a>Address Cell (Hyperlinks Section)

Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.
  
Sie können eine Adresse angeben, wie ein relativer Pfad basierend auf der Basispfad für das Dokument in das Feld **Hyperlinkbasis** auf der Registerkarte **Zusammenfassung** des Dialogfelds **Eigenschaften** definiert (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Info**, klicken Sie auf ** Eigenschaften ** und klicken Sie dann auf **Erweiterte Eigenschaften**). Wenn das Dokument keinen Basispfad verfügt, navigiert die Anwendung basierend auf den Dokumentpfad. Wenn das Dokument nicht gespeichert wurde, ist der Hyperlink nicht definiert.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert der Zelle Address auch im Dialogfeld Hyperlinks festlegen (klicken Sie auf der Registerkarte Einfügen auf Hyperlink). 
  
Wenn Sie einen Bezug auf die Zelle Address aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name* . Beheben von Where Hyperlink. *ist der Name der Hyperlinkzeile*  <br/> |
   
Zum Abrufen eines Verweises auf die Zelle Address nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkAddress** <br/> |
   

