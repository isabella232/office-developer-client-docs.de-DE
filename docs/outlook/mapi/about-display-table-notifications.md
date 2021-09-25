---
title: Informationen zu Benachrichtigungen für Anzeigetabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 582e970e3a31c6a3da9c96569f7a3c98b795c7eb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551947"
---
# <a name="about-display-table-notifications"></a>Informationen zu Benachrichtigungen für Anzeigetabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigungen in einer Anzeigetabelle werden von dem Dienstanbieter gesendet, der für das Erstellen der Anzeigetabelle an die MAPI verantwortlich ist. MAPI registriert sich für diese Benachrichtigungen, indem die [IMAPITable::Advise-Methode](imapitable-advise.md) einer Anzeigetabelle aufgerufen und das Tabellenänderungsereignis angegeben wird. 
  
Wie bei allen Tabellenbenachrichtigungen enthalten die Anzeigetabellenbenachrichtigungen eine [TABLE_NOTIFICATION](table_notification.md) Struktur. Nur die **ulTableEvent-** und **propIndex-Elemente** dieser Struktur sind von Bedeutung. die anderen Member werden ignoriert. Der **ulTableEvent-Member** wird auf TABLE_ROW_MODIFIED und das **propIndex-Element** auf den Wert der **Spalte PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) in der entsprechenden Zeile festgelegt. MAPI antwortet auf die Benachrichtigung, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) für die im Steuerelement angezeigte Eigenschaft aufgerufen und der neue Wert angezeigt wird. 
  
Anzeigetabellenbenachrichtigungen können von einem Dienstanbieter verwendet werden, um Änderungen an verwandten Steuerelementen im Dialogfeld zu koordinieren. Wenn die Implementierung der Eigenschaftenschnittstelle beispielsweise ein oder mehrere Felder im Dialogfeld aktualisieren muss , z. B. als Reaktion auf ein anderes Steuerelement, das das DT_SET_IMMEDIATE-Flag in seiner **PR_CONTROL_FLAGS** -Eigenschaft ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) festgelegt hat, kann eine Anzeigetabellenbenachrichtigung generiert werden. Eine Anzeigetabellenbenachrichtigung kann die Implementierung der Eigenschaftenschnittstelle darauf hinweisen, dass der Wert eines oder mehrerer Steuerelemente aufgrund einer Änderung oder eines externen Ereignisses erneut gelesen werden muss. 
  
Ein Dienstanbieter kann Anzeigetabellenbenachrichtigungen ausstellen:
  
- Aufrufen von [ITableData::HrNotify](itabledata-hrnotify.md), wenn die Anzeigetabelle mit einem Tabellendatenobjekt erstellt wurde.
    
    - Oder -
    
- Verwenden Sie einen eigenen Code, wenn die Anzeigetabelle mit der **IMAPITable-Implementierung** des Anbieters erstellt wurde. 
    
MAPI reagiert bei Bedarf auf die Anzeige von Tabellenbenachrichtigungen, indem der Wert eines Steuerelements aus der Implementierung der Eigenschaftenschnittstelle erneut gelesen wird. In der folgenden Tabelle werden die Details zur Behandlung von MAPI-Benachrichtigungen für bestimmte Steuerelementtypen beschrieben.
  
|**Control**|**MAPI-Aktion**|
|:-----|:-----|
|Schaltfläche  <br/> |Calls [IMAPIProp::OpenProperty](imapiprop-openproperty.md)to retrieve the control object by way of the property represented by the **ulPRControl** member of the [DTBLBUTTON](dtblbutton.md) structure if the call had failed previously. Ruft das IMAPIControl-Steuerelement des Steuerelementobjekts [auf::GetState,](imapicontrol-getstate.md) um zu bestimmen, ob die Schaltfläche aktiviert werden soll, und aktiviert oder deaktiviert die Schaltfläche entsprechend.  <br/> |
|Kontrollkästchen  <br/> |Liest den Wert für den **ulPRPropertyName-Member** neu.  <br/> |
|Kombinationsfeld  <br/> |Öffnet die Tabelle erneut, die dem **ulPRTableName-Element** der [DTBLCOMBOBOX-Struktur](dtblcombobox.md) zugeordnet ist. Rereads all of the rows including the value for the **ulPRPropertyName** member.  <br/> |
|Dropdown-Listenfeld  <br/> |Öffnet die Tabelle erneut, die dem **ulPRTableName-Element** der [DTBLDDLBX-Struktur](dtblddlbx.md) zugeordnet ist, und liest alle Zeilen neu. Ruft [IMAPIProp::GetProps](imapiprop-getprops.md) auf, um die Werte für die in den **UlPRDisplayProperty-** und **ulPRSetProperty-Membern** gespeicherten Eigenschaften abzurufen.  <br/> |
|Bearbeiten  <br/> |Liest die Eigenschaft neu und zeigt sie erneut an.  <br/> |
|Gruppenfeld  <br/> |Ignoriert die Benachrichtigung.  <br/> |
|Beschriftung  <br/> |Ignoriert die Benachrichtigung.  <br/> |
|Mehrfachauswahl-Listenfeld  <br/> |Wenn eine der Spalten ein Eintragsbezeichner ist, wird das Listenfeld aktualisiert. Das entsprechende Objekt wird nicht geschlossen oder neu geladen.  <br/> |
|Listenfeld "Einzelne Auswahl"  <br/> |Liest die set-Eigenschaft und versucht, sie zu identifizieren.  <br/> |
|Mehrwertiges Listenfeld  <br/> |Liest die Eigenschaft neu und fügt das Listenfeld erneut ein.  <br/> |
|Registerkartenseite  <br/> |Es gibt keine Benachrichtigungen für dieses Steuerelement; alles ist statisch.  <br/> |
|Optionsfeld  <br/> |Rereads the property that is associated with the button and is stored in the **ulPropTag** member of the [DTBLRADIOBUTTON](dtblradiobutton.md) structure and makes the appropriate selection with the controls.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

