---
title: Zelle "Address" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
ms.localizationpriority: medium
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.
ms.openlocfilehash: ef893335b25fb400cbfc1f153a3fcdcd7a66be02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578291"
---
# <a name="address-cell-hyperlinks-section"></a>Zelle "Address" (Abschnitt "Hyperlinks")

Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.
  
Sie können Address als relativen Pfad basierend auf dem Basispfad angeben, der für das Dokument im **Hyperlink-Basisfeld** auf der Registerkarte **"Zusammenfassung"** des Dialogfelds **"Eigenschaften"** definiert ist (klicken Sie auf die Registerkarte **"Datei",** klicken Sie auf **"Info",** klicken Sie auf **Eigenschaften **, und klicken Sie dann auf **"Erweiterte Eigenschaften").** Wenn das Dokument keinen Basispfad aufweist, navigiert die Anwendung basierend auf dem Dokumentpfad. Wenn das Dokument noch nicht gespeichert wurde, bleibt der Hyperlink undefiniert.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert der Zelle  Address auch im Dialogfeld Hyperlinks festlegen (klicken Sie auf der Registerkarte Einfügen auf Hyperlink).   
  
Um einen Verweis auf die Zelle Address anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name*  . Adresse, an der hyperlink. *Name*  ist der Name der Hyperlinkzeile  <br/> |
   
Verwenden Sie zum Abrufen eines Verweises auf die Zelle Address anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkAddress** <br/> |
   

