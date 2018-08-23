---
title: Anzeigen von Tabellenzeilen und-spalten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dba7bd1fb7b0ca9bc23dbc45e07f44d0cc0dc8fe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568140"
---
# <a name="displaying-table-rows-and-columns"></a>Anzeigen von Tabellenzeilen und-spalten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 Eine Eigenschaftenseite kann durch Benutzer neue e-Mail-Empfängern definieren vom Adressbuch-Dienstanbieter verwendet werden. 
  
Die entsprechenden zeigt die Tabelle enthält die vier Zeilen, eine für jedes Steuerelement. Die Werte für die Spalten, die Position angeben, sind wie folgt.
  
|**Control**|**XPOS**|**YPOS DARGESTELLT WERDEN**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Bezeichnung anzeigen  <br/> |14  <br/> |18  <br/> |49  <br/> |8  <br/> |
|Feld Anzeigename bearbeiten  <br/> |76  <br/> |16  <br/> |89  <br/> |12  <br/> |
|E-Mail-Adressetikett  <br/> |14  <br/> |42  <br/> |50  <br/> |8  <br/> |
|Bearbeitungsfeld für e-Mail-Adresse  <br/> |76  <br/> |40  <br/> |89  <br/> |12  <br/> |
|Kontrollkästchen  <br/> |14  <br/> |64  <br/> |90  <br/> |12  <br/> |
   
In der nächsten Tabelle schlägt geeignete Werte für den Typ des Steuerelements, dessen **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))-Eigenschaft und die Bitmaske aus Flags, dessen **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))-Eigenschaft.
  
|**Control**|**Typ**|**Flags**|
|:-----|:-----|:-----|
|Bezeichnung anzeigen  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Feld Anzeigename bearbeiten  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|E-Mail-Adressetikett  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Bearbeitungsfeld für e-Mail-Adresse  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Kontrollkästchen  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
Die endgültige Tabelle enthält jedes Steuerelement mit dem Inhalt der zugeordneten Steuerelements-Struktur. Beachten Sie, dass der Wert für jede der Label-Steuerelemente im Arbeitsspeicher, die unmittelbar auf der Struktur angezeigt wird.
  
|**Control**|**Structure**|
|:-----|:-----|
|Bezeichnung anzeigen  <br/> |{sizeof(DTBLLABEL), 0} "Anzeigename:"  <br/> |
|Feld Anzeigename bearbeiten  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|E-Mail-Adressetikett  <br/> |{sizeof(DTBLLABEL), 0} "E-Mail-Adresse:"  <br/> |
|Bearbeitungsfeld für e-Mail-Adresse  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Kontrollkästchen  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Die Schaltflächen **OK**, **Abbrechen**und **Hilfe** sind nicht in der Tabelle anzeigen enthalten. Die Benutzeroberfläche kann Kontext zu einem Dialogfeld hinzufügen, durch Hinzufügen von Steuerelementen nicht in der Tabelle anzeigen. 
  
## <a name="see-also"></a>Siehe auch



[Anzeigen der Tabellenimplementierung](display-table-implementation.md)

