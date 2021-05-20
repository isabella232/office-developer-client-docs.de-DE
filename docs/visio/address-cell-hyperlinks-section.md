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
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438036"
---
# <a name="address-cell-hyperlinks-section"></a>Zelle "Address" (Abschnitt "Hyperlinks")

Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.
  
Sie können Address als relativen Pfad basierend auf dem Basispfad angeben,  der für  das Dokument im  **Feld Hyperlinkbasis** auf der Registerkarte Zusammenfassung des Dialogfelds Eigenschaften definiert ist (klicken Sie auf die Registerkarte Datei, klicken Sie auf **Info,** klicken Sie auf ** Eigenschaften **, und klicken Sie dann auf **Erweiterte Eigenschaften**). Wenn das Dokument keinen Basispfad hat, navigiert die Anwendung basierend auf dem Dokumentpfad. Wenn das Dokument noch nicht gespeichert wurde, bleibt der Hyperlink undefiniert.
  
## <a name="remarks"></a>Hinweise

Sie können auch den Wert der Zelle Address im Dialogfeld  **Hyperlinks** festlegen (klicken Sie auf der Registerkarte Einfügen auf **Hyperlink).** 
  
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Address nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name*  . Adresse, an der Hyperlink angezeigt wird. *Name*  ist der Name der Hyperlinkzeile  <br/> |
   
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Address anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkAddress** <br/> |
   

