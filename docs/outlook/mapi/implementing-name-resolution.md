---
title: Implementieren von namensauflösung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4d55404149baca07a64b75d460bdfb2a8c541725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792559"
---
# <a name="implementing-name-resolution"></a>Implementieren von namensauflösung

  
  
**Betrifft**: Outlook 
  
Von adressbuchanbietern implementierte sind verantwortlich für die Unterstützung von namensauflösung – der Vorgang der Zuordnung eines Eintrags-ID mit dem Anzeigenamen. Clients initiieren namensauflösung beim Aufruf [IAddrBook::ResolveName](iaddrbook-resolvename.md) , um sicherzustellen, dass jedes Mitglied eine ausgehende Nachricht Empfängerliste in eine gültige Adresse entspricht. 
  
Auflösung von kann Ihren Anbieter unterstützt werden:
  
- Unterstützung der eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), eine Voraussetzung für alle Address Book Container.
    
- Implementieren der [IABContainer](iabcontainer-resolvenames.md) -Methode, eine Option für alle Address Book Container. 
    
Wenn Sie versuchen, eine genaue Übereinstimmung für jeden nicht aufgelösten Anzeigename in der [ADRLIST](adrlist.md) -Struktur, die mit der _LpAdrList_ -Parameter übergebene suchen, unterstützt **IABContainer**auswählen. Sie können identifizieren Sie eine nicht aufgelöste Anzeigename, da es in der Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) im Array Eigenschaft Wert in seine **aEntries** Mitglied der **ADRLIST** -Struktur fehlt. Ignorieren Sie alle Einträge, die keine Eigenschaften zugeordnet haben. 
  
Melden Sie das Ergebnis Ihrer Versuch der Lösung im Parameter _LpFlagList_ , ein Array von Flags, die das Array von Anzeigenamen in _LpAdrList_entspricht. Die Flags sind positionelle so, dass das erste Flag auf den ersten **aEntries** Member in der Struktur **ADRLIST** entspricht, das zweite Flag entspricht der zweite **aEntries** Member usw.. 
  
Es gibt drei mögliche Ergebnisse für jeden nicht aufgelösten Eintrag:
  
- Keine Übereinstimmung wurde gefunden, was bedeutet, dass keines der Einträge in der Container-Einträge der Eintrag in der Struktur **ADRLIST** übereinstimmen. Legen Sie den entsprechenden Eintrag in der Parameter _LpFlagList_ MAPI_UNRESOLVED. 
    
- Was bedeutet, dass es sind mehrere Container Einträge, die den Eintrag in der Struktur **ADRLIST** entsprechen können mehrere Übereinstimmungen gefunden werden. Legen Sie den entsprechenden Eintrag in der Parameter _LpFlagList_ MAPI_AMBIGUOUS. Die Anzahl der Einträge in der Struktur **ADRLIST** nicht geändert. 
    
- Eine genaue Übereinstimmung kann gefunden werden, d. h., es ist nur ein Container-Eintrag, der den Eintrag in der Struktur **ADRLIST** übereinstimmt. Legen Sie den entsprechenden Member im Parameter _LpFlagList_ für MAPI_RESOLVED, und fügen Sie die Eintrags-ID in das Array mit den Eintrag **ADRLIST** zugeordneten Eigenschaften. 
    
Wenn Sie nicht zur Unterstützung von **IABContainer**auswählen, geben die Implementierung MAPI_E_NO_SUPPORT zurück.
  
Alle von adressbuchanbietern implementierte sind erforderlich, um die Auflösung nicht eindeutiger Namen unterstützen – der **PR_ANR** eigenschaftseinschränkung – für ihre Container Inhalt Tabellen. Um diese zu unterstützen, behandeln Sie die PR_ANR Einschränkung in der Implementierung der [Methode IMAPITable:: Restrict](imapitable-restrict.md) durch Ausführen eines "am besten erraten" Typs der Übereinstimmung mit einer oder mehrerer bestimmte Eigenschaften, die für den Anbieter sinnvoll-Suche. Sie können auswählen, damit ein Administrator eine Liste der zulässigen Eigenschaften aus oder verwenden Sie die gleiche Eigenschaft oder Eigenschaften jedes Mal, wie **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)). 
  
Obwohl die meisten Anbieter eigene Inhalt Tabelle Implementierung angeben, können Sie die Implementierung von MAPI bereitgestellt wird, über die Funktion [CreateTable](createtable.md) anpassen. Allerdings, da die MAPI-Implementierung Einschränkungen jeglicher Art nicht unterstützt, müssen Sie erstellen ein Wrapperobjekt, um einer benutzerdefinierten Version **Restrict** enthalten, die den Anruf fängt ab. 
  

