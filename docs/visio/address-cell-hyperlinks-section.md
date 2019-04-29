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
  
Sie können die Adresse als relativen Pfad basierend auf dem Basis Pfad angeben, der für das Dokument im **** Feld Hyperlinkbasis auf der Registerkarte **Zusammenfassung** des Dialogfelds **Eigenschaften** festgelegt ist (Klicken Sie auf die Registerkarte **Datei** , dann auf **Info**und dann auf * * Eigenschaften * * , und klicken Sie dann auf **Erweiterte Eigenschaften**). Wenn das Dokument keinen Basispfad aufweist, navigiert die Anwendung auf Grundlage des Dokumentpfads. Wenn das Dokument noch nicht gespeichert wurde, bleibt der Hyperlink undefiniert.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert der Zelle Adresse auch im Dialogfeld **Hyperlinks** festlegen (Klicken Sie auf der Registerkarte **Einfügen** auf **Hyperlink** ). 
  
Wenn Sie einen Verweis auf die Zelle address aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name* . Adresse, an der Hyperlink. *Name* ist der Name der Hyperlink-Zeile.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle address aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkAddress** <br/> |
   

