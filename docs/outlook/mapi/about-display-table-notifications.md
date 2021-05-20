---
title: Informationen zu Benachrichtigungen für Anzeigetabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 41e6a2c8b6856bf072972325e7e08aabe3e17446
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430014"
---
# <a name="about-display-table-notifications"></a>Informationen zu Benachrichtigungen für Anzeigetabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigungen in einer Anzeigetabelle werden vom Dienstanbieter gesendet, der für das Erstellen der Anzeigetabelle an MAPI zuständig ist. MAPI registriert diese Benachrichtigungen, indem die [IMAPITable::Advise-Methode](imapitable-advise.md) einer Anzeigetabelle aufruft und das Table Modified-Ereignis angegeben wird. 
  
Wie bei allen Tabellenbenachrichtigungen enthalten Anzeigetabelle Benachrichtigungen eine [TABLE_NOTIFICATION](table_notification.md) Struktur. Nur die **ulTableEvent-** und **propIndex-Elemente** dieser Struktur sind signifikant. die anderen Mitglieder werden ignoriert. Das **element ulTableEvent** wird auf TABLE_ROW_MODIFIED und das **element propIndex** auf den Wert der **Spalte PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) in der entsprechenden Zeile festgelegt. MAPI antwortet auf die Benachrichtigung, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) für die im Steuerelement angezeigte Eigenschaft und der neue Wert angezeigt wird. 
  
Anzeigetabelle Benachrichtigungen können von einem Dienstanbieter verwendet werden, um Änderungen an verwandten Steuerelementen im Dialogfeld zu koordinieren. Wenn die Implementierung der Eigenschaftsschnittstelle beispielsweise ein oder mehrere Felder im Dialogfeld aktualisieren muss – möglicherweise als Reaktion auf ein anderes Steuerelement, das das DT_SET_IMMEDIATE-Flag in seiner **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))-Eigenschaft festgelegt hat – kann eine Anzeigetabelle generiert werden. Eine Anzeigetabelle Benachrichtigung kann die Implementierung der Eigenschaftsschnittstelle warnen, dass der Wert eines oder mehrere Steuerelemente aufgrund einer vorgenommenen Änderung oder eines externen Ereignisses erneut gelesen werden muss. 
  
Ein Dienstanbieter kann Benachrichtigungen zur Anzeigetabelle aus dem Folgenden erstellen:
  
- Aufrufen [von ITableData::HrNotify](itabledata-hrnotify.md), wenn die Anzeigetabelle mit einem Tabellendatenobjekt erstellt wurde.
    
    - Oder -
    
- Verwenden Sie eigenen Code, wenn die Anzeigetabelle mit der **IMAPITable-Implementierung** des Anbieters erstellt wurde. 
    
MAPI reagiert auf die Anzeige von Tabellenbenachrichtigungen, wenn dies erforderlich ist, indem der Wert eines Steuerelements aus der Implementierung der Eigenschaftsschnittstelle erneut gelesen wird. In der folgenden Tabelle werden die Details zur Art und Weise beschrieben, wie MAPI Benachrichtigungen für bestimmte Steuerelementtypen verarbeitet.
  
|**Control**|**MAPI-Aktion**|
|:-----|:-----|
|Schaltfläche  <br/> |Ruft [IMAPIProp::OpenProperty auf,](imapiprop-openproperty.md)um das Steuerelementobjekt über die Eigenschaft abzurufen, die durch das **ulPRControl-Element** der [DTBLBUTTON-Struktur](dtblbutton.md) dargestellt wird, wenn der Aufruf zuvor fehlgeschlagen war. Ruft im [IMAPIControl::GetState](imapicontrol-getstate.md) des Steuerelementobjekts auf, um zu bestimmen, ob die Schaltfläche aktiviert werden soll, und aktiviert oder deaktiviert die Schaltfläche entsprechend.  <br/> |
|Kontrollkästchen  <br/> |Der Wert für das **ulPRPropertyName-Element wird erneut** gelesen.  <br/> |
|Kombinationsfeld  <br/> |Öffnet die Tabelle, die dem **ulPRTableName-Element** der [DTBLCOMBOBOX-Struktur zugeordnet](dtblcombobox.md) ist. Alle Zeilen einschließlich des Werts für das **ulPRPropertyName-Element** werden erneut gelesen.  <br/> |
|Dropdownlistenfeld  <br/> |Öffnet die tabelle, die dem **ulPRTableName-Element** der [DTBLDDLBX-Struktur](dtblddlbx.md) zugeordnet ist, und alle Zeilen erneut. Ruft [IMAPIProp::GetProps auf,](imapiprop-getprops.md) um die Werte für die Eigenschaften abzurufen, die in **den UlPRDisplayProperty-** und **ulPRSetProperty-Membern gespeichert** sind.  <br/> |
|Bearbeiten  <br/> |Die Eigenschaft wird erneut gelesen und erneut angezeigt.  <br/> |
|Gruppenfeld  <br/> |Ignoriert die Benachrichtigung.  <br/> |
|Bezeichnung  <br/> |Ignoriert die Benachrichtigung.  <br/> |
|Listenfeld mit mehreren Auswahlen  <br/> |Wenn es sich bei einer der Spalten um einen Eintragsbezeichner handelt, wird das Listenfeld aktualisiert. Das entsprechende Objekt wird nicht geschlossen oder neu geladen.  <br/> |
|Listenfeld für einzelne Auswahl  <br/> |Liest die set-Eigenschaft und versucht, sie zu identifizieren.  <br/> |
|Mehrwertiges Listenfeld  <br/> |Die Eigenschaft wird erneut gelesen und das Listenfeld erneut aufgefüllt.  <br/> |
|Registerkartenseite  <br/> |Es gibt keine Benachrichtigungen für dieses Steuerelement. alles ist statisch.  <br/> |
|Optionsfeld  <br/> |Die Eigenschaft, die der Schaltfläche zugeordnet ist und im **ulPropTag-Element** der [DTBLRADIOBUTTON-Struktur](dtblradiobutton.md) gespeichert ist, wird erneut gelesen und mit den Steuerelementen die entsprechende Auswahl getroffen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

