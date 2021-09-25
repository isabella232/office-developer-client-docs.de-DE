---
title: Anzeigen von Tabellenzeilen und -spalten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6b029383bf4287596ac6d03ee4e5f2861eff4053
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605006"
---
# <a name="displaying-table-rows-and-columns"></a>Anzeigen von Tabellenzeilen und -spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Eine Eigenschaftenseite kann von einem Adressbuchanbieter verwendet werden, um Benutzern das Definieren neuer E-Mail-Empfänger zu ermöglichen. 
  
Die entsprechende Anzeigetabelle enthält vier Zeilen, eine für jedes Steuerelement. Die Werte für die Spalten, die die Position angeben, sind wie folgt.
  
|**Control**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Anzeigenamenbeschriftung  <br/> |14   <br/> |18   <br/> |49  <br/> |8   <br/> |
|Anzeigenamen-Bearbeitungsfeld  <br/> |76  <br/> |16   <br/> |89  <br/> |12   <br/> |
|E-Mail-Adressbezeichnung  <br/> |14   <br/> |42  <br/> |50  <br/> |8   <br/> |
|Bearbeitungsfeld für E-Mail-Adresse  <br/> |76  <br/> |40  <br/> |89  <br/> |12   <br/> |
|Kontrollkästchen  <br/> |14   <br/> |64  <br/> |90  <br/> |12   <br/> |
   
In dieser nächsten Tabelle werden die entsprechenden Werte für den Typ des Steuerelements, die **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) -Eigenschaft und die Bitmaske von Flags, die **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) -Eigenschaft vorgeschlagen.
  
|**Control**|**Typ**|**Flags**|
|:-----|:-----|:-----|
|Anzeigenamenbeschriftung  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Anzeigenamen-Bearbeitungsfeld  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|E-Mail-Adressbezeichnung  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Bearbeitungsfeld für E-Mail-Adresse  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Kontrollkästchen  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
In der endgültigen Tabelle sind die einzelnen Steuerelemente mit dem Inhalt der zugehörigen Steuerelementstruktur aufgeführt. Beachten Sie, dass der Wert für jedes der Bezeichnungssteuerelemente direkt nach der Struktur im Speicher angezeigt wird.
  
|**Control**|**Structure**|
|:-----|:-----|
|Anzeigenamenbeschriftung  <br/> |{sizeof(DTBLLABEL), 0} "Anzeigename:"  <br/> |
|Anzeigenamen-Bearbeitungsfeld  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|E-Mail-Adressbezeichnung  <br/> |{sizeof(DTBLLABEL), 0} "E-Mail-Adresse:"  <br/> |
|Bearbeitungsfeld für E-Mail-Adresse  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Kontrollkästchen  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Die Schaltflächen **OK,** **Abbrechen** und **Hilfe** sind nicht in der Anzeigetabelle enthalten. Die Benutzeroberfläche kann einem Dialogfeld Kontext hinzufügen, indem Steuerelemente hinzugefügt werden, die nicht in der Anzeigetabelle enthalten sind. 
  
## <a name="see-also"></a>Siehe auch



[Implementierung von Anzeigetabellen](display-table-implementation.md)

