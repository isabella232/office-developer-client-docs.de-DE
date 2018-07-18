---
title: Informationen zu anzeigebenachrichtigungen-Tabelle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a696357c97a85442bbfd5532892c06d570f6367c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791222"
---
# <a name="about-display-table-notifications"></a>Informationen zu anzeigebenachrichtigungen-Tabelle

**Betrifft**: Outlook 
  
Benachrichtigungen für eine Tabelle angezeigt werden vom verantwortlich für die Erstellung der Tabelle anzeigen, um MAPI-Dienstanbieter gesendet. Für diese Benachrichtigungen werden MAPI durch eine Anzeige Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode aufrufen und das geänderte Tabelle-Ereignis registriert. 
  
Wie bei allen Tabelle Benachrichtigungen enthalten anzeigebenachrichtigungen Tabelle eine [TABLE_NOTIFICATION](table_notification.md) Struktur. Nur die **UlTableEvent** und die **PropIndex** Mitglieder dieser Struktur werden berücksichtigt. die anderen Mitglieder werden ignoriert. Der **UlTableEvent** Member auf TABLE_ROW_MODIFIED festgelegt ist, und der **PropIndex** Member wird auf den Wert der Spalte **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) in der entsprechenden Zeile festgelegt. MAPI antwortet auf die Benachrichtigung durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode für die Eigenschaft, die im Steuerelement angezeigt werden und den neuen Wert angezeigt. 
  
Tabelle anzeigebenachrichtigungen können von einem Dienstanbieter zur Koordinierung von Änderungen an verwandter Steuerelemente im Dialogfeld verwendet werden. Beispiel: bei der Implementierung der Eigenschaft muss auf einem oder mehreren Feldern im Dialogfeld refresh – vielleicht als Antwort auf ein anderes Steuerelement, das das Flag DT_SET_IMMEDIATE in seiner **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))-Eigenschaft festgelegt wurde – Sie können eine Benachrichtigung über eine Anzeige Tabelle generieren. Die Implementierung der Eigenschaft-Schnittstelle, die aufgrund einer Änderung abgelesen werden der Wert der ein oder mehrere Steuerelemente muss oder ein externes Ereignis auftritt, kann eine Benachrichtigung über eine Anzeige Tabelle warnen. 
  
Ein Dienstanbieter kann Tabelle anzeigebenachrichtigungen durch ausgeben:
  
- Aufrufen von [ITableData::HrNotify](itabledata-hrnotify.md), wenn die Anzeige-Tabelle mit einem Table-Datenobjekt erstellt wurde.
    
    - Oder -
    
- Verwenden ihren eigenen Code, wenn mit der Anbieter **IMAPITable** Implementierung die Anzeige-Tabelle erstellt wurde. 
    
MAPI antwortet Tabelle Benachrichtigungen bei Bedarf Anzeige durch erneutes Lesen den Wert eines Steuerelements aus der Eigenschaft schnittstellenimplementierung. In der folgenden Tabelle werden die Details rund um die Behandlung von Benachrichtigungen für bestimmte Typen von Steuerelementen in MAPI beschrieben.
  
|**Control**|**MAPI-Aktion**|
|:-----|:-----|
|Schaltfläche  <br/> |Ruft die [IMAPIProp::OpenProperty](imapiprop-openproperty.md)zum Abrufen des Control-Objekts über die Eigenschaft vom **UlPRControl** Member der Struktur [DTBLBUTTON](dtblbutton.md) dargestellt werden, wenn der Anruf zuvor fehlgeschlagenen hatte. Ruft das Control-Objekt [IMAPIControl::GetState](imapicontrol-getstate.md) , um zu bestimmen, ob die Schaltfläche aktiviert werden soll und aktiviert oder die Schaltfläche entsprechend deaktiviert an.  <br/> |
|Kontrollkästchen  <br/> |Liest den Wert für den **UlPRPropertyName** Member bei.  <br/> |
|Kombinationsfeld  <br/> |Öffnet die Tabelle, die dem **UlPRTableName** Member der Struktur [DTBLCOMBOBOX](dtblcombobox.md) zugeordnet. Liest bei allen Zeilen, einschließlich des Werts für den **UlPRPropertyName**-Member.  <br/> |
|Dropdown-Listenfeld  <br/> |Öffnet die Tabelle, die dem **UlPRTableName** Member der Struktur [DTBLDDLBX](dtblddlbx.md) zugeordnet und liest bei allen Zeilen. Ruft die [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen der Werte für die Eigenschaften in die **UlPRDisplayProperty** und die **UlPRSetProperty** Elemente gespeichert.  <br/> |
|Bearbeiten  <br/> |Liest die Eigenschaft bei, und wird erneut angezeigt.  <br/> |
|Gruppenfeld  <br/> |Die Benachrichtigung wird ignoriert.  <br/> |
|Beschriftung  <br/> |Die Benachrichtigung wird ignoriert.  <br/> |
|Mehrfachauswahl-Listenfeld  <br/> |Wenn eine der Spalten eine Eintrags-ID ist, aktualisiert das Listenfeld. Das entsprechende Objekt ist nicht geschlossen oder erneut geladen.  <br/> |
|Einfachauswahl Listenfeld  <br/> |Liest die Set-Eigenschaft, versucht er zu identifizieren.  <br/> |
|Mehrwertiges Listenfeld  <br/> |Liest die Eigenschaft bei, und das Listenfeld zugewiesen.  <br/> |
|Seite mit Registerkarten  <br/> |Es gibt keine Benachrichtigungen für dieses Steuerelement. Alles ist statisch.  <br/> |
|Optionsfeld  <br/> |Liest die Eigenschaft, die die Schaltfläche zugeordnet ist und in der **UlPropTag** -Member der Struktur [DTBLRADIOBUTTON](dtblradiobutton.md) gespeichert ist und stellt die entsprechende Auswahl mit den Steuerelementen bei.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

