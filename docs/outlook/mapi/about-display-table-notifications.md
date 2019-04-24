---
title: Informationen zu Benachrichtigungen für Anzeigetabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 41e6a2c8b6856bf072972325e7e08aabe3e17446
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326411"
---
# <a name="about-display-table-notifications"></a>Informationen zu Benachrichtigungen für Anzeigetabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigungen für eine Anzeigetabelle werden von dem Dienstanbieter gesendet, der für die Erstellung der Anzeigetabelle in MAPI zuständig ist. MAPI registriert diese Benachrichtigungen, indem die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Display-Tabelle aufgerufen und das Table modified-Ereignis angegeben wird. 
  
Wie bei allen Tabellen Benachrichtigungen, enthält die Anzeige Tabellen Benachrichtigungen eine [TABLE_NOTIFICATION](table_notification.md) -Struktur. Nur die **ulTableEvent** -und die **propIndex** -Elemente dieser Struktur sind erheblich; die anderen Elemente werden ignoriert. Das **ulTableEvent** -Element wird auf TABLE_ROW_MODIFIED festgelegt, und das **propIndex** -Element wird auf den Wert der **PR_CONTROL_ID** ([pidtagcontrolid (](pidtagcontrolid-canonical-property.md))-Spalte in der entsprechenden Zeile festgelegt. MAPI reagiert auf die Benachrichtigung durch Aufrufen der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode für die im Steuerelement angezeigte Eigenschaft und durch Anzeigen des neuen Werts. 
  
Anzeige Tabellen Benachrichtigungen können von einem Dienstanbieter verwendet werden, um Änderungen an verwandten Steuerelementen im Dialogfeld zu koordinieren. Wenn die Implementierung der Eigenschaften Schnittstelle beispielsweise ein oder mehrere Felder im Dialogfeld aktualisieren muss, möglicherweise als Reaktion auf ein anderes Steuerelement, das das DT_SET_IMMEDIATE-Flag in seiner **PR_CONTROL_FLAGS** ([pidtagcontrolflags (](pidtagcontrolflags-canonical-property.md))-Eigenschaft festgelegt hat, Es kann eine Anzeige Tabellenbenachrichtigung generieren. Eine Anzeige Tabellenbenachrichtigung kann die Eigenschaften Schnittstellenimplementierung Benachrichtigen, dass der Wert eines oder mehrerer Steuerelemente aufgrund einer Änderung oder eines externen Ereignisses erneut gelesen werden muss. 
  
Ein Dienstanbieter kann Anzeige Tabellen Benachrichtigungen ausgeben, indem er:
  
- Aufrufen von [ITableData:: HrNotify](itabledata-hrnotify.md), wenn die Anzeigetabelle mit einem Tabellendaten Objekt erstellt wurde.
    
    - Oder
    
- Verwenden des eigenen Codes, wenn die Anzeigetabelle mit der **IMAPITable** -Implementierung des Anbieters erstellt wurde. 
    
MAPI reagiert auf Anzeige von Tabellen Benachrichtigungen, wenn dies erforderlich ist, indem der Wert eines Steuerelements aus der Eigenschaften Schnittstellenimplementierung erneut gelesen wird. In der folgenden Tabelle werden die Details zur Behandlung von Benachrichtigungen für bestimmte Steuerelementtypen beschrieben.
  
|**Control**|**MAPI-Aktion**|
|:-----|:-----|
|Schaltfläche  <br/> |Ruft [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)auf, um das Control-Objekt mithilfe der vom **ulPRControl** -Element der [DTBLBUTTON](dtblbutton.md) -Struktur dargestellten Eigenschaft abzurufen, wenn der Aufruf zuvor fehlgeschlagen war. Ruft das [IMAPIControl:: GetState](imapicontrol-getstate.md) des Control-Objekts auf, um zu bestimmen, ob die Schaltfläche aktiviert werden soll, und aktiviert oder deaktiviert die Schaltfläche entsprechend.  <br/> |
|Kontrollkästchen  <br/> |Liest den Wert für das **ulPRPropertyName** -Element erneut.  <br/> |
|Kombinationsfeld  <br/> |Öffnet die Tabelle, die dem **ulPRTableName** -Element der [DTBLCOMBOBOX](dtblcombobox.md) -Struktur zugeordnet ist, erneut. Liest alle Zeilen einschließlich des Werts für das **ulPRPropertyName**-Element erneut.  <br/> |
|Dropdown-Listenfeld  <br/> |Öffnet die Tabelle, die dem **ulPRTableName** -Element der [DTBLDDLBX](dtblddlbx.md) -Struktur zugeordnet ist, und liest alle Zeilen erneut. Ruft [IMAPIProp::](imapiprop-getprops.md) GetProps auf, um die Werte für die Eigenschaften abzurufen, die in den **UlPRDisplayProperty** -und **ulPRSetProperty** -Elementen gespeichert sind.  <br/> |
|Bearbeiten  <br/> |Die Eigenschaft wird erneut gelesen und erneut angezeigt.  <br/> |
|Gruppenfeld  <br/> |Die Benachrichtigung wird ignoriert.  <br/> |
|Label  <br/> |Die Benachrichtigung wird ignoriert.  <br/> |
|Listenfeld für Mehrfachauswahl  <br/> |Wenn eine der Spalten eine Eintrags-ID ist, wird das Listenfeld aktualisiert. Das entsprechende Objekt wird nicht geschlossen oder erneut geladen.  <br/> |
|Einzelauswahl-Listenfeld  <br/> |Liest die Set-Eigenschaft und versucht, Sie zu identifizieren.  <br/> |
|Mehrwertiges Listenfeld  <br/> |Liest die Eigenschaft erneut ein und füllt das Listenfeld erneut auf.  <br/> |
|Registerkartenseite  <br/> |Es sind keine Benachrichtigungen für dieses Steuerelement vorhanden; Alles ist statisch.  <br/> |
|Optionsfeld  <br/> |Liest die Eigenschaft, die der Schaltfläche zugeordnet ist und im **ulPropTag** -Element der [DTBLRADIOBUTTON](dtblradiobutton.md) -Struktur gespeichert ist, und trifft die entsprechende Auswahl mit den Steuerelementen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

