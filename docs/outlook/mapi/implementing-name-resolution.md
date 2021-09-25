---
title: Implementieren der Namensauflösung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 62370da7b5ae4eadffd1d55564d363de7ea6415d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567305"
---
# <a name="implementing-name-resolution"></a>Implementieren der Namensauflösung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter sind für die Unterstützung der Namensauflösung verantwortlich – das Zuordnen eines Eintragsbezeichners zu einem Anzeigenamen. Clients initiieren die Namensauflösung, wenn sie [IAddrBook::ResolveName](iaddrbook-resolvename.md) aufrufen, um sicherzustellen, dass jedes Mitglied der Empfängerliste einer ausgehenden Nachricht einer gültigen Adresse entspricht. 
  
Ihr Anbieter kann die Namensauflösung wie folgt unterstützen:
  
- Unterstützung der **Eigenschaftseinschränkung PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), eine Anforderung für alle Adressbuchcontainer.
    
- Implementieren der [IABContainer::ResolveNames-Methode,](iabcontainer-resolvenames.md) eine Option für alle Adressbuchcontainer. 
    
If you choose to support **IABContainer::ResolveNames**, attempt to locate an exact match for each unresolved display name in the [ADRLIST](adrlist.md) structure passed in with the  _lpAdrList_ parameter. Sie können einen nicht aufgelösten Anzeigenamen identifizieren, da die **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) im Eigenschaftswertarray in seinem **aEntries-Element** der **ADRLIST-Struktur** fehlt. Ignorieren Sie alle Einträge, denen Nulleigenschaften zugeordnet sind. 
  
Melden Sie das Ergebnis des Auflösungsversuchs im Parameter  _lpFlagList,_ einem Array von Flags, das dem Array der Anzeigenamen in  _lpAdrList_ entspricht. Die Flags sind so positioniert, dass das erste Flag dem ersten **aEntries-Element** in der **ADRLIST-Struktur** entspricht, das zweite Flag dem zweiten **aEntries-Element** usw. 
  
Es gibt drei mögliche Ergebnisse für jeden nicht aufgelösten Eintrag:
  
- Es wurde keine Übereinstimmung gefunden, was bedeutet, dass keine der Einträge in Ihren Containereinträgen mit dem Eintrag in der **ADRLIST-Struktur** übereinstimmt. Legen Sie den entsprechenden Eintrag im  _lpFlagList-Parameter_ auf MAPI_UNRESOLVED fest. 
    
- Es können mehrere Übereinstimmungen gefunden werden, was bedeutet, dass mehrere Containereinträge vorhanden sind, die mit dem Eintrag in der **ADRLIST-Struktur** übereinstimmen. Legen Sie den entsprechenden Eintrag im  _parameter lpFlagList_ auf MAPI_AMBIGUOUS fest. Ändern Sie die Anzahl der Einträge in der **ADRLIST-Struktur** nicht. 
    
- Eine genaue Übereinstimmung kann gefunden werden, d. h., es gibt nur einen Containereintrag, der mit dem Eintrag in der **ADRLIST-Struktur** übereinstimmt. Legen Sie das entsprechende Element im  _lpFlagList-Parameter_ auf MAPI_RESOLVED fest, und fügen Sie den Eintragsbezeichner dem Array der Eigenschaften hinzu, die dem **ADRLIST-Eintrag** zugeordnet sind. 
    
Wenn Sie **IABContainer::ResolveNames** nicht unterstützen möchten, geben Sie MAPI_E_NO_SUPPORT aus Ihrer Implementierung zurück.
  
Alle Adressbuchanbieter müssen mehrdeutige Namensauflösungen – die **PR_ANR** Eigenschaftseinschränkung – in den Inhaltsverzeichnissen ihrer Container unterstützen. Um diese Unterstützung bereitzustellen, behandeln Sie die PR_ANR Einschränkung in Ihrer Implementierung von [IMAPITable::Restrict,](imapitable-restrict.md) indem Sie einen Suchtyp vom Typ "beste Schätzung" ausführen, der mit einer oder mehreren bestimmten Eigenschaften übereinstimmt, die für Ihren Anbieter sinnvoll sind. Sie können die gleiche Eigenschaft oder Eigenschaften jedes Mal verwenden, z. **B. PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), oder einem Administrator die Auswahl aus einer Liste zulässiger Eigenschaften gestatten. 
  
Obwohl die meisten Anbieter ihre eigene Inhaltstabellenimplementierung bereitstellen, können Sie die von der MAPI bereitgestellte Implementierung über die [CreateTable-Funktion](createtable.md) anpassen. Da die MAPI-Implementierung jedoch keine Einschränkungen jeder Art unterstützt, müssen Sie ein Wrapperobjekt erstellen, um eine angepasste Version von **Restrict** einzuschließen, die den Aufruf abfängt. 
  

