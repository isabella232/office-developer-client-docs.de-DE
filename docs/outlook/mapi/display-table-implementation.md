---
title: Anzeigen der Tabellenimplementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e31dd7b25b3abf333505c8bde57f61be7a10901
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580607"
---
# <a name="display-table-implementation"></a>Anzeigen der Tabellenimplementierung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zeigt die Tabelle wird verwendet, um ein Eigenschaftenblatt spezielle ein Dialogfeld, das aus der einen oder mehrere im Registerkartenformat Eigenschaftenseiten zum Anzeigen und Bearbeiten von möglicherweise eine oder mehrere Eigenschaften anzeigen. Verknüpft ist mit jedem Display-Tabelle ist eine [IAttach: IMAPIProp](iattachimapiprop.md) Schnittstelle Implementierung. Die Implementierung [IMAPIProp](imapipropiunknown.md) verwaltet die Daten, die im Eigenschaftenfenster angezeigt werden. 
  
Die Zeilen in einer Tabelle anzeigen darstellen der Steuerelemente im Eigenschaftenfenster. Die meisten Steuerelemente können mit der Implementierung **IMAPIProp** verwaltet Eigenschaften zugeordnet werden. Wenn ein Benutzer den Wert eines Steuerelements änderbare ändert, wird die entsprechende Eigenschaft aktualisiert. 
  
Die Spalten in einer Tabelle anzeigen dargestellt Eigenschaften des Steuerelements, wie ihre Position im Eigenschaftenfenster, dessen Typ, zugeordnete-Struktur und Bezeichner. Eine vollständige Liste der erforderlichen Anzeige Tabellenspalten finden Sie unter [Tabellen angezeigt](display-tables.md).
  
MAPI wird dem Benutzer von einer Clientanwendung aus einem Eigenschaftenfenster Eigenschaftswerte aus der **IMAPIProp** Implementierung der Anzeige-Tabelle zugeordnet oder aus der Tabelle anzeigen direktem lesen angezeigt. Der Benutzer mit dem Eigenschaftenfenster arbeitet, ruft Ändern der Werte in den Steuerelementen MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) zum Speichern eines geänderten Steuerelements, wenn das Steuerelement DT_SET_IMMEDIATE Flag festgelegt ist. Für Steuerelemente ohne das DT_SET_IMMEDIATE-Flag festgelegt werden Änderungen an Eigenschaften gespeichert, wenn der Benutzer das Dialogfeld schließt, indem Sie auf die Schaltfläche **OK** oder **Übernehmen** . Wenn eine der folgenden Schaltflächen oder die Schaltfläche **Abbrechen** geklickt wird, werden MAPI Eigenschaftenfenster aus der Ansicht entfernt. 
  
MAPI erhält Zugriff auf Ihre zeigt die Tabelle aus, entweder durch Aufrufen der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode in der Implementierung **IMAPIProp** und die Eigenschaft **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) anfordern oder durch erben ihn in einen Rufen Sie, dass Sie MAPI, wie etwa [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)vorgenommen haben.
  
Die erste Access Technik wird verwendet, wenn von adressbuchanbietern implementierte zum Anzeigen von Details zu messaging Benutzer oder Verteilerlisten aufgefordert werden. Die folgende Vorgänge ausgeführt:
  
1. Ein Client Ruft die [IAddrBook::Details](iaddrbook-details.md) -Methode. 
    
2. MAPI-Aufrufen der Adressbuchanbieter [IABLogon::OpenEntry](iablogon-openentry.md) -Methode, um die messaging-Benutzer zugreifen, der den ausgewählten Eintrag darstellt. 
    
3. MAPI-Aufrufen [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Abrufen der **PR_DETAILS_TABLE** -Eigenschaft der Tabelle anzeigen im Dialogfeld Details der messaging-Benutzer. 
    
4. MAPI zeigt das Dialogfeld behandeln Interaktion mit den Informationen des Benutzers und entfernt sie, wenn der Benutzer abgeschlossen hat. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

