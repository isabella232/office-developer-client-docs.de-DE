---
title: Implementieren der Namensauflösung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15c1d502947865c02973f4950b6b6fa8109b8e78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434704"
---
# <a name="implementing-name-resolution"></a>Implementieren der Namensauflösung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter sind für die Unterstützung der Namensauflösung verantwortlich – das Zuordnen einer Eintrags-ID zu einem Anzeigenamen. Clients initiieren die Namensauflösung, wenn [sie IAddrBook::ResolveName aufrufen,](iaddrbook-resolvename.md) um sicherzustellen, dass jedes Mitglied der Empfängerliste einer ausgehenden Nachricht einer gültigen Adresse entspricht. 
  
Ihr Anbieter kann die Namensauflösung unterstützen, indem er:
  
- Unterstützung der **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) -Eigenschaftseinschränkung, eine Anforderung für alle Adressbuchcontainer.
    
- Implementieren der [IABContainer::ResolveNames-Methode,](iabcontainer-resolvenames.md) eine Option für alle Adressbuchcontainer. 
    
Wenn Sie **IABContainer::ResolveNames** unterstützen möchten, versuchen Sie, eine genaue Übereinstimmung für jeden nicht aufgelösten Anzeigenamen in der [ADRLIST-Struktur](adrlist.md) zu finden, die mit dem  _lpAdrList-Parameter_ übergeben wurde. Sie können einen nicht aufgelösten Anzeigenamen identifizieren, da die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft im Eigenschaftswertarray in seinem **aEntries-Element** der **ADRLIST-Struktur** fehlt. Ignorieren Sie alle Einträge, deren Eigenschaften null zugeordnet sind. 
  
Melden Sie das Ergebnis Ihres Lösungsversuchs im _lpFlagList-Parameter,_ einem Array von Flags, das dem Array der Anzeigenamen in _lpAdrList entspricht._ Die Flags sind so positionierend, dass das erste Flag dem ersten **aEntries-Element** in der **ADRLIST-Struktur** entspricht, das zweite Flag dem zweiten **aEntries-Element** und so weiter. 
  
Es gibt drei mögliche Ergebnisse für jeden nicht aufgelösten Eintrag:
  
- Es wurde keine Übereinstimmung gefunden, d. h. keiner der Einträge in Ihren Containereinträgen ist mit dem Eintrag in der **ADRLIST-Struktur** übereinstimmend. Legen Sie den entsprechenden Eintrag im  _lpFlagList-Parameter_ auf MAPI_UNRESOLVED. 
    
- Es können mehrere Übereinstimmungen gefunden werden, d. h. es gibt mehrere Containereinträge, die mit dem Eintrag in der **ADRLIST-Struktur** übereinstimmen. Legen Sie den entsprechenden Eintrag im  _lpFlagList-Parameter_ auf MAPI_AMBIGUOUS. Ändern Sie die Anzahl der Einträge in der **ADRLIST-Struktur nicht.** 
    
- Eine genaue Übereinstimmung kann gefunden werden, d. h., es gibt nur einen Containereintrag, der dem Eintrag in der **ADRLIST-Struktur** entspricht. Legen Sie das entsprechende Element im  _lpFlagList-Parameter_ auf MAPI_RESOLVED und fügen Sie den Eintragsbezeichner dem Array von Eigenschaften hinzu, das dem **ADRLIST-Eintrag zugeordnet** ist. 
    
Wenn Sie **IABContainer::ResolveNames** nicht unterstützen möchten, geben Sie MAPI_E_NO_SUPPORT Implementierung zurück.
  
Alle Adressbuchanbieter müssen die mehrdeutige Namensauflösung  – die Einschränkung der PR_ANR - für die Inhaltstabellen ihrer Container unterstützen. Um diese Unterstützung zu bieten, behandeln Sie die PR_ANR-Einschränkung in Ihrer Implementierung von [IMAPITable::Restrict,](imapitable-restrict.md) indem Sie einen Suchtyp "best guess" ausführen, der mit einer oder mehreren bestimmten Eigenschaften abgleicht, die für Ihren Anbieter sinnvoll sind. Sie können die gleiche Eigenschaft oder Eigenschaften jedes Mal verwenden, z. B. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), oder einem Administrator die Auswahl aus einer Liste akzeptabler Eigenschaften erlauben. 
  
Obwohl die meisten Anbieter eigene Inhaltstabellenimplementierung liefern, können Sie die von MAPI bereitgestellte Implementierung über die [CreateTable-Funktion](createtable.md) anpassen. Da die MAPI-Implementierung jedoch keine Einschränkungen jeglicher Art unterstützt, müssen Sie ein Wrapperobjekt erstellen, das eine angepasste Version von **Restrict** enthält, die den Aufruf abfängt. 
  

