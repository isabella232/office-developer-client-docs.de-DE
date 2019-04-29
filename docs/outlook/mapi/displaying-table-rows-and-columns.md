---
title: Anzeigen von Tabellenzeilen und-Spalten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9f1cc0bebf3c90a5c12f2714e8ab7eea59104da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407116"
---
# <a name="displaying-table-rows-and-columns"></a>Anzeigen von Tabellenzeilen und-Spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Eine Eigenschaftenseite kann von einem Adressbuchanbieter verwendet werden, um Benutzern das Definieren neuer e-Mail-Empfänger zu ermöglichen. 
  
Die entsprechende Anzeigetabelle enthält vier Zeilen, eine für jedes Steuerelement. Die Werte für die Spalten, die die Position anzeigen, lauten wie folgt.
  
|**Control**|**XPOS**|**YPOS**|**DELTAX**|**DELTAy**|
|:-----|:-----|:-----|:-----|:-----|
|Bezeichnung für Anzeigename  <br/> |14   <br/> |18  <br/> |49  <br/> |8  <br/> |
|Anzeigename-Bearbeitungsfeld  <br/> |76  <br/> |16   <br/> |89  <br/> |12  <br/> |
|E-Mail-Adress Bezeichnung  <br/> |14   <br/> |42  <br/> |50  <br/> |8  <br/> |
|E-Mail-Adresse-Bearbeitungsfeld  <br/> |76  <br/> |40  <br/> |89  <br/> |12  <br/> |
|Kontrollkästchen  <br/> |14   <br/> |64  <br/> |90  <br/> |12  <br/> |
   
In der folgenden Tabelle werden die entsprechenden Werte für den Typ des Steuerelements, dessen **PR_CONTROL_TYPE** ([pidtagcontroltype (](pidtagcontroltype-canonical-property.md)) und die Bitmaske der Flags, dessen **PR_CONTROL_FLAGS** ([pidtagcontrolflags (](pidtagcontrolflags-canonical-property.md))-Eigenschaft vorgeschlagen.
  
|**Control**|**Type**|**Flags**|
|:-----|:-----|:-----|
|Bezeichnung für Anzeigename  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Anzeigename-Bearbeitungsfeld  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|E-Mail-Adress Bezeichnung  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|E-Mail-Adresse-Bearbeitungsfeld  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Kontrollkästchen  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
In der letzten Tabelle sind die einzelnen Steuerelemente mit dem Inhalt der zugehörigen Steuerelementstruktur aufgeführt. Beachten Sie, dass der Wert für jedes Label-Steuerelement im Arbeitsspeicher direkt nach der Struktur angezeigt wird.
  
|**Control**|**Structure**|
|:-----|:-----|
|Bezeichnung für Anzeigename  <br/> |{sizeof (DTBLLABEL), 0} "Anzeigename:"  <br/> |
|Anzeigename-Bearbeitungsfeld  <br/> |{sizeof (DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|E-Mail-Adress Bezeichnung  <br/> |{sizeof (DTBLLABEL), 0} "E-Mail-Adresse:"  <br/> |
|E-Mail-Adresse-Bearbeitungsfeld  <br/> |{sizeof (DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Kontrollkästchen  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Die Schaltflächen **OK**, **Abbrechen**und **Hilfe** sind nicht in der Anzeigetabelle enthalten. Die Benutzeroberfläche kann einem Dialogfeld Kontext hinzufügen, indem Sie Steuerelemente hinzufügen, die nicht in der Anzeigetabelle enthalten sind. 
  
## <a name="see-also"></a>Siehe auch



[Anzeigen der Tabellen Implementierung](display-table-implementation.md)

